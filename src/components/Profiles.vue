<template>
  <div class="profiles">
    <div class="profiles__user-image">&nbsp;</div>
  </div>
</template>

<style lang="scss" scoped>
@import './../styles/variables.scss';

.profiles {
  margin: em(10);

  &__user-image {
    border-radius: 100%;
    width: em(30);
    height: em(30);
    background-color: #000;
  }
}
</style>
