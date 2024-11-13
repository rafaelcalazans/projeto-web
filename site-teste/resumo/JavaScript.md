# Noções básicas de JavaScript

JavaScript é uma linguagem de programação que adiciona interatividade ao seu site. Isso acontece em jogos, no comportamento das respostas quando botões são pressionados ou com entrada de dados em formulários, com estilo dinâmico; com animação.

O próprio JavaScript é relativamente compacto, mas muito flexível. Os desenvolvedores escreveram uma variedade de ferramentas sobre a linguagem JavaScript principal, desbloqueando uma grande quantidade de funcionalidades com o mínimo de esforço. Esses incluem:

° Interfaces de programação de aplicativos de navegador (APIs) incorporadas a navegadores da Web, fornecendo funcionalidades como criação dinâmica de HTML e definição de estilos CSS; coletar e manipular um fluxo de vídeo da webcam de um usuário ou gerar gráficos 3D e amostras de áudio.

° APIs de terceiros que permitem aos desenvolvedores incorporar funcionalidades em sites de outros provedores de conteúdo, como Twitter ou Facebook.

° Estruturas e bibliotecas de terceiros que você pode aplicar ao HTML para acelerar o trabalho de construção de sites e aplicativos.

## Variáveis

Variáveis são contêineres que armazenam valores.

let myVariable;

Você pode nomear uma variável para praticamente qualquer coisa, mas há algumas restrições.
JavaScript diferencia maiúsculas de minúsculas.

Atribuir uma valor a variável:

myVariable = "Bob";

podemos fazer essas duas operações na mesma linha:

let myVariable = "Bob";

Recuperamos o valor chamando o nome da variável:

myVariable;

Depois de atribuir um valor a uma variável, você pode alterá-lo posteriormento no código: (somente LET)

let myVariable = "Bob";
myVariable = "Steve";

Tipos de Dados:

1 - STRING
Esta é uma sequência de texto conhecida como string. Para signficar que o valor for uma string, coloque-a entre aspas simples.

let myVariable = 'Bob';

2 - NUMBER
Isto é um número. Os números não têm aspas:

deixe minhaVariável = 10;

3 - BOOLEAN
Valor verdadeiro ou Falso. As palavras TRUE e FALSE são palavras-chave especiais que não precisam de aspas:

let myVariable = true;

4 - ARRAY
Estrutura que permite armazenar vários valores em uma única referência:

let myVariable = [1,'Bob','Steve',10];
Refere-se a cada membro do array assim:
myVariable[0], myVariable[1], etc.

5 - OBJECT
Isso pode ser qualquer coisa. Tudo em JavaScript é um objeto e pode ser armazenados em uma variável.

let myVariable = document.querySelector('h1');
Todos os exemplos acima também.

Então, por que precisamos de variáveis? As variáveis são necessárias para fazer qualquer coisa interessante na programação. Se os valores não pudessem ser alterados, você não poderia fazer nada dinâmico, como personalizar uma mensagem de saudação ou alterar uma imagem exibida em uma galeria de imagens.

COMENTÁRIOS
Comentários são trechos de texto que podem ser adicionados junto com o código. Igual ao CSS

/*
Tudo no meio é um comentário.
*/

Comentarios de uma linha usar, duas barras:

// Isso é um comentário

## Condicionais

Condicionais são estruturas de código usadas para testar se uma expressão retorna verdadeira ou não. Exemplo de condicionais é a instrução IF...ELSE.

let iceCream = "chocolate";
if (iceCream === "chocolate") {
  alert("Sim, eu amo sorvete de chocolate!");
} else {
  alert("Aaaah, mas chocolate é o meu favorito…");
}

A expressão dentro do if () é o teste. Isso usa o operador de igualdade estrita (conforme descrito acima) para comparar a variável iceCream com a string chocolate para ver se as duas são iguais. Se esta comparação retornar true, o primeiro bloco de código será executado. Se a comparação não for verdadeira, o segundo bloco de código — após a instrução else — será executado.

## Funções

Funções são uma forma de empacotar a funcionalidade que você deseja reutilizar. É possível definir um corpo de código como uma função que é executada quando você chama o nome da função em seu código. Esta é uma boa alternativa para escrever repetidamente o mesmo código.

let myVariable = document.querySelector("h1");

