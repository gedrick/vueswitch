<template>
  <div class="switch-screen">
    <div class="switch-screen__inner">
      <div class="switch-screen__header">
        Header!
      </div>
      <GameList :games="gamesList"></GameList>
      <div class="switch-screen__footer">
        Footer!
      </div>
    </div>
  </div>
</template>

<script>
import GameList from './GameList.vue';

export default {
  name: 'SwitchScreen',
  components: {
    GameList
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
    grid-template-rows: 15% 65% 20%;
  }

  &__header {
    background-color: red;
  }

  &__footer {
    background-color: white;
  }
}
</style>
