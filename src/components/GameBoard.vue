<template>
  <div class="game-board triangle">
    <div class="top-row">
      <game-icon icon="paper"/>
      <game-icon icon="scissors"/>
    </div>
    <div class="bottom-row">
      <game-icon icon="rock"/>
    </div>
  </div>
</template>

<script>
import GameIcon from './GameIcon.vue';

export default {
  name: 'GameBoard',
  props: {
    msg: String,
  },
  components: {
    GameIcon,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.game-board {
  display: flex;
  flex-direction: column;
  width: 50%;
  padding: 0 1.6rem 0 1.6rem;
}
.triangle {
  background: url('~@/assets/images/bg-triangle.svg') no-repeat;
  background-size: 15rem;
  background-position: center;
}
.top-row {
  display: flex;
  justify-content: space-around;
  margin-bottom: 1rem;
}
.bottom-row {
  display: flex;
  justify-content: center;
}

@media screen and (max-width: $screen-max-width) {
.game-board {
  padding: 0;
  width: 100%;
}}

</style>
