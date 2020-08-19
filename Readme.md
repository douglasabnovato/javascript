# Rocketseat - Starter JavaScript 

### Atualização: 19 de agosto de 2020 - Done
### Criação: 14 de Outubro de 2019
### Prática : @douglasabnovato

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
````javascript
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

````javascript
	var x = 9, y = 3;
	console.log(x + y);
````

#### 5. Funções
````javascript
	function soma(numero1, numero2){
	    var resultado = numero1 + numero2;
	    return resultado;
	}
	var resultadosoma = soma(1, 2);
	console.log(resultadosoma);
````

#### 6. Condicionais
- if
````javascript
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
````javascript
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
````javascript        
	var sexo = 'M', idade = 23;
	if(sexo === 'M' && idade >=18){
	    console.log('OK');
	}
````
- or
````javascript       
	var sexo = 'M', idade = 15;
	if(sexo === 'M' || idade >=18){
	    console.log('OK');
	}
````
- not : verificar a desigualdade
```` javascript       
	var sexo = 'F';
	if(sexo !== 'M'){
	    console.log('OK');
	}
````

#### 8. Condicional Ternária
- estrutura tradicional if else
````javascript
	var sexo = 'M';
	if (sexo === 'M'){
	    return 'Masculino';
	} else {
	    return 'Feminino';
	}
````
- estrutura ternária
````javascript
	var sexo = 'F';
	var retorno = (sexo === 'M') ? 'Masculino' : 'Feminino';
	console.log(retorno);
````

#### 9. Estruturas de Repetição
- for : exibir no console de 0 a 99 
````javascript
	for (var i = 0; i < 100; i++){
	    console.log(i);
	}
````
- while - quando não há conhecimento de quantas interações serão realizadas
````javascript
	var j = 0;
	while (j<100){
	    console.log(j);
	    j++;
	}
````

#### 10. Intervalo e Timeout
- Intervalo : executa repetidas vezes no intervalo de tempo informado como parâmetro
````javascript
	function exibirAlgo(){
	    console.log('@douglasabnovato');
	}
	setInterval(exibirAlgo, 1000);
````
- Timeout : executa uma vez após o intervalo de tempo informado como parâmetro
````javascript	
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
````javascript
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
````javascript
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
````javascript
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
````javascript
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
````javascript
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

#### 11. Eventos inline 
- eventos : onclick, onmouseover, onkeypress, entre outros.
````html
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

#### 12. Trabalhando com a DOM 
- objetivo é buscar as informações nos elementos da DOM
- getElementsByTagName
- getElementsByClassName
- getElementsById 
- manipulando elementos da nossa DOM
````html
	<div id="app">
		<input type="text" name="nome"/>
		<button class="botao">Adicionar</button>
	</div>
	<script>
		var btnElement = document.querySelector('button.botao');
		var inputElement = document.querySelector('input[name=nome]');
		btnElement.onclick = function(){
			var text = inputElement.value;
			alert(text);
		}
	</script>
````
- criando e removendo
````html
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
#### 13. Lidando com elementos
- criando elementos HTML com JS.
````html
<body>
	<div id = "app">

	</div>
	<script>
		var linkElement = document.createElement('a');//criando a tag <a>
		linkElement.setAttribute('href', 'http://rocketseat.com.br');
		var textElement = document.createTextNode('Acessar site da Rocketseat.');
		linkElement.appendChild(textElement);
		var containerElement = document.querySelector('#app');
		containerElement.appendChild(linkElement);
	</script>
</body>
````
#### 14. Alterando Estilos 
- controlar estilização css
````html
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
````html
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
````html
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
- tarefa 3 
````html
	<script>
		var nomes = ["Diego", "Lucas", "Gabriel", "Lucas"];

		var element = document.body;

		var newUl = document.createElement('ul');
		
		for(var i = 0 ; i < nomes.length ; i++){
			var newLi = document.createElement('li');
			var itemLi = document.createTextNode(nomes[i]);
			newLi.appendChild(itemLi);
			newUl.appendChild(newLi);
			element.appendChild(newUl); 
		}
	</script>
