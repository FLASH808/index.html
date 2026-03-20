<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Calculadora de Diluição Flash</title>

<style>
body{
  background:#0b0f1a;
  font-family:Arial;
  display:flex;
  justify-content:center;
  align-items:center;
  min-height:100vh;
  margin:0;
}

.box{
  background:#111827;
  padding:20px;
  border-radius:15px;
  color:#fff;
  width:340px;
  text-align:center;
}

.logo{
  width:180px;
  margin-bottom:10px;
}

select, button{
  width:100%;
  padding:10px;
  margin-top:10px;
  border-radius:8px;
  border:none;
}

button{
  background:#00aaff;
  color:#fff;
  font-weight:bold;
}

.result img{
  width:120px;
  margin-top:10px;
  border-radius:10px;
}
</style>
</head>

<body>

<div class="box">

<img src="https://i.imgur.com/I1w5gfd.png" class="logo">

<h2>Calculadora de Diluição Flash</h2>

<select id="produto">
<option value="">Selecione o produto</option>
<option value="ativex">Ativex Pro</option>
<option value="multiex">Multiex</option>
<option value="theking">The King</option>
<option value="ceramic">Ceramic Floc</option>
<option value="protectwax">Protect Wax</option>
</select>

<button onclick="mostrar()">Ver informações</button>

<div id="resultado" class="result"></div>

<a href="https://www.lojaflashprodutos.com/" target="_blank">
<button>Ir para loja</button>
</a>

<a href="https://wa.me/5512996463221" target="_blank">
<button style="background:#25d366">WhatsApp</button>
</a>

</div>

<script>
function mostrar(){
let p = document.getElementById("produto").value;

let dados = {
ativex:{img:"https://i.imgur.com/WAu0167.jpeg",txt:"Leve 1:40 | Pesada 1:20"},
multiex:{img:"https://i.imgur.com/6H8Hqkt.jpeg",txt:"Leve 1:20 | Pesada 1:10"},
theking:{img:"https://i.imgur.com/5U9skat.jpeg",txt:"Leve 1:60 | Média 1:40 | Pesada 1:20"},
ceramic:{img:"https://i.imgur.com/AxVkIp0.jpeg",txt:"Até 1:500"},
protectwax:{img:"https://i.imgur.com/kd4AQPL.png",txt:"Produto pronto uso"}
};

let item = dados[p];

if(!item){
document.getElementById("resultado").innerHTML="";
return;
}

document.getElementById("resultado").innerHTML =
`<img src="${item.img}"><p>${item.txt}</p>`;
}
</script>

</body>
</html>
