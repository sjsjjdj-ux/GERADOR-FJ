# GERADOR-FJ
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GERADORFJ</title>

<style>
body{
background:#0a0014;
color:#b300ff;
font-family:Consolas,monospace;
display:flex;
align-items:center;
justify-content:center;
height:100vh;
margin:0;
overflow:hidden;
}

.scan{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
pointer-events:none;
background:linear-gradient(
transparent 95%,
rgba(179,0,255,0.15) 100%
);
background-size:100% 4px;
animation:scan 6s linear infinite;
}

@keyframes scan{
0%{background-position:0 0}
100%{background-position:0 100%}
}

.panel{
border:2px solid #b300ff;
padding:40px;
border-radius:15px;
box-shadow:0 0 30px rgba(179,0,255,0.4);
width:340px;
background:#050005;
}

h1{
text-align:center;
margin-top:0;
letter-spacing:2px;
color:#d966ff;
}

.btn{
width:100%;
padding:15px;
background:#b300ff;
border:none;
font-weight:bold;
cursor:pointer;
border-radius:8px;
margin-top:10px;
color:#000;
}

.btn:hover{
opacity:0.85;
}

.result{
margin-top:20px;
display:none;
}

.row{
display:flex;
justify-content:space-between;
margin:8px 0;
}

.status{
text-align:center;
font-size:12px;
margin-top:15px;
color:#d966ff;
}
</style>
</head>

<body>

<div class="scan"></div>

<div class="panel">

<h1>🩵 GERADOR FJ 🩵</h1>

<button class="btn" onclick="gerar()">🎮 GERAR SENSI</button>

<div class="result" id="res">

<div class="row">🔥 DPI <span id="dpi"></span></div>
<div class="row">🎯 GERAL <span id="geral"></span></div>
<div class="row">🔴 RED DOT <span id="red"></span></div>
<div class="row">🔎 MIRA 2X <span id="m2"></span></div>
<div class="row">🎯 MIRA 4X <span id="m4"></span></div>
<div class="row">💥 AWM <span id="awm"></span></div>

<div class="status">
⚡ STATUS: SENSI CALIBRADA ⚡
</div>

</div>
</div>

<script>
function rand(min,max){
return Math.floor(Math.random()*(max-min)+min)
}

function gerar(){
document.getElementById("res").style.display="block"
document.getElementById("dpi").innerText = rand(600,1200)
document.getElementById("geral").innerText = rand(120,200)
document.getElementById("red").innerText = rand(110,180)
document.getElementById("m2").innerText = rand(110,170)
document.getElementById("m4").innerText = rand(100,160)
document.getElementById("awm").innerText = rand(90,150)
}
</script>

</body>
</html>
