<template>
  <div class="screen">
    <div class="screen__bezel">
      <div class="screen__inside">
        <Profiles class="screen__block-profiles"></Profiles>
        <div class="clock"></div>
        <div class="games"></div>
        <div class="controls"></div>
        <div class="footer"></div>
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
  padding: 1em;
  background-color: #000;

  &__bezel {
    height: 100%;
  }

  &__inside {
    color: #000;
    height: 100%;
    background-color: #fff;
  }

  &__block-profiles {
    height: em(2);
  }
}
</style>
