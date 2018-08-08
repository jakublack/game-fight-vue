<template>
  <div class="wrapper--app">
    <div class="wrapper--person">
      <div class="person--player">
        <p>You</p>
        <div class="player--health"></div>
      </div>
      <div class="person--player">
        <p>Monster</p>
        <div class="monster--health"></div>
      </div>
    </div>


  </div>

</template>

<script>
export default {
  name: 'Game',

}
</script>

<style lang="sass" scoped>
.wrapper--person {
  text-align: center;
}

.person--player {
  width: 40%;
  display: inline-block;
  margin: auto;
  text-align: center;
}


</style>


