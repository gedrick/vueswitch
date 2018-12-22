<template>
  <div class="game">
    <div class="game__box">
      <img :src="game.image" :alt="game.title">
    </div>
    <div class="game__title">
      {{game.title}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Game',
  props: ['game']
};
</script>

<style lang="scss">
@import '../styles/variables.scss';

.game {
  width: $game-size;
  height: $game-size;
  background-color: green;
  display: grid;
  grid-template-rows: 85% 15%;

  &__box {
    background-color: cyan;

    img {
      width: 100%;
      height: 100%;
    }
  }

  &__title {
    @include alignCenter;
  }
}
</style>
