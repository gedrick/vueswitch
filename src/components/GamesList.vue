<template>
  <div class="games-list">
    <Game
      v-for="game in games"
      v-bind:key="game.id">
    </Game>
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
  background-color: red;
}
</style>
