<template>
  <div class="games-list">
    <div class="games-list__container">
      <Game
        v-for="game in games"
        :game="game"
        v-bind:key="game.id">
      </Game>
    </div>
  </div>
</template>

<script>
import Game from '@/components/Game.vue';

export default {
  props: ['games'],
  components: {
    Game
  }
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';

.games-list {
  width: 100%;
  height: 100%;
  padding-left: em(20);

  &__container {
    width: 100%;
    height: 100%;
    position: absolute;
    overflow-x: scroll;
    overflow-y: hidden;
    white-space: nowrap;
    display: flex;
  }
}
</style>
