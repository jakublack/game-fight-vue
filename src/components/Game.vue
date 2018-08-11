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
    <div class="wrapper--action">

      <button v-if="!startGame" class="btn btn-new-game" v-on:click="startNewGame">Start New Game</button>

      <template v-else>
        <button class="btn btn-atack">Attack</button>
        <button class="btn btn-extra-atack">Extra Attack</button>
        <button class="btn btn-health">Health</button>
        <button v-on:click="resetGame" class="btn btn-give-up">Give Up</button>
      </template>

    </div>
    <div v-show="gameEnd" class="wrapper--info">
      <div class="wrapper--info--text">
        <p class="info--title">Game Over</p>
        <p>{{msg}}</p>
        <div v-on:click="closeModal" class="close--element">
        </div>
      </div>
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
      msg: 'Ohhh... no you Give Up... why?',
      gameEnd: false,
    }
  },
  methods: {
    startNewGame: function() {
      this.startGame = !this.startGame;
    },
    resetGame: function() {
      this.startGame = !this.startGame;
      this.gameEnd = !this.gameEnd;
    },
    closeModal : function() {
      this.gameEnd = !this.gameEnd;

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.wrapper--person {
  text-align: center;
}

.wrapper--app {
  position: relative;
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
.wrapper--action {
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
.wrapper--info {
  position: absolute;
  height: 200px;
  width: 300px;
  background-color: #fff;
  box-shadow: 0px 0px 15px 0px rgba(0,0,0,0.3);

  left: 50%;
  transform: translate(-50%,-50%);
}
.wrapper--info--text {
  text-align: center;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  position: relative;
}

.close--element {
  width: 30px;
  height: 30px;
  position: absolute;
  top: 0;
  right: 0;
  cursor: pointer;

}
.close--element::before,
.close--element::after {
  content: "";
  height: 3px;
  background-color: #000;
  width: 100%;
  display: block;
  position: absolute;
  top: 50%;
  border-radius: 10px;
}

.close--element::before{
  transform: rotate(45deg)
}
.close--element::after{
  transform: rotate(-45deg)
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
