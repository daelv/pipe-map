<template>
  <div class='intro-container'>
    <div :id='cardId' class='intro-content'>
      <div class='header-container'>
        <intro-header></intro-header>
      </div>
      <div class='body-container'>
        {{ introText }}
      </div>
      <div class='footer'>
      </div>
    </div>
  </div>
</template>

<script>
import IntroHeader from 'components/IntroHeader.vue'

export default {
  props: {
    cardId: ''
  },

  components: {
    'intro-header': IntroHeader
  },

  data() {
    return {
      introText: 'Scroll down to traverse time. Clicking on accident sites show their Wikipedia descriptions. Radii correspond to gallons spilt (if applicable).'
    }
  }
}
</script>

<style scoped>
.intro-container {
  text-align: center;
  pointer-events: all;
  height: 100vh;
  width: 100%;
  transition: height 999999s;
  background-color: white;
  display: flex;
  align-content: center;
  justify-content: center;
}
.intro-content {
  max-width: 60%;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
}
.body-container {
  width: 90%;
  font-size: 3vh;
  align-self: center;
  margin-bottom: 5%;
  margin-top: 5%;
}
.footer {
  border-bottom: 1px solid black;
}
@media only screen and (max-width: 768px) {
  .body-container {
    font-size: 2em;
    width: 100%;
  }
  .footer {
    border-bottom: 0;
  }
}
</style>
