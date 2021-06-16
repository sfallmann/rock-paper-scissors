<template>
  <div class="game-icon">
    <div class="game-icon__outer-circle" :class="`${icon}__outer-circle`">
      <div class="game-icon__inner-circle">
        <img :src="imgSrc" class="game-icon__icon"/>
      </div>
    </div>
  </div>
</template>

<script>
import Rock from '../assets/images/icon-rock.svg';
import Paper from '../assets/images/icon-paper.svg';
import Scissors from '../assets/images/icon-scissors.svg';

export default {
  name: 'GameIcon',
  props: {
    icon: {
      type: String,
      required: true,
    },
  },
  computed: {
    imgSrc() {
      if (this.icon === 'rock') return Rock;
      if (this.icon === 'paper') return Paper;
      if (this.icon === 'scissors') return Scissors;
      return null;
    },
  },
};
</script>

<style scoped lang="scss">
.game-icon__outer-circle {
  position: relative;
  border-radius: 50%;
  width: 10rem;
  height: 10rem;
  box-shadow: inset -2px -.6rem 3px -2px  rgba(0,0,0,0.2)
  //   box-shadow: inset -2px -15px 3px -2px  rgba(0,0,0,0.2)
}
.game-icon__inner-circle {
  @include center;
  border-radius: 50%;
  background-color: white;
  width: 7rem;
  height: 7rem;
  box-shadow: inset 2px .8rem 1px -4px  rgba(200,200,200,0.9);
  // box-shadow: inset 2px 16px 1px -4px  rgba(200,200,200,0.9);
}

.game-icon__icon {
  @include center;
  width: 3rem;
}

.rock__outer-circle {
   background-image: radial-gradient(hsl(349, 71%, 52%) 4%, hsl(349, 70%, 56%));
}

.paper__outer-circle {
  // background-color: $rock-gradient;
   background-image: radial-gradient(hsl(230, 89%, 62%) 4%, hsl(230, 89%, 65%));
}

.scissors__outer-circle {
  // background-color: $rock-gradient;
   background-image: radial-gradient(hsl(39, 89%, 49%) 4%, hsl(40, 84%, 53%));
}

</style>
