<template>
  <div class="screen-outer">
    <div class="screen-inner">
      <div class="logo-left">
        <div class="logo-ball-left"></div>
      </div>
      <div class="logo-right">
        <div class="logo-ball-right"></div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.screen-outer {
  position: absolute;
  background: none;
  width: 70%;
  left: 15%;
  background: black;
  height: 100%;
}

.screen-inner {
  position: absolute;
  background: none;
  width: 90%;
  left: 5%;
  top: 5%;
  background: #e60001;
  height: 90%;
}

.logo-left {
  position: absolute;
  height: 60%;
  width: 16%;
  left: 25%;
  top: 16%;
  background: #e60001;
  border: solid 8px white;
  border-top-left-radius: 30px;
  border-bottom-left-radius: 30px;
}

.logo-right {
  position: absolute;
  height: 60%;
  width: 16%;
  right: 25%;
  top: 16%;
  background: white;
  border: solid 8px white;
  border-top-right-radius: 30px;
  border-bottom-right-radius: 30px;
}

.logo-ball-left {
  position: absolute;
  border-radius: 50%;
  background: white;
  height: 20%;
  width: 50%;
  top: 15%;
  left: 25%;
  animation: move-it-left 2s infinite;
}

.logo-ball-right {
  position: absolute;
  border-radius: 50%;
  background: #e60001;
  height: 20%;
  width: 50%;
  bottom: 15%;
  left: 25%;
  animation: move-it-right 2s infinite;
}

//css animations
@keyframes move-it-left {
  0% {
    top: 15%;
  }
  50% {
    top: 80%;
  }
  100% {
    top: 15%;
  }
}

@keyframes move-it-right {
  0% {
    bottom: 15%;
  }
  50% {
    bottom: 80%;
  }
  100% {
    bottom: 15%;
  }
}
</style>
