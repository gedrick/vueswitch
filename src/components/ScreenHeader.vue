<template>
  <div class="screen-header">
    <div class="screen-header__expand" @click="expand"></div>
    <div class="screen-header__contract" @click="contract">
      <div class="screen-header__contract-square">&nbsp;</div>
      <div class="screen-header__contract-square">&nbsp;</div>
      <div class="screen-header__contract-square">&nbsp;</div>
      <div class="screen-header__contract-square">&nbsp;</div>
    </div>
    Header!
  </div>
</template>

<script>
export default {
  name: 'ScreenHeader',
  methods: {
    expand() {
      this.$emit('expand');
    },
    contract() {
      this.$emit('contract');
    }
  }
};
</script>


<style lang="scss" scoped>
@import '../styles/variables.scss';

.screen-header {
  @include alignCenter;
  padding: em(10);
  justify-content: flex-start;
  background-color: green;
  color: white;

  &__expand {
    cursor: pointer;
    background-color: #fff;
    width: em(16);
    height: em(16);
    border: em(1) solid rgba(#000000, 0.8);
  }

  &__contract {
    cursor: pointer;
    display: grid;
    grid-row: 50% 50%;
    grid-column: 50% 50%;
    grid-template-rows: 50% 50%;
    grid-template-columns: 50% 50%;

    &-square {
      width: em(7);
      height: em(7);
      background-color: #fff;
      border: em(1) solid rgba(#000000, 0.8);
    }
  }
}
</style>
