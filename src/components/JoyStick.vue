<template>
  <div class="joystick" :class="'joystick--' + side">
    <div class="joystick__inner"></div>
  </div>
</template>

<script>
export default {
  name: 'JoyStick',
  props: ['side']
};
</script>

<style lang="scss" scoped>
.joystick {
  height: 4em;
  width: 4em;
  border-radius: 100%;
  position: absolute;
  background-color: gray;
  z-index: 5;

  &--left {
    top: 5em;
    left: calc(50% - 2em);
    right: unset;
  }
  &--right {
    top: 12em;
    left: unset;
    right: calc(50% - 2em);
  }

  &__inner {
    position: absolute;
    width: 3em;
    height: 3em;
    border-radius: 100%;
    top: 12%;
    left: 12%;
    background-color: #000;
    z-index: 10;
  }
}
</style>
