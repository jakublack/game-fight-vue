<template>
  <div class="wrapper--app">
    <div class="wrapper--person">
      <div class="person--player">
        <p>You</p>
        <div class="person--health player--health">{{healthYou}}</div>
      </div>
      <div class="person--player">
        <p>Monster</p>
        <div class="person--health monster--health">{{healthMonster}}</div>
      </div>
    </div>
    <div class="wrapper-action">
      <button class="btn btn-new-game">Start New Game</button>
      <template v-show="startGame">
        <button class="btn btn-atack">Atack</button>
        <button class="btn btn-extra-atack">Extra Atack</button>
        <button class="btn btn-health">Health</button>
        <button class="btn btn-give-up">Give Up</button>

      </template>
    </div>


  </div>

</template>

<script>
export default {
  name: 'Game',
  data:  function() {
    return {
      healthYou : 100,
      healthMonster : 100,
      startGame : false,
    }
  }

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
  color: #fff;
}
.wrapper-action {
  width: calc(80% + 20px);
  height: auto;
  min-height: 80px;
  margin: 10px auto;
  border: 1px solid #ccc;
  box-shadow: 0px 0px 15px 0px rgba(0,0,0,0.3);
  display: flex;
  justify-content: center;
  align-items: center;
}
.btn {
  width: 150px;
  height: 40px;
  border: none;
  cursor: pointer;
  font-size: 14px;
  outline: none;
  color: #fff;
  border-radius: 10px;
  margin: 5px;
}
.btn-new-game {
  background-color: #2A983D;
}
.btn-atack {
  background-color:#FF1919;
}
.btn-extra-atack {
  background-color: #7f0c0c;
}
.btn-health {
  background-color: #00C3FF;
}
.btn-give-up {
  background-color: #F4EEE8;
}




</style>
