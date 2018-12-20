<template>
  <div class="screen">
    <div class="screen__bezel">
      <div class="screen__inside">
        <div class="screen__header">
          <Profiles></Profiles>
          <Icons></Icons>
        </div>
        <div class="screen__content">
          <GamesList></GamesList>
        </div>
        <div class="screen__footer">
          Footer
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import GamesList from '@/components/GamesList.vue';
import Profiles from '@/components/Profiles.vue';
import Icons from '@/components/Icons.vue';

export default {
  components: {
    GamesList,
    Profiles,
    Icons
  }
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';

$bezelSize: 20; // px
.screen {
  width: 100%;
  height: 100%;

  &__bezel {
    padding: em($bezelSize);
    height: calc(100% - (#{$bezelSize}px * 2));
    background-color: #000;
  }

  &__inside {
    background-color: #333333;
    width: 100%;
    height: 100%;
    display: grid;
    flex-direction: column;
    grid-template-rows: 15% 65% 20%;
  }

  &__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__content {
    background-color: red;
  }

  &__footer {
    background-color: yellow;
  }
}
</style>
