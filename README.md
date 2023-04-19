<!DOCTYPE html>
<html>

<head>
	<title>Funções JavaScript</title>
	<meta charset="UTF-8">
	<link rel="stylesheet" href="style.css" />
<style>
h1 {
    color:rgba(255, 129, 203, 0.76);
    font-size: 28px;
    font-weight: font-family:courier,arial,helvetica;
    margin-bottom: 10px;
}
h2 {
    color: rgba(255, 129, 203, 0.76);
    font-size: 24px;
    font-weight: font-family:courier,arial,helvetica;
    margin-top: 20px;
    margin-bottom: 10px;
}
p {
    font-size: 18px;
    margin-bottom: 10px;
}
label {
    display: block;
    font-size: 18px;
    margin-bottom: 5px;
}
input[type="text"], input[type="number"] {
    font-size: 18px;
    padding: 5px;
    margin-bottom: 10px;
}
button {
    font-size: 18px;
    padding: 5px 10px;
    background-color: rgb(0, 0, 0);
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
button:hover {
    background-color: rgb(0, 0, 0);
}













</style>
	<script>
	// código JavaScript
	</script>



	<script>
		function cubo(numero) {
			return numero * numero * numero;
		}

		function fahrenheitParaCelsius(temperaturaF) {
			return (temperaturaF - 32) * 5 / 9;
		}

		function areaTriangulo(base, altura) {
			return (base * altura) / 2;
		}

		function areaPerimetroCirculo(raio) {
			let area = Math.PI * raio * raio;
			let perimetro = 2 * Math.PI * raio;
			return { area: area, perimetro: perimetro };
		}

		function desconto(valor) {
			return valor * 0.05;
		}

		function verificaMaioridade(anoNascimento) {
			let anoAtual = new Date().getFullYear();
			let idade = anoAtual - anoNascimento;
			if (idade >= 18) {
				return "Maior de idade";
			} else {
				return "Menor de idade";
			}
		}

		function calculaConsumoCombustivel(dinheiro) {
			let precoLitro = 5;
			let litros = dinheiro / precoLitro;
			let kmRodados = litros * 20;
			return { litros: litros, kmRodados: kmRodados };
		}
		function calcularDesconto(valor) {
			var desconto = valor * 0.05;
			return desconto;
		}
		function verificarIdade(ano) {
			var idade = new Date().getFullYear() - ano;
			if (idade >= 18) {
				return 'Você é maior de idade.';
			} else {
				return 'Você é menor de idade.';
			}
		}
		function calcularCombustivel(dinheiro) {
			var litros = dinheiro / 5;
			var km = litros * 20;
			return 'Com R$ ' + dinheiro + ', você pode comprar ' + litros.toFixed(2) + ' litros de combustível e percorrer ' + km.toFixed(2) + ' km.';
		}
	</script>
</head>

<body>
	<h1>Funções JavaScript</h1>
	<h2>1- Cubo de um número</h2>
	<p>Digite um número para calcular o seu cubo:</p>
	<input type="text" id="numeroCubo">
	<button onclick="alert(cubo(document.getElementById('numeroCubo').value))">Calcular</button>

	<h2>2- Conversão de temperatura</h2>
	<p>Digite uma temperatura em graus Fahrenheit para converter em Celsius:</p>
	<input type="text" id="temperaturaF">
	<button onclick="alert(fahrenheitParaCelsius(document.getElementById('temperaturaF').value))">Converter</button>

	<h2>3- Área de um triângulo</h2>
	<p>Digite a base e a altura do triângulo para calcular a sua área:</p>
	<label for="baseTriangulo">Base:</label>
	<input type="text" id="baseTriangulo">
	<label for="alturaTriangulo">Altura:</label>
	<input type="text" id="alturaTriangulo">
	<button
		onclick="alert(areaTriangulo(document.getElementById('baseTriangulo').value, document.getElementById('alturaTriangulo').value))">Calcular</button>

	<h2>4- Área e perímetro de um círculo</h2>
	<p>Digite o raio do círculo para calcular a sua área e perímetro:</p>
	<input type="text" id="raioCirculo">
	<button
		onclick="alert('Área: ' + areaPerimetroCirculo(document.getElementById('raioCirculo').value).area + '\nPerímetro: ' + areaPerimetroCirculo(document.getElementById('raioCirculo').value).perimetro)">Calcular</button>

	<h1>5- Calculadora de Desconto</h1>
	<p>Insira o valor do produto:</p>
	<input type="number" id="valor">
	<button
		onclick="alert('O desconto é de R$ ' + calcularDesconto(document.getElementById('valor').value).toFixed(2))">Calcular</button>

	<h1>6- Verificador de Idade</h1>
	<p>Insira o seu ano de nascimento:</p>
	<input type="number" id="ano">
	<button onclick="alert(verificarIdade(document.getElementById('ano').value))">Verificar</button>

	<h1>7- Calculadora de Combustível</h1>
	<p>Quanto dinheiro você tem?</p>
	<input type="number" id="dinheiro">
	<button onclick="alert(calcularCombustivel(document.getElementById('dinheiro').value))">Calcular</button>
