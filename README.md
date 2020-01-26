<html>
<head>
  <title>Igra</title>

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
<img id="die" src="/wp/dice1.jpg" width="50" height="50">
<img id="die" src="/wp/dice2.png" width="50" height="50">
<img id="die" src="/wp/dice3.png" width="50" height="50">
<img id="die" src="/wp/dice4.png" width="50" height="50">
<img id="die" src="/wp/dice5.png" width="50" height="50">
<img id="die" src="/wp/dice6.png" width="50" height="50">  
  
<button onclick="AniDice()">Roll Dice</button>
<button onclick="stopDice()">Stop</button>

<script>

function AniDice()
{
myVar=setInterval(rolldice,20)
}

function rolldice()
{
var ranNum = Math.floor( 1 + Math.random() * 6 );
var dice = document.getElementById("die");
dice.src=ranNum+".jpg";
}
function stopDice()
{clearInterval(myVar);}
</script>

</body>
</html>
