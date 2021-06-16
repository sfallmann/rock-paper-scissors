<template>
  <div id="app">
    <score-board />
    <game-board />
  </div>
</template>

<script>
import GameBoard from './components/GameBoard.vue';
import ScoreBoard from './components/ScoreBoard.vue';

export default {
  name: 'App',
  components: {
    GameBoard,
    ScoreBoard,
  },
};
</script>

<style lang="scss">
#app {
  max-width: 1366px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 100%;
  padding-top: 40px;
}
</style>
