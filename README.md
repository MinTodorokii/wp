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
  
 <h1>Klikni ovdje!</h1> 
<script> 
function rollDice(){
  var die1 = document.getElementById("die1");
  var die2 = document.getElementById("die2");
  var status = document.getElementById("status");
  var d1 = Math.floor(Math.random() * 6) + 1;
  var d2 = Math.floor(Math.random() * 6) + 1;
  die1.innerHTML = d1;
  die2.innerHTML = d2;
  status.innerHTML = "Dobili ste"
  if(d1 == d2){
       status.innerHTML +="neriješeno!!"
  }
  }
</script>
</body>
</html>
