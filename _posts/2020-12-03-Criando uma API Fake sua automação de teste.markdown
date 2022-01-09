---
title:  "API Fake pode te ajudar a adiantar sua automação ou desenvolvimento frontend"
date:   2016-01-08 15:04:23
categories: [JsonServer]
tags: [Api]
---

JSON Server é uma biblioteca capaz de criar uma API Fake em segundos e sem precisar escrever nenhuma linha de código.
É uma forma de otimizar o trabalho quando se tem o contrato da API mas o backend ainda não terminou o desenvolvimento
e o front precisa consumir. Também como QA Test já utilizei para adiantar automação de teste enquando a api estava sendo
desenvolvida.
Com o Json Server podemos criar varios bancos no formato Json, simular requisições (GET, POST, PUT e DELETE).Processo é bem simples é preciso ter node previamente instalado.

Instalação Json Server:
``` node
npm install -g json-server
```
Agora crie um arquivo de nome db.json e salve em uma pasta no seu computador.
Nesse exemplo vamos simular API de veiculos e marca.
``` json
{
	"marcas": [{
			"name": "HONDA",
			"fipe_name": "Honda",
			"order": 2,
			"key": "honda-25",
			"id": 25
		},
		{
			"name": "FORD",
			"fipe_name": "Ford",
			"order": 2,
			"key": "ford-22",
			"id": 22
		},
		{
			"name": "CHEVROLET",
			"fipe_name": "GM - Chevrolet",
			"order": 2,
			"key": "gm-chevrolet-23",
			"id": 23
		}
	],
	"veiculo": [{
			"name": "Accord Coupe EX",
			"combustivel": "Gasolina",
			"marca": "Honda",
			"ano_modelo": "1998",
			"preco": "R$ 12.448,00",
			"key": "accord-1998",
			"veiculo": "Accord Coupe EX",
			"id_marca": 25
		},
		{
			"name": "CITY Sedan EXL 1.5 Flex  16V 4p Aut.",
			"combustivel": "Gasolina",
			"marca": "Honda",
			"ano_modelo": "2021",
			"preco": "R$ 87.599,00",
			"key": "city-2021",
			"veiculo": "CITY Sedan EXL 1.5 Flex  16V 4p Aut.",
			"id_marca": 25
		},
		{
			"name": "Fit Twist 1.5 Flex 16V 5p Mec.",
			"combustivel": "Gasolina",
			"marca": "Honda",
			"ano_modelo": "2014",
			"preco": "R$ 41.175,00",
			"key": "fit-2014",
			"veiculo": "Fit Twist 1.5 Flex 16V 5p Mec.",
			"id_marca": 25
		},
		{
			"name": "Focus 1.6 S/1.6 SE Flex 16v 5p Aut",
			"combustivel": "Gasolina",
			"marca": "Ford",
			"ano_modelo": "2016",
			"preco": "R$ 52.866,00",
			"key": "focus-2016",
			"veiculo": "Focus 1.6 S/1.6 SE Flex 16v 5p Aut",
			"id_marca": 22
		},
		{
			"name": "Ka 1.0 S TiVCT Flex 5p",
			"combustivel": "Gasolina",
			"marca": "Ford",
			"ano_modelo": "2021",
			"preco": "R$ 45.177,00",
			"key": "ka-2021",
			"veiculo": "Ka 1.0 S TiVCT Flex 5p",
			"id_marca": 22
			
		},
		{
			"name": "Ka 1.0 S TiVCT Flex 5p",
			"combustivel": "Gasolina",
			"marca": "Ford",
			"ano_modelo": "2018",
			"preco": "R$ 38.225,00",
			"key": "ka-2018",
			"veiculo": "Ka 1.0 S TiVCT Flex 5p",
			"id_marca": 22
		},
		{
			"name": "ONIX HATCH 1.0 12V TB Flex 5p Aut.",
			"combustivel": "Gasolina",
			"marca": "GM - Chevrolet",
			"ano_modelo": "2021",
			"preco": "R$ 60.105,00",
			"key": "onix-2021",
			"veiculo": "ONIX HATCH 1.0 12V TB Flex 5p Aut.",
			"id_marca": 23
		},
		{
			"name": "ONIX HATCH 1.0 12V TB Flex 5p Aut.",
			"combustivel": "Gasolina",
			"marca": "GM - Chevrolet",
			"ano_modelo": "2020",
			"preco": "R$ 58.225,00",
			"key": "onix-2020",
			"veiculo": "ONIX HATCH 1.0 12V TB Flex 5p Aut.",
			"id_marca": 23
		},
		{
			"name": "Celta Life/ LS 1.0 MPFI 8V FlexPower 5p",
			"combustivel": "Gasolina",
			"marca": "GM - Chevrolet",
			"ano_modelo": "2014",
			"preco": "R$ 24.591,00",
			"key": "celta-2014",
			"veiculo": "Celta Life/ LS 1.0 MPFI 8V FlexPower 5p",
			"id_marca": 23
		}

	]
}
```

No prompt de comando Iniciando o servidor usando o comando:
``` node
json-server --watch db.json
```

