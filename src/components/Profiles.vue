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
        },
        {
          id: 2,
          name: 'Bob'
        },
        {
          id: 3,
          name: 'Luca'
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
}
</style>
