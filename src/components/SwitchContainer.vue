<template>
  <div class="switch-container">
    <JoyConLeft :keyStatus="keyStatus.dPadLeft"></JoyConLeft>
    <JoyConRight :keyStatus="keyStatus.dPadRight"></JoyConRight>
    <SwitchScreen></SwitchScreen>
  </div>
</template>

<script>
import JoyConLeft from '@/components/JoyConLeft.vue';
import JoyConRight from '@/components/JoyConRight.vue';
import SwitchScreen from '@/components/SwitchScreen.vue';

export default {
  components: {
    JoyConLeft,
    JoyConRight,
    SwitchScreen
  },
  data() {
    return {
      keyStatus: {
        dPadLeft: {
          up: false,
          down: false,
          left: false,
          right: false
        },
        dPadRight: {
          up: false,
          down: false,
          left: false,
          right: false
        }
      }
    };
  },
  mounted() {
    window.addEventListener('keydown', this.processKeyEvent.bind(this));
    window.addEventListener('keyup', this.processKeyEvent.bind(this));
  },
  methods: {
    processKeyEvent(e) {
      const val = e.type === 'keydown';
      switch (e.key) {
        case 'w':
          this.keyStatus.dPadLeft.up = val;
          break;
        case 'a':
          this.keyStatus.dPadLeft.left = val;
          break;
        case 's':
          this.keyStatus.dPadLeft.down = val;
          break;
        case 'd':
          this.keyStatus.dPadLeft.right = val;
          break;
        case 'ArrowUp':
          this.keyStatus.dPadRight.up = val;
          break;
        case 'ArrowLeft':
          this.keyStatus.dPadRight.left = val;
          break;
        case 'ArrowDown':
          this.keyStatus.dPadRight.down = val;
          break;
        case 'ArrowRight':
          this.keyStatus.dPadRight.right = val;
          break;
      }
    }
  }
};
</script>

<style lang="scss">
.switch-container {
  position: absolute;
  width: 80%;
  height: 60%;
  background: none;
  top: 20%;
  left: 10%;
}

.d-pad-up {
  position: absolute;
  height: 30%;
  width: 30%;
  left: 35%;
  top: 0%;
  background: black;
  border-radius: 50%;
}

.d-pad-down {
  position: absolute;
  height: 30%;
  width: 30%;
  left: 35%;
  bottom: 0%;
  background: black;
  border-radius: 50%;
}

.d-pad-left {
  position: absolute;
  height: 30%;
  width: 30%;
  left: 0%;
  top: 35%;
  background: black;
  border-radius: 50%;
}

.d-pad-right {
  position: absolute;
  height: 30%;
  width: 30%;
  right: 0%;
  top: 35%;
  background: black;
  border-radius: 50%;
}

.d-pad-button {
  &--on {
    background-color: blue;
  }
}
</style>
