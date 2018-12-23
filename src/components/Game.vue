<template>
  <div class="game" :style="{'height': size + 'vw', 'width': size + 'vw'}">
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
  props: ['game', 'modifier'],
  data() {
    return {
      baseSize: 20
    };
  },
  computed: {
    size() {
      return this.baseSize / this.modifier;
    }
  }
};
</script>

<style lang="scss">
@import '../styles/variables.scss';

.game {
  display: grid;
  grid-template-rows: 80% 20%;

  &__box {
    img {
      width: 100%;
      height: 100%;
    }
  }

  &__title {
    @include alignCenter;
    color: white;
    font-size: em(12);
  }
}
</style>
