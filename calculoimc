<!DOCTYPE html>
<html>
<head>
	<title>Calculo de IMC</title>
</head>
<body>
	<h1>Calculo de IMC</h1>
	<form method="post">
		<label>Peso (em kg):</label>
		<input type="text" name="peso"><br><br>
		<label>Altura (em m):</label>
		<input type="text" name="altura"><br><br>
		<input type="submit" name="submit" value="Calcular IMC">
	</form>
	<?php
	if(isset($_POST['submit'])) {
		$peso = $_POST['peso'];
		$altura = $_POST['altura'];
    	$imc = $peso / ($altura * $altura);
	$imc = round($imc, 2); // Arredonda para 2 casas decimais

	echo "<p>Seu IMC é: $imc</p>";

	// Chama a função que você criou para classificar o IMC
	classificaIMC($imc);
}

// Função para classificar o IMC em uma das faixas estabelecidas
function classificaIMC($imc) {
	$faixas = array(
		array("Magreza", 0, 18.5),
		array("Saudável", 18.51, 24.9),
		array("Sobrepeso", 25, 29.9),
		array("Obesidade Grau I", 30, 34.9),
		array("Obesidade Grau II", 35, 39.9),
		array("Obesidade Grau III", 40, 999)
	);

	foreach($faixas as $faixa) {
		if($imc >= $faixa[1] && $imc <= $faixa[2]) {
			$classificacao = $faixa[0];
			break;
		}
	}

	echo "<p>Você está classificado como: $classificacao</p>";
}
?>

</body>
</html>
