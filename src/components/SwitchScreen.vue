<template>
  <div class="switch-screen">
    <div class="switch-screen__inner">
      <ScreenHeader></ScreenHeader>
      <GameList :games="gamesList"></GameList>
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
        }
        // {
        //   id: 3,
        //   title: 'Game 3',
        //   image: 'https://via.placeholder.com/255'
        // },
        // {
        //   id: 4,
        //   title: 'Game 4',
        //   image: 'https://via.placeholder.com/255'
        // }
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
