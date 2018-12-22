<template>
  <div class="game-list">
    <Game
      v-for="game in games"
      :game="game"
      :key="game.id">
    </Game>
  </div>
</template>

<script>
import Game from './Game.vue';

export default {
  name: 'GameList',
  components: {
    Game
  },
  props: ['games']
};
</script>


<style lang="scss" scoped>
@import '../styles/variables.scss';

.game-list {
  @include alignCenter;
  background-color: blue;
}
</style>
