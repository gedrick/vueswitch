<template>
  <div class="game-list" :class="'game-list--' + rows + 'row'">
    <div ref="gameList" class="game-list__container">
      <Game
        v-for="game in games"
        :game="game"
        :modifier="rows"
        :key="game.id">
      </Game>
    </div>
  </div>
</template>

<script>
import Game from './Game.vue';

export default {
  name: 'GameList',
  components: {
    Game
  },
  props: ['games', 'rows'],
  data() {
    return {
      boundHandleScroll: this.handleScroll.bind(this)
    };
  },
  mounted() {
    this.$refs.gameList.addEventListener('mousewheel', this.boundHandleScroll);
  },
  destroyed() {
    this.$refs.gameList.removeEventListener(
      'mousewheel',
      this.boundHandleScroll
    );
  },
  methods: {
    handleScroll(e) {
      this.$refs.gameList.scrollLeft += e.deltaY;
    }
  }
};
</script>


<style lang="scss" scoped>
@import '../styles/variables.scss';

.game-list {
  @include alignCenter;
  justify-content: flex-start;
  background-color: blue;
  overflow: hidden;
  padding-top: 5%;

  &__container {
    display: grid;
    grid-gap: em(5);
    overflow-x: hidden;
    overflow-y: hidden;
    height: 100%;
    grid-auto-flow: column;
  }

  &--1row &__container {
    grid-auto-columns: 40%;
  }

  &--2row &__container {
    grid-auto-rows: 50%;
    grid-template-rows: 50% 50%;
  }

  &--3row &__container {
    grid-auto-rows: 33%;
    grid-template-rows: 33% 33% 33%;
  }
}
</style>
