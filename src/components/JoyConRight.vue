<template>
  <div class="joy-con-right">
    <div class="analog-right"></div>
    <div class="circle-button-right"></div>
    <div class="d-pad-container-right">
      <div :class="{'d-pad-button--on': keyStatus.up}" class="d-pad-button d-pad-up"></div>
      <div :class="{'d-pad-button--on': keyStatus.left}" class="d-pad-button d-pad-left"></div>
      <div :class="{'d-pad-button--on': keyStatus.right}" class="d-pad-button d-pad-right"></div>
      <div :class="{'d-pad-button--on': keyStatus.down}" class="d-pad-button d-pad-down"></div>
    </div>
    <div class="d-pad-2-container">
      <div class="d-pad-2-vertical"></div>
      <div class="d-pad-2-horizontal"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'JoyConRight',
  props: ['keyStatus']
};
</script>


<style lang="scss" scoped>
.joy-con-right {
  position: absolute;
  height: 100%;
  width: 15%;
  right: 0%;
  background: #737a80;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
}

.analog-right {
  position: absolute;
  border-radius: 50%;
  background: black;
  height: 13%;
  width: 40%;
  top: 50%;
  left: 25%;
  border: solid 5px #202226;
}

.circle-button-right {
  position: absolute;
  border-radius: 50%;
  background: black;
  height: 3%;
  width: 10%;
  bottom: 18%;
  left: 10%;
  border: solid 5px #202226;
}

.d-pad-container-right {
  position: absolute;
  height: 23%;
  width: 70%;
  left: 15%;
  background: none;
  top: 20%;
}

.d-pad-2-container {
  position: absolute;
  background: none;
  height: 8%;
  width: 25%;
  top: 3%;
  left: 8%;
}

.d-pad-2-vertical {
  position: absolute;
  height: 100%;
  background: black;
  width: 35%;
  left: 32.5%;
}

.d-pad-2-horizontal {
  position: absolute;
  width: 100%;
  background: black;
  height: 35%;
  top: 32.5%;
}
</style>
