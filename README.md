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
   <script>
    function generator (){
      var x = Math.floor((Math.random()*6)+1);
       console.log(x);
        document.GetElementById('divImage').innerHTML ='
  <img src="img/dice${x}.png" style="width:300px;">
  '
  }
</script>
  
  <h1>Press here</h1x>
</body>
</html>
