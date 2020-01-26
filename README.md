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
<input type="button" value="Roll The Dice" onClick="rollDice()" />
<br />

<script type="text/javascript">
var score = 0;
var maxScore = 50;
var rolls = 0;
var maxRolls = 20;


function rollDice()
{
    var x = Math.floor( Math.random() * 6 ) + 1;
    var y = Math.floor( Math.random() * 6 ) + 1;

    if( x == y )
    {
        score = getScore( x );
        alert("You threw a Double " + x + " Your Score is "+ score);
    }
    else
    {
        alert("You threw a " + x + " and a " + y + " Your Score is " + score);
    }

    rolls++;

    if (rolls == maxRolls && score < maxScore)

    {

        alert("Sorry You Lose!");

        score = 0;

        rolls = 0;

        return;

    }

    else if (score >= maxScore)
    {
        alert("Congratulations You Win!");
        score = 0;
        rolls = 0;
        return;
    }
}

function getScore(x)
{
    switch( x )
    {
        case 1:
            score += 5;
            break;
        case 2:
            score += 5;
            break;
        case 3:
            score = 0;
            break;
        case 4:
            score += 5;
            break;
        case 5:
            score += 5;
            break;
        case 6:
            score += 25;
            break;
    }

    return score;
}
</script>
</body>
</html>
