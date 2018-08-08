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
    <div class="wrapper-action">
      <button class="btn btn-new-game">Start New Game</button>
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
  box-shadow: 0px 0px 15px 0px rgba(0,0,0,0.3);
}

.person--player p {
  font-size: 24px;
}

.person--health {
  width: 90%;
  height: 30px;
  margin: 10px auto;
  background-color: #35BF4D;
  border: 1px solid #000;
}
.wrapper-action {
  width: calc(80% + 20px);
  height: 50px;
  margin: 10px auto;
  border: 1px solid #ccc;
  box-shadow: 0px 0px 15px 0px rgba(0,0,0,0.3);
  display: flex;
  justify-content: center;
  align-items: center;
}
.btn {
  width: 130px;
  height: 30px;
  border: none;

}



</style>
