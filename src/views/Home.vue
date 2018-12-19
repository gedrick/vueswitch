<template>
  <div class="home">
    <div class="box">
      <Stage></Stage>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Stage from '@/components/Stage.vue';

export default {
  components: {
    Stage
  },
  name: 'home',
  data: () => {
    return {
      isMounted: false
    };
  },
  mounted() {
    this.isMounted = true;
  },
  computed: {
    width() {
      if (!this.isMounted) {
        return null;
      }
      return this.$el.offsetWidth;
    },
    height() {
      if (!this.isMounted) {
        return null;
      }
      return this.$el.offsetHeight;
    }
  }
};
</script>

<style lang="scss">
@import './../styles/variables.scss';

body {
  font-size: 16px;
  margin: 0;
  padding: 0;
}

.home {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.box {
  width: em(568);
  height: 320px;
  @include breakpoint($tb) {
    width: 768px;
    height: 432px;
  }
  @include breakpoint($lg) {
    width: 1024px;
    height: 576px;
  }
  @include breakpoint($xl) {
    width: 1280px;
    height: 720px;
  }
  // padding-bottom: -56.25%;
  background-color: blue;
}
</style>
