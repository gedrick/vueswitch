<template>
  <div class="controller-buttons">
    <div class="controller-buttons__interior">
      <div class="controller-buttons__buttons">
        <ControllerButton label="A"></ControllerButton>
      </div>
    </div>
  </div>
</template>

<script>
import ControllerButton from '@/components/ControllerButton.vue';

export default {
  name: 'ControllerButtons',
  components: {
    ControllerButton
  }
};
</script>

<style lang="scss" scoped>
.controller-buttons {
  width: 1em;
  height: 1em;
  border-radius: 100%;
  background-color: #202226;
  &__interior {
    span {
      color: #fff;
      font-size: 10px;
    }
  }
}
</style>

