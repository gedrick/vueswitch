<template>
  <div class="joycon" :class="'joycon--' + side">
    <div class="joycon__controls joycon__controls--left">
      <ButtonMinus></ButtonMinus>
      <JoyStick side="left"></JoyStick>
      <ControllerButtons></ControllerButtons>
    </div>
    <div class="joycon__controls joycon__controls--right">
      <JoyStick side="right"></JoyStick>
    </div>
  </div>
</template>

<script>
import ButtonMinus from '@/components/ButtonMinus.vue';
import JoyStick from '@/components/JoyStick.vue';
import ControllerButtons from '@/components/ControllerButtons.vue';

export default {
  components: {
    ButtonMinus,
    JoyStick,
    ControllerButtons
  },
  props: ['side']
};
</script>

<style lang="scss" scoped>
$border-radius-size: 20px;

.joycon {
  width: 15%;
  height: 100%;
  z-index: 10;

  &--left {
    background-color: blue;
    border-radius: $border-radius-size 0 0 $border-radius-size;
  }

  &--right {
    border-radius: 0 $border-radius-size $border-radius-size 0;
    background-color: red;
  }

  &__controls {
    position: relative;
    width: 100%;
    height: 100%;
    display: none;

    .joycon--left &--left {
      display: block;
    }
    .joycon--right &--right {
      display: block;
    }
  }
}
</style>
