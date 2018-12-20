<template>
  <div class="profile">
    <div class="profile__user">
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
  &__user {
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    width: em(30);
    height: em(30);
    background-color: #000;
    color: #fff;
  }

  &__user-letter {
    font-weight: bold;
  }
}
</style>
