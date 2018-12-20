<template>
  <div class="screen">
    <div class="screen__bezel">
      <div class="screen__inside">
        Screen
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Screen'
};
</script>

<style lang="scss" scoped>
@import './../styles/variables.scss';

$bezelSize: 20; // px
.screen {
  width: 100%;
  height: 100%;

  &__bezel {
    padding: em($bezelSize);
    height: calc(100% - (#{$bezelSize}px * 2));
    background-color: #000;
  }

  &__inside {
    background-color: #fff;
    width: 100%;
    height: 100%;
  }
}
</style>
