<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Relógio Digital</title>
  <link rel="stylesheet" href="clock.css">
  <style>
    * {
    margin: 0;
    padding: 0;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
}
h1 {
    color: white;
    margin-top: 45%;
}
body {
    height: 100vh;
    background: linear-gradient(white, blue);
    display: flex;
    align-items: center;
    justify-content: center;
}
.relogio {
    display: flex;
    align-items: center;
    justify-content: space-around;
    height: 200px;
    width: 500px;
    background: transparent;
    border-radius: 5px;
    box-shadow: 0px 8px 10px rgba(0, 0, 0, .3);
}
.relogio div {
    height: 170px;
    width: 150px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: antiquewhite;
    background: rgba(6, 6, 0, .10);
    box-shadow: 7px;
    border-radius: 8px;
    letter-spacing: 4px;
}
.relogio span{
    font-weight: bolder;
    font-size: 55px;
}
.relogio span.tempo{
font-size: 15px;
}
  </style>
</head>
<body>
    <h1>Relógio Digital</h1>
  <div class="relogio">
    <div>
  <span id="horas">00</span>
  <span class="tempo">Horas</span>
  </div>
  <div>
    <span id="minutos">00</span>
    <span class="tempo">Minutos</span>
    </div>
    <div>
     <span id="segundos">00</span>
     <span class="tempo">Segundos</span>
 </div>
  
  </div>
  
  <script>
    const horas = document.getElementById("horas");
const minutos = document.getElementById("minutos");
const segundos = document.getElementById("segundos");

const relogio = setInterval (function time() {
    let dateToday = new Date();
    let hr = dateToday.getHours();
    let minu = dateToday.getMinutes();
    let seg = dateToday.getSeconds();
  
    horas.textContent = hr;
    minutos.textContent = minu;
    segundos.textContent = seg;
  
    if (hr < 10) hr = '0' + hr;
    if (minu < 10) minu = '0' + minu;
    if (seg < 10) seg = '0' + seg:
})
  </script>
</body>
</html>
