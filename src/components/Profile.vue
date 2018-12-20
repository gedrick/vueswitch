<template>
  <div class="profile">
    <div class="profile__icon">
      <div class="profile__user-letter">{{name.substring(0, 1)}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Profile',
  props: ['name']
};
</script>

<style lang="scss" scoped>
@import './../styles/variables.scss';

.profile {
  &__icon {
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    width: em(30);
    height: em(30);
    background-color: #fff;
    color: #000;
    border: 2px solid #000;
    margin-right: em(5);
  }

  &__user-letter {
    font-weight: bold;
  }
}
</style>
