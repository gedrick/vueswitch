<template>
  <div class="switch-screen">
    <div class="switch-screen__inner">
      <ScreenHeader
        :gameCount="games.length"
        @expand="doExpand"
        @contract="doContract">
      </ScreenHeader>
      <GameList
        :rows="rows"
        :games="games">
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
  props: ['games'],
  data() {
    return {
      rows: 1
    };
  },
  methods: {
    doExpand() {
      if (this.rows > 1) {
        this.rows--;
      }
    },
    doContract() {
      if (this.rows < 3) {
        this.rows++;
      }
    }
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
