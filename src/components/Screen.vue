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
import Profiles from '@/components/Profiles.vue';

export default {
  components: {
    Profiles
  }
};
</script>

<style lang="scss" scoped>
@import './../styles/variables.scss';

.screen {
  width: 100%;
  height: 100%;

  &__bezel {
    padding: em(20);
    height: calc(100% - 40px);
    background-color: #000;
  }

  &__inside {
    background-color: #fff;
    width: 100%;
    height: 100%;
  }
}
</style>
