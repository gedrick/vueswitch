<template>
  <div class="switch-screen">
    <div class="switch-screen__inner">
      <ScreenHeader></ScreenHeader>
      <GameList
        :rows="2"
        :games="gamesList">
      </GameList>
    </div>
  </div>
</template>

<script>
import GameList from './GameList.vue';
import ScreenHeader from './ScreenHeader.vue';

export default {
  name: 'SwitchScreen',
  components: {
    GameList,
    ScreenHeader
  },
  data() {
    return {
      gamesList: [
        {
          id: 1,
          title: 'Game 1',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 2,
          title: 'Game 2',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 3,
          title: 'Game 3',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 4,
          title: 'Game 4',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 5,
          title: 'Game 5',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 6,
          title: 'Game 6',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 7,
          title: 'Game 7',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 8,
          title: 'Game 8',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 9,
          title: 'Game 9',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 10,
          title: 'Game 10',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 11,
          title: 'Game 11',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 12,
          title: 'Game 12',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 13,
          title: 'Game 13',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 14,
          title: 'Game 14',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 15,
          title: 'Game 15',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 16,
          title: 'Game 16',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 17,
          title: 'Game 17',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 18,
          title: 'Game 18',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 19,
          title: 'Game 19',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 20,
          title: 'Game 20',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 21,
          title: 'Game 21',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 22,
          title: 'Game 22',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 23,
          title: 'Game 23',
          image: 'https://via.placeholder.com/255'
        },
        {
          id: 24,
          title: 'Game 24',
          image: 'https://via.placeholder.com/255'
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.switch-screen {
  position: absolute;
  background: none;
  width: 70%;
  left: 15%;
  background: black;
  height: 100%;

  &__inner {
    position: absolute;
    background: none;
    width: 90%;
    left: 5%;
    top: 5%;
    background: #c0c0c0;
    height: 90%;

    display: grid;
    grid-template-rows: 15% 85%;
  }
}
</style>
