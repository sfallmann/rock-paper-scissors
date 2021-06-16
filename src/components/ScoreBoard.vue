<template>
  <div class="score-board">
    <img :src="imgSrc" class="score-board__logo" />
  </div>
</template>

<script>
import Logo from '../assets/images/logo.svg';

export default {
  name: 'ScoreBoard',

  computed: {
    imgSrc() {
      return Logo;
    },
  },
};
</script>

<style scoped lang="scss">
.score-board {
  min-width: 20rem;
  width: 50%;
  padding: 15px;
  border-radius: 10px;
  border: 3px solid $header-outline;
  margin-bottom: 80px;
}
.score-board__logo {
  width: 80px;
}

@media screen and (max-width: $screen-max-width) {
  .score-board  {
    width: 80%;
  }
}
</style>
