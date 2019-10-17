# Rocketseat - Starter JavaScript 

## Atualização: 17 de Outubro de 2019 - 15:33
## Criação: 14 de Outubro de 2019
## Prática : @douglasabnovato

## Ferramentas : 

![Git](/images/logo-git.png)
![Github](/images/logo-github.png)
![Javascript](/images/logo-javascript.png)
![VSCode](/images/logo-VSCode.png)
![Rocketseat](/images/logo-rocketseat.png)

### Introdução à Javascript 

#### 1. Introdução 
- interpretar scripts na interface do navegador no ambiente do cliente.
- comunidade javascript.

#### 2. Configuração Ambiente 
- Visual Studio Code
- Console de Desenvolvedor - Google Chrome

#### 3. Variáveis e Dados
- string, inteiro, decimal, boolean, vetor, objeto
- console.log
````
	var nome = "douglas";//string
	var idade = 29;//inteiro
	var peso = 80.5;//decimal
	var humano = true;//boolean
	var alunos = ['douglasabn', 'Roberto', 'Lucas'];//vetor
	var aluno = {//objeto
	    nome: 'douglasabnovato',
	    idade: 29,
	    peso: 84.5,
	    humano: true
	};
	console.log(alunos[1]);
	console.log(aluno.peso);
````

#### 4. Operações Matemáticas

````
	var x = 9, y = 3;
	console.log(x + y);
````

#### 5. Funções
````
	function soma(numero1, numero2){
	    var resultado = numero1 + numero2;
	    return resultado;
	}
	var resultadosoma = soma(1, 2);
	console.log(resultadosoma);
````

#### 6. Condicionais
- if
````
	function qualSexo(sexo){//M ou F
	    if(sexo == 'M'){
	        return 'Masculino';
	    } else if( sexo == 'F') {
	        return 'Feminino'; 
	    } else {
	        return 'Outro';
	    }
	}
	var resultadoSexo = qualSexo('M');
	console.log(resultadoSexo);
````

- switch case
````
	function qualSexo(sexo){//M ou F
	    switch (sexo) {
	        case 'M':
	            return 'Masculino';
	        case 'F':
	            return 'Feminino';
	        default:
	            return 'Outro';
	    }
	}
	var resultadoSexo = qualSexo('F');
	console.log(resultadoSexo);
````

#### 7. Operadores Lógicos
- and
````         
	var sexo = 'M', idade = 23;
	if(sexo === 'M' && idade >=18){
	    console.log('OK');
	}
````
- or
````         
	var sexo = 'M', idade = 15;
	if(sexo === 'M' || idade >=18){
	    console.log('OK');
	}
````
- not : verificar a desigualdade
````         
	var sexo = 'F';
	if(sexo !== 'M'){
	    console.log('OK');
	}
````

#### 8. Condicional Ternária
- estrutura tradicional if else
````
	var sexo = 'M';
	if (sexo === 'M'){
	    return 'Masculino';
	} else {
	    return 'Feminino';
	}
````
- estrutura ternária
````
	var sexo = 'F';
	var retorno = (sexo === 'M') ? 'Masculino' : 'Feminino';
	console.log(retorno);
````

#### 9. Estruturas de Repetição
- for : exibir no console de 0 a 99 
````
	for (var i = 0; i < 100; i++){
	    console.log(i);
	}
````
- while - quando não há conhecimento de quantas interações serão realizadas
````
	var j = 0;
	while (j<100){
	    console.log(j);
	    j++;
	}
````

#### 10. Intervalo e Timeout
- Intervalo : executa repetidas vezes no intervalo de tempo informado como parâmetro
````
	function exibirAlgo(){
	    console.log('@douglasabnovato');
	}
	setInterval(exibirAlgo, 1000);
````
- Timeout : executa uma vez após o intervalo de tempo informado como parâmetro
````	
	function exibirAlgo(){
		console.log('@douglasabnovato');
	}
	setTimeout(exibirAlgo, 6000);
````

#### Desafio
- arquivo pdf : desafio1-introducao.pdf
- consultas :
1. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf
2. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for...of
3. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/join
- tarefa 1
````
	<script>  
		var endereco = {
		    rua: "Rua dos pinheiros",
		    numero: 1293,
		    bairro: "Centro",
		    cidade: "São Paulo",
		    uf: "SP"
		};
		function montarEndereco(){

		    return 'O usuário mora em ' + endereco.cidade + '/' + endereco.uf 
		            + ', no bairro ' + endereco.bairro + ', na rua ' + endereco.rua 
		            + ' com nº ' + endereco.numero + '.'
		}

		console.log(montarEndereco());

	</script>
````
- tarefa 2
````
	function exibirPares(x, y){
		for(var i = x; i <= y; i++){
		    if(i%2 === 0){
		        console.log(i);
		    } 
		}
	}
	console.log(exibirPares(32,321));
````
- tarefa 3
````
	function temHabilidade(skills, possuiEssaSkill){
	    return skills.indexOf(possuiEssaSkill);
	}

	var skills = [ "Html", "Javascript", "ReactJS", "React  Native"];
	var possuiEssaSkill = "Javascript";

	if(temHabilidade(skills, possuiEssaSkill) != -1){
	    console.log('Possui a habilidade ' + possuiEssaSkill + '.');
	} else {
	    console.log('Não Possui a habilidade ' + possuiEssaSkill + '.');
	}