````
- tarefa 4
````html
	<input type="text" name="nome">
	<button class="botao" onClick="adicionar()">Adicionar</button>
	<script>
		var nomes = ["Diego", "Lucas", "Gabriel", "Lucas"];
		var element = document.body;
		var newUl = document.createElement('ul');
		for(var i = 0 ; i < nomes.length ; i++){
			var newLi = document.createElement('li');
			var itemLi = document.createTextNode(nomes[i]);
			newLi.appendChild(itemLi);
			newUl.appendChild(newLi);
			element.appendChild(newUl); 
		}
		function adicionar(){
			var inputElement = document.querySelector('input[name=nome]');
			var newLi = document.createElement('li');
			var itemLi = document.createTextNode(inputElement.value);
			newLi.appendChild(itemLi);
			newUl.appendChild(newLi);
			element.appendChild(newUl); 
		}
	</script>
````

### App de Todos

#### 15. Estrutura do App
- `index.html`
- `todos.js`
- referenciar os elementos html no javascript

#### 16. Iniciando aplicação
- array de todos

#### 17. Renderizando Todos
- renderizar via javascript

#### 18. Criando Todos
- criando via javascript

#### 19. Excluindo Todos
- excluindo via javascript

#### 20. Salvando no Storage
- storage via javascript

**projeto AppTodos**
- `index.html`
````html
<html>
    <head>
        <title>Javascript-@douglasabnovato</title>
    </head>
    <body>
        <div id="app">
            <ul></ul>
            <input type="text" placeholder="Digite um todo">
            <button>Adicionar</button>
        </div>
        <script src="todos.js"></script>
    </body>
</html>
````
- `todos.js`
````javascript
var listElement = document.querySelector('#app ul');
var inputElement = document.querySelector('#app input');
var buttonElement = document.querySelector('#app button');

var todos = JSON.parse(localStorage.getItem('list_todos')) || [];

function renderTodos(){

    listElement.innerHTML = '';

    for (todo of todos ){

        var todoElement = document.createElement('li');
        var todoText = document.createTextNode(todo);

        var linkElement = document.createElement('a');
        linkElement.setAttribute('href', '#');
        var pos = todos.indexOf(todo);
        linkElement.setAttribute('onclick','deleteTodo('+ pos +')');
        var linkText = document.createTextNode('Excluir');

        linkElement.appendChild(linkText);
        todoElement.appendChild(todoText);
        todoElement.appendChild(linkElement);
        listElement.appendChild(todoElement);

    }
}

renderTodos();

function addTodo(){
    var todoText = inputElement.value;
    todos.push(todoText);
    inputElement.value = '';
    renderTodos();
    saveToStorage();
}

buttonElement.onclick = addTodo;

function deleteTodo(pos){
    todos.splice(pos, 1);
    renderTodos();
    saveToStorage();
}

function saveToStorage(){
    localStorage.setItem('list_todos', JSON.stringify(todos));
}
````

### JS Assíncrono

#### 21. Requisições AJAX
- requisitar informações do servidor sem precisar atualizar a página
- recuperar informações do servidor
- arquivo `main.js`
````javascript
var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://api.github.com/users/diego3g');
xhr.send(null);

xhr.onreadystatechange = function(){
    if(xhr.readyState === 4){
        console.log(JSON.parse(xhr.responseText));
    }
}
````
- arquivo `index.html`
- consumir as informações do serviços

#### 22. Promises
- funções para manipulação das informações vinda do servidor
````javascript
var myPromise = function() {

    return new Promise(function(resolve, reject){
        var xhr = new XMLHttpRequest();
        xhr.open('GET', 'https://api.github.com/users/diego3g');
        xhr.send(null);

        xhr.onreadystatechange = function(){
            if(xhr.readyState === 4){
                if(xhr.status === 200) {
                    resolve(JSON.parse(xhr.responseText));
                }else{
                    reject('Erro na requisição');
                }
            }
        }
    });
}

