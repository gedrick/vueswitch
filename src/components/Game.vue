<template>
  <div class="game">
    <div class="game__image">
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

<style lang="scss" scoped>
@import '@/styles/variables.scss';
.game {
  // float: left;
  height: 15vw;
  width: 15vw;
  background-color: cyan;
  border: 1px solid black;
  margin-right: em(10);
}
</style>
