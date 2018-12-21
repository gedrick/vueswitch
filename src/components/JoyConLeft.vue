<template>
  <div class="joy-con-left">
    <div class="ellipse-button"></div>
    <div class="analog-left"></div>
    <div class="d-pad-container-left">
      <div :class="{'d-pad-button--on': keyStatus.up}" class="d-pad-button d-pad-up"></div>
      <div :class="{'d-pad-button--on': keyStatus.left}" class="d-pad-button d-pad-left"></div>
      <div :class="{'d-pad-button--on': keyStatus.right}" class="d-pad-button d-pad-right"></div>
      <div :class="{'d-pad-button--on': keyStatus.down}" class="d-pad-button d-pad-down"></div>
    </div>
    <div class="square-button"></div>
  </div>
</template>

<script>
export default {
  name: 'JoyConLeft',
  props: ['keyStatus']
};
</script>

<style lang="scss">
.joy-con-left {
  position: absolute;
  height: 100%;
  width: 15%;
  background: #737a80;
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;
}

.ellipse-button {
  position: absolute;
  height: 3%;
  width: 30%;
  top: 8%;
  right: 5%;
  background: black;
  border-radius: 50px;
}

.analog-left {
  position: absolute;
  border-radius: 50%;
  background: black;
  height: 13%;
  width: 40%;
  top: 20%;
  left: 25%;
  border: solid 5px #202226;
}

.d-pad-container-left {
  position: absolute;
  height: 23%;
  width: 70%;
  left: 15%;
  background: none;
  top: 45%;
}

.square-button {
  position: absolute;
  bottom: 15%;
  right: 13%;
  height: 7%;
  width: 23%;
  background: black;
}
</style>
