<template>
  <div class="wrapper--app">
    <div class="wrapper--person">
      <div class="person--player">
        <p>You</p>
        <div class="person--health player--health"></div>
      </div>
      <div class="person--player">
        <p>Monster</p>
        <div class="person--health monster--health"></div>
      </div>
    </div>


  </div>

</template>

<script>
export default {
  name: 'Game',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scss scoped>

.wrapper--person {
  text-align: center;
}

.person--player {
  width: 40%;
  display: inline-block;
  margin: 10px;
  text-align: center;
  border: 1px solid #ccc;
}

.person--player p {
  font-size: 24px;
}

.person--health {
  width: 90%;
  height: 30px;
  margin: 10px auto;
  background-color: #35BF4D;

}



</style>
