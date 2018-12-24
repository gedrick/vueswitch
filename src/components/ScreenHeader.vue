<template>
  <div class="screen-header">
    <div class="screen-header__sizing">
      <div class="screen-header__expand" @click="expand"></div>
      <div class="screen-header__contract" @click="contract">
        <div class="screen-header__contract-square"></div>
        <div class="screen-header__contract-square"></div>
        <div class="screen-header__contract-square"></div>
        <div class="screen-header__contract-square"></div>
      </div>
    </div>
    <div class="screen-header__username">
      <h2>Gedrick</h2>
    </div>
    <div class="screen-header__count">
      <span v-if="gameCount">{{gameCount}} game<span v-if="gameCount > 1">s</span></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ScreenHeader',
  props: ['gameCount'],
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
  display: grid;
  grid-template-columns: 20% calc(60% - 20px) 20%;
  height: 100%;
  padding: 0 em(10);
  justify-content: space-between;
  background-color: $switch-bg-color;
  color: white;

  @include breakpoint($mobile) {
    padding: 0 em(3);
  }

  &__sizing {
    display: flex;
    align-self: center;
  }

  &__username {
    align-self: center;

    h2 {
      font-weight: bold;
      font-size: em(16);

      @include breakpoint($mobile) {
        font-size: em(12);
      }
    }
  }

  &__count {
    align-self: center;
    color: white;
    & > span {
      font-size: em(14);
    }
  }

  &__expand {
    cursor: pointer;
    background-color: #fff;
    width: em(16);
    height: em(16);
    border: em(1) solid rgba(#000000, 0.8);
  }

  &__contract {
    cursor: pointer;
    margin-left: em(5);
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