````
- tarefa 4 
````
	function experiencia(anos) {
	    if(anos > 0 && anos <= 1 ){
	        return anos + ' anos de estudo. Você é um programador Iniciante';
	    }
	    if(anos > 1 && anos <= 3 ){
	        return anos + ' anos de estudo. Você é um programador Intermediário';
	    }
	    if(anos > 3 && anos <= 6 ){
	        return anos + ' anos de estudo. Você é um programador Avançado';
	    }
	    if(anos > 6 ){
	        return anos + ' anos de estudo. Você é um programador Jedi Master';
	    }
	    else {
	        return ' Você quer ser programador ?';
	    }
	}
	var anosEstudo = 5;
	console.log(experiencia(anosEstudo));
````

- tarefa 5
````
	var usuarios = [
		{
		    nome: "Diego",
		    habilidades: ["Javascript", "ReactJS", "Redux"]
		},
		{
		    nome: "Gabriel",
		    habilidades: ["VueJS", "Ruby on Rails", "Elixir"]
		}
	];

	function leitura(usuarios){
		for(let usuario of usuarios){
		    console.log('O '+ usuario.nome +' possui as habilidades ' + usuario.habilidades + '.');
		}
	}

	leitura(usuarios);
````
### Manipulando a DOM

#### 1. Eventos inline 
- eventos : onclick, onmouseover, entre outros.
````
	<body>
		<h4> @douglasabnovato </h4>
		<h5> Manipulando DOM</h5>
		<div id="app">
			<button onmouseover ="mostraAlerta()">Pressione</button>
		</div>
		<script>
			function mostraAlerta(){
				alert('Botão foi clicado.');
			}
		</script>
	</body>
````

#### 2. Trabalhando com a DOM 
- objetivo é buscar as informações nos elementos da DOM
- getElementsByTagName
- getElementsByClassName
- getElementsById 
- manipulando elementos da nossa DOM
````
	<div id="app">
		<input type="text" name="nome"/>
		<button class="botao">Adicionar</button>
	</div>
	<script>
		var btnElement = document.querySelector('button.botao');
		var inputElement = document.querySelector('input[name=nome');
		btnElement.onclick = function(){
			var text = inputElement.value;
			alert(text);
		}
	</script>
````
- criando e removendo
````
	<div id="app">
		<input id="nome"/>
	</div>
	<script>
		var linkElement = document.createElement('a');
		linkElement.setAttribute('href','http://rocketseat.com.br');

		var textElement = document.createTextNode('Acessar site da rocketseat.');
		linkElement.appendChild(textElement);

		var containerElement = document.querySelector('#app');
		containerElement.appendChild(linkElement);

		var inputElement = document.querySelector('#nome');
		containerElement.removeChild(inputElement);

	</script>
````

#### 3. Alterando Estilos 
- controlar estilização css
````
	<div id="app">
		<div class="box"></div>
	</div>
	<script>
		var boxElement = document.querySelector('.box');

		boxElement.style.width = 100;
		boxElement.style.height = 100;
		boxElement.style.backgroundColor = '#f00';            
	</script>
```` 

#### Desafio
- arquivo pdf : desafio2-manipulandoDOM.pdf 
- tarefa 1
````
	<button class='botao' id='btnCriar' onClick="gerarQuadrado()">Gerar novo</button>
	<div id="app">
		<div class="box"></div>
	</div>
	<script>        
		function gerarQuadrado() {

			let boxElement = document.createElement("div");

			boxElement.style.width = '100px';
			boxElement.style.height = '100px';
			boxElement.style.margin = '10px';
			boxElement.style.backgroundColor = '#f00';

			//adiciona a classe .box na div criada
			boxElement.classList.add('box');

			document.body.appendChild(boxElement);
		}
	</script>
````
- tarefa 2
````
	<button class='botao' id='btnCriar' onClick="gerarQuadrado()" >Gerar novo</button>
	<div id="app">
		<div class="box" onmouseover="trocarCor(this)"></div>
	</div>
	<script>        

		function gerarQuadrado() {

			let boxElement = document.createElement("div");

			boxElement.style.width = '100px';
			boxElement.style.height = '100px';
			boxElement.style.margin = '10px';
			boxElement.style.backgroundColor = '#f00';

			//cria evento mouseover
			boxElement.addEventListener("mouseover", () => {
				let newColor = getRandomColor();
				boxElement.style.backgroundColor = newColor;
			});

			//adiciona a classe .box na div criada
			boxElement.classList.add('box');

			document.body.appendChild(boxElement);
		}

		function getRandomColor() {
			var letters = "0123456789ABCDEF";
			var color = "#";
			for (var i = 0; i < 6; i++) {
				color += letters[Math.floor(Math.random() * 16)];
			}
			return color;
		}
		
	</script>
````

:. De Rocketseat - Starter - Javascript.<br>
Por Diego Fernandes : https://skylab.rocketseat.com.br/node/curso-java-script/group/introducao-java-script/lesson/configurando-ambiente-3