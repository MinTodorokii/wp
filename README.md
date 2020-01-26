<html>
<head>
  <title>Igra</title>
  <meta charset="UTF-8">
        <meta name="viewport content=width=device, initial-scale=1,0">
        <meta http-eyuiv="X-UA-Compatible" content="ie=edge">
        <title>Document</title>
<style>
.container {
  width: 70%;
  margin: auto;
  text-align: center;
}

.dice {
  text-align: center;
  display: inline-block;

}

body {
  background-color: #7e697e;
}

h1 {
  margin: 30px;
  font-family: 'Britannic Bold', cursive;
  text-shadow: 3px 0 #232931;
  font-size: 8rem;
  color: #fbe1f8;
  text-align: center;
}

p {
  font-size: 2rem;
  color: #fbe1f8;
  font-family: 'Britannic Bold', cursive;
}

img {
  width: 80%;
}

footer {
  margin-top: 5%;
  color: #fbe1f8;
  text-align: center;
  font-family: 'Britannic Bold', cursive;

}
</style>
</head>
<body>
 function rollSingleDice()
{
    return Math.floor(Math.random()*6+1);
}

//Make the rollDice function roll dice,
//check for doubles, and return the
//total score achieved by all rolls
function rollDice(player) {
var score = 0;
var roll1; var roll2;
var playerScore;
    do {
        roll1 = rollSingleDice();
        roll2 = rollSingleDice();
        score = roll1 + roll2;
        player.addToScore(score);
        playerScore = player.getScore();
        console.log("Roll 1: " + roll1 + " Roll 2: " + roll2 + " Total Score: " + playerScore);
       
        if (roll1 == roll2) {
            if (roll1 === 1) {
                console.log("Snake Eyes!");
                return true;
            } else {
                console.log("Congrats! Double Thrown!");
            }
        }
    } while (roll1 === roll2);
    return false;
}


function Player(name) {
  this.name = name;
  var score = 0; // this is a private attribute
  this.addToScore = function(points) {
    score = score + points;
  };
  this.getScore = function() {
    return score;
  };
}

var player1 = new Player("Bobby");
var snakeEyes = false;
while(snakeEyes === false) {
    snakeEyes = rollDice(player1);
} 
 
</body>
</html>
