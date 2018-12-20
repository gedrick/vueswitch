<template>
  <div class="icons">
    <div class="icons__icon">8:12<span>pm</span></div>
    <div class="icons__icon">S</div>
    <div class="icons__icon">BATTERY</div>
  </div>
</template>

<script>
export default {
  name: 'Icons'
};
</script>

<style lang="scss" scoped>
@import './../styles/variables.scss';

.icons {
  margin-right: em(20);
  color: #fff;
  font-family: $base;
  display: flex;

  &__icon {
    font-size: em(12);
    margin-left: em(5);

    span {
      text-transform: uppercase;
      font-size: em(10);
    }
  }
}
</style>
