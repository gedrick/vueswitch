<template>
  <div class="screen">
    <div class="screen__bezel">
      <div class="screen__inside">
        <div class="screen__header">
          <Profiles></Profiles>
          <Icons></Icons>
        </div>
        <div class="screen__content">
          <GamesList
            :games="games">
          </GamesList>
        </div>
        <div class="screen__footer">
          Footer
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Profiles from '@/components/Profiles.vue';
import Icons from '@/components/Icons.vue';
import GamesList from '@/components/GamesList.vue';

export default {
  components: {
    Profiles,
    Icons,
    GamesList
  },
  data() {
    return {
      games: [
        {
          id: 1,
          name: 'Legend of Zelda: Breath of the Wild',
          image: 'http://via.placeholder.com/255'
        },
        {
          id: 2,
          name: 'Snipperclips',
          image: 'http://via.placeholder.com/255'
        },
        {
          id: 3,
          name: 'Super Mario Odyssey',
          image: 'http://via.placeholder.com/255'
        },
        {
          id: 4,
          name: 'PicrossS',
          image: 'http://via.placeholder.com/255'
        },
        {
          id: 5,
          name: 'Pokemon: Lets Go Pikachu!',
          image: 'http://via.placeholder.com/255'
        },
        {
          id: 6,
          name: 'IMPLOSION',
          image: 'http://via.placeholder.com/255'
        }
      ]
    };
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
    border-radius: em(5);
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

  $padding: 20;
  &__content {
    display: flex;
    padding: em($padding) 0;
    height: calc(100% - (#{$padding}px * 2));
  }

  &__footer {
    background-color: yellow;
  }
}
</style>
