<template>
  <div class="joycon-left">
    <div class="joycon-left__minus"></div>
    <div class="joycon-left__analog"></div>
    <div class="joycon-left__d-pad-container">
      <div :class="{'d-pad-button--on': keyStatus.up}" class="d-pad-button d-pad-up"></div>
      <div :class="{'d-pad-button--on': keyStatus.left}" class="d-pad-button d-pad-left"></div>
      <div :class="{'d-pad-button--on': keyStatus.right}" class="d-pad-button d-pad-right"></div>
      <div :class="{'d-pad-button--on': keyStatus.down}" class="d-pad-button d-pad-down"></div>
    </div>
    <div class="joycon-left__screenshot"></div>
  </div>
</template>

<script>
export default {
  name: 'JoyConLeft',
  props: ['keyStatus']
};
</script>

<style lang="scss">
@import '../styles/variables.scss';

.joycon-left {
  position: absolute;
  height: 100%;
  width: 15%;
  background: $joycon-blue;
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;

  &__minus {
    position: absolute;
    height: 3%;
    width: 19%;
    top: 6%;
    right: 5%;
    background: black;
    border-radius: 50px;
  }

  &__analog {
    position: absolute;
    border-radius: 50%;
    background: black;
    height: 13%;
    width: 40%;
    top: 20%;
    left: 25%;
    border: solid 5px #202226;
  }

  &__d-pad-container {
    position: absolute;
    height: 23%;
    width: 70%;
    left: 15%;
    background: none;
    top: 45%;
  }

  &__screenshot {
    position: absolute;
    bottom: 15%;
    right: 13%;
    height: 7%;
    width: 23%;
    background: black;
  }
}
</style>