myPromise()
    .then(function(response) {
        console.log(response);
    })
    .catch(function(error) {
        console.warn(error);
    });
````

#### 23. Utilizando AXIOS
- biblioteca AXIOS 
- `https://github.com/axios/axios`
- `npm install axios`
- main.js
````javascript
axios.get('https://api.github.com/users/diego3g')
    .then(function(response) {
        console.log(response);
    })
    .catch(function(error) {
        console.warn(error);
    });
````
- index.html
````html
<html>
    <head>
        <title>Javascript-@douglasabnovato</title>
    </head>
    <body>
        @douglasabnovato
        <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
        <script src="main.js"></script>
    </body>
</html>
````

#### Desafio
- arquivo pdf : desafio3-requisicao-assincrona.pdf

**index.html**
````html
<html>
    <head>
        <title>Javascript-@douglasabnovato</title>
    </head>
    <body>
        @douglasabnovato
        <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
        <script src="main.js"></script>
    </body>
</html>
````
- tarefa 1
````javascript
function checaIdade(idade) {
    return new Promise(function(resolve, reject) {
      setTimeout(function() {
        return idade >= 18 ? resolve() : reject();
      }, 2000);
    });
  }
  
  checaIdade(15)
    .then(function() {
      console.log("Maior que 18");
    })
    .catch(function() {
      console.log("Menor que 18");
    });
````
- tarefa 2
````html
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Exercício 02</title>
</head>

<body>
  <input type="text" name="user">
  <button onclick="listRepositories()">Adicionar</button>

  <ul></ul>

  <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
  <script>
    var listElement = document.querySelector('ul');
    var inputElement = document.querySelector('input');
    function renderRepositories(repositories) {
      for (repo of repositories) {
        const textElement = document.createTextNode(repo.name);
        const liElement = document.createElement('li');
        liElement.appendChild(textElement);
        listElement.appendChild(liElement);
      }
    }
    function listRepositories() {
      var user = inputElement.value;
      if (!user) return;
      axios.get('https://api.github.com/users/' + user + '/repos')
        .then(function (response) {
          renderRepositories(response.data);
        })
    }
  </script>
</body>

</html>
````
- tarefa 3
````html
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Exercício 02</title>
</head>

<body>
  <input type="text" name="user">
  <button onclick="listRepositories()">Adicionar</button>

  <ul></ul>

  <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
  <script>
    var listElement = document.querySelector('ul');
    var inputElement = document.querySelector('input');
    function renderRepositories(repositories) {
      listElement.innerHTML = "";
      for (repo of repositories) {
        const textElement = document.createTextNode(repo.name);
        const liElement = document.createElement('li');
        liElement.appendChild(textElement);
        listElement.appendChild(liElement);
      }
    }
    function renderLoading(loading) {
      listElement.innerHTML = "";
      var textElement = document.createTextNode('Carregando...');
      var loadingElement = document.createElement('li');
      loadingElement.appendChild(textElement);
      listElement.appendChild(loadingElement);
    }
    function renderError(loading) {
      listElement.innerHTML = "";
      var textElement = document.createTextNode('Erro!');
      var errorElement = document.createElement('li');
      errorElement.style.color = "#F00";
      errorElement.appendChild(textElement);
      listElement.appendChild(errorElement);
    }
    function listRepositories() {
      var user = inputElement.value;
      if (!user) return;
      renderLoading();
      axios.get('https://api.github.com/users/' + user + '/repos')
        .then(function (response) {
          renderRepositories(response.data);
        })
        .catch(function () {
          renderError();
        });
    }
  </script>
</body>

</html>
````

:. De Rocketseat - Starter - Javascript.<br>
Por Diego Fernandes : https://skylab.rocketseat.com.br/node/curso-java-script/group/introducao-java-script/lesson/configurando-ambiente-3