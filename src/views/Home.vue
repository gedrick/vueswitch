<template>
  <div class="container">
    <SwitchContainer></SwitchContainer>
  </div>
</template>

<script>
import SwitchContainer from '@/components/SwitchContainer.vue';

export default {
  name: 'Home',
  components: {
    SwitchContainer
  }
};
</script>

<style lang="scss">
@import './../styles/variables.scss';

body {
  overflow: hidden;
  height: 100vh;
  font-size: 16px;
  margin: 0;
  padding: 0;
  font-family: $base-font;
  background-image: linear-gradient(-45deg, #0074df, #003f78);
}

.container {
  // transform: scale(1.1);
  position: relative;
  display: block;
  margin: auto;
  margin-top: 8%;
  background: none;
  border: none;
  height: 56.25vw;
  width: 100vw;

  @include breakpoint($mobile) {
    height: 100vh;
  }
}
</style>
