<template>
  <div class="switch-container">
    <JoyConLeft :keyStatus="leftKeyStatus"></JoyConLeft>
    <JoyConRight></JoyConRight>
    <ScreenOuter></ScreenOuter>
  </div>
</template>


<script>
import JoyConLeft from '@/components/JoyConLeft.vue';
import JoyConRight from '@/components/JoyConRight.vue';
import ScreenOuter from '@/components/ScreenOuter.vue';

export default {
  components: {
    JoyConLeft,
    JoyConRight,
    ScreenOuter
  },
  data() {
    return {
      keyStatus: {
        dPadLeft: {
          top: false,
          bottom: false,
          left: false,
          right: false
        },
        dPadRight: {
          top: false,
          bottom: false,
          left: false,
          right: false
        }
      }
    };
  },
  computed: {
    leftKeyStatus() {
      return {
        dPad: {
          top: false,
          bottom: false,
          left: false,
          right: false
        }
      };
    }
  },
  mounted() {
    window.addEventListener('keydown', this.processKeyEvent.bind(this));
    window.addEventListener('keyup', this.processKeyEvent.bind(this));
  },
  methods: {
    processKeyEvent(e) {
      const key = e.key;
      const val = e.type === 'keydown';
      switch (key) {
        case 'w':
          this.keyStatus.dPadLeft.top = val;
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
          this.keyStatus.dPadRight.top = val;
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

.d-pad-top {
  position: absolute;
  height: 30%;
  width: 30%;
  left: 35%;
  top: 0%;
  background: black;
  border-radius: 50%;
}

.d-pad-bottom {
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
</style>
