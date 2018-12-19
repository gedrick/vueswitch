<template>
  <div class="stage">
    <!-- <JoyCon
      side="left">
    </JoyCon> -->
    <Screen></Screen>
    <!-- <JoyCon
      side="right">
    </JoyCon> -->
  </div>
</template>

<script>
// import JoyCon from '@/components/JoyCon.vue';
import Screen from '@/components/Screen.vue';

export default {
  components: {
    // JoyCon,
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
