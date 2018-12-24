<template>
  <div class="game-list" :class="'game-list--' + rows + 'row'">
    <div ref="gameList" class="game-list__container">
      <Game
        v-for="(game, index) in games"
        :game="game"
        :selected="index === selectedIndex"
        :rows="rows"
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
      selectedIndex: 0,
      boundHandleScroll: this.handleScroll.bind(this)
    };
  },
  mounted() {
    this.$refs.gameList.addEventListener('mousewheel', this.boundHandleScroll);
  },
  beforeDestroy() {
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

$grid-gap: 3px;

.game-list {
  @include alignCenter;
  justify-content: flex-start;
  background-color: blue;
  overflow: hidden;
  padding-top: 5%;

  &__container {
    display: grid;
    grid-gap: $grid-gap;
    overflow-x: auto;
    overflow-y: hidden;
    height: 100%;
    grid-auto-flow: column;
    padding-left: em(20);
    // grid-template-rows: 100%;
  }

  $row-width-2: calc(50% - (#{$grid-gap} * 2));
  &--2row &__container {
    grid-auto-rows: 50%;
    grid-template-rows: $row-width-2 $row-width-2;
  }

  $row-width-3: calc(33% - (#{$grid-gap} * 1.5));
  &--3row &__container {
    grid-template-rows: $row-width-3 $row-width-3 $row-width-3;
    grid-auto-rows: 33%;
  }
}
</style>