alert("olá!");

Essas funções, document.querySelector e alert, são incorporadas ao navegador.

Se você ver algo parecido com uma variável, seguido por () provamente é uma função. As funções geralmente usam argumentos: bits de dados de que precisam para realizar o trabalho. Os argumentos ficam dentro dos parênteses, seprados por vírgulas se houver mais de um argumento.

A função de exemplo alert() faz com que uma caixa pop-up apareça na janela do navegador, mas precisamos dar a ela uma string como argumento para informar à função qual mensagem exibir.

Podemos definir nossas proprias funções, abaixo uma função simples que recebe dois números como argumento e os multiplica.

function multiply(num1, num2) {
  let result = num1 * num2;
  return result;
}

Exemplo para executar no console:

multiply(4, 7);
multiply(20, 20);
multiply(0.5, 3);

Nota: A instrução return diz ao navegador para retornar a variável result da função para que ela esteja disponível usar. Isso é necessário porque as variáveis definidas dentro das funções só estão disponíveis dentro dessas funções. Isso é chamado de variável escopo.

## Eventos

A interatividade real em um site requer manipuladores de eventos são estruturas de código que detectam atividades, por exemplo um click do mouse. Segue abaixo um exemplo de código:

document.querySelector("html").addEventListener("click", function () {
  alert("Ai! Pare de me cutucar!");
});

Selecionamos o elemento <html> e chamamos sua função addEventListener(), passando o nome do evento para ouvir ('click') e uma função para executar quando o evento acontecer.

addEventListener() aqui é chamada de função anônima, porque não tem um nome. Podemos escrever como uma função de seta. Uma função de seta usa () => em vez de function (). 

document.querySelector("html").addEventListener("click", () => {
  alert("Ai! Pare de me cutucar!");
});

### Adicionando um trocar de imagens 

const myImage = document.querySelector("img");

myImage.onclick = () => {
  const mySrc = myImage.getAttribute("src");
  if (mySrc === "images/firefox-icon.png") {
    myImage.setAttribute("src", "images/firefox2.png");
  } else {
    myImage.setAttribute("src", "images/firefox-icon.png");
  }
};

Armazenamos uma referência ao elemento <img> na variável **myImage**. Em seguida, tornei a propriedade do manipulador de eventos **onclik** desta variável igaul a uma função "anônima". Toda vez que esse elemento for clicado: 

1. O código recupera o valor do atributo **src** da imagem. 
2. O código usa uma condicional para verificar se o vaor **src** é igual ao caminho da imagem original. 
  i. Se for, o código altera o valor **src** para o caminho da segunda imagem, forçando a outra imagem a ser carregada dentro do elemento **img**. 
  ii. Se não for o valor **src** volta para o caminho da imagem original. 

### Adicionando uma mensagem de boas-vindas personalizada. 

1. Vamos adicionar a seguinte linda antes do elemento <script> no index.html:

<button>Alterar usuário</button>

2. adicionamos ao arquivo main.js duas variaveis internas:

let myButton = document.querySelector("button");
let myHeading = document.querySelector("h1");

3. e a seguir: a função para definir a saudação personalizada:

function setUserName() {
  const myName = prompt("Por favor, digite o seu nome");
  localStorage.setItem("name", myName);
  myHeading.textContent = `Mozilla é legal, ${myName}`;
}

A função **setUserName()** contém a função **prompt()** que exibe uma caixa de diálogo, solicitando ao usuário que insira dados e armazenando-os em uma variável após clicar em *OK*. Nesta caso estamos solicitando que o usuário insira um nome. O código chama uma API **localStorage**, que nos permite armazenar dados no navegador e recuperá-lo posteriormente. Usamos a função **setItem()** do localStorage para criar e armazenar um item de daos chamado **'name'**, configura seu valor para a variável **myName**  que contém a entrada do usuário para o nome. Definimos o **textContent** do cabeçalho como uma string, mais o nome do usuário. 

4. Adicionando um bloco de condição ou código de inicialização, pois ele estrutura o aplicativo quando é carregado pela primeira vez. 

if (!localStorage.getItem("name")) {
  setUserName();
} else {
  const storedName = localStorage.getItem("name");
  myHeading.textContent = `Mozilla é legal, ${storedName}`;
}

