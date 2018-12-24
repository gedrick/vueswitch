<template>
  <div
    class="game"
    :class="{'game--selected': selected, 'game--rows': rows > 1}"
    :style="{'height': size + 'vw','width': size + 'vw'}">
    <div class="game__box">
      <!-- <img :src="gameImage" :alt="game.title"> -->
    </div>
    <div class="game__title">
      {{game.title}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Game',
  props: ['game', 'rows', 'selected'],
  data() {
    return {
      baseSize: 20
    };
  },
  computed: {
    size() {
      return this.baseSize / this.rows;
    },
    gameImage() {
      const gameImageUrl = this.game.image;
      if (gameImageUrl.startsWith('http')) {
        return gameImageUrl;
      } else {
        return `assets/${gameImageUrl}`;
      }
    }
  }
};
</script>

<style lang="scss">
@import '../styles/variables.scss';

.game {
  display: grid;
  grid-template-rows: 80% 20%;
  transition-property: width, height;
  transition-duration: 0.4s;
  transition-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1.275);

  &--selected &__box {
    outline: em(2) inset cyan;
  }

  &--rows {
    grid-template-rows: auto;
  }

  &--rows &__title {
    display: none;
  }

  &__box {
    background-color: white;
    width: 100%;
    height: 100%;

    img {
      width: 100%;
      height: 100%;
    }
  }

  &__title {
    @include alignCenter;
    color: white;
    font-size: em(12);

    &--hidden {
      display: none;
    }
  }
}
</style>
