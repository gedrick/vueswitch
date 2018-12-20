<template>
  <div class="home">
    <div class="box">
      <Stage></Stage>
    </div>
  </div>
</template>

<script>
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
  background-image: linear-gradient(-45deg, #0074df, #003f78);
}

.home {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.box {
  width: em(568);
  height: em(320);
  max-height: 80vh;

  @include breakpoint($tb) {
    width: em(768);
    height: em(432);
  }
  @include breakpoint($lg) {
    width: em(1024);
    height: em(576);
  }
  @include breakpoint($xl) {
    width: em(1280);
    height: em(720);
  }
}
</style>
