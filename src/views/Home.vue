<template>
  <div class="box">
    <SwitchContainer></SwitchContainer>
  </div>
</template>

<script>
import SwitchContainer from '@/components/SwitchContainer.vue';

export default {
  components: {
    SwitchContainer
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

.box {
  position: relative;
  display: block;
  margin: auto;
  margin-top: 8%;
  background: none;
  border: none;
  height: 45vw;
  width: 80vw;
}
</style>
