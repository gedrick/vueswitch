<template>
  <div class="stage">
    <Screen></Screen>
  </div>
</template>

<script>
import Screen from '@/components/Screen.vue';

export default {
  components: {
    Screen
  }
};
</script>

<style lang="scss" scoped>
.stage {
  font-size: 16px;
  margin: auto;
  width: 100%;
  height: 100%;
  align-self: center;
  background-color: rgba(red, 0.4);
}
</style>
