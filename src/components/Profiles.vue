<template>
  <div class="profiles">
    <Profile
      v-for="profile in profiles"
      :name="profile.name"
      v-bind:key="profile.id">
    </Profile>
  </div>
</template>

<script>
import Profile from '@/components/Profile.vue';

export default {
  name: 'Profiles',
  components: {
    Profile
  },
  data() {
    return {
      profiles: [
        {
          id: 1,
          name: 'Geddy'
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import './../styles/variables.scss';

.profiles {
  margin-left: em(20);
  display: flex;

  &__user {
    border-radius: 100%;
    width: em(30);
    height: em(30);
    background-color: #000;
    margin-left: em(5);
  }
}
</style>
