# Anatomia de um conjunto de regras CSS 

<img src="imagens/css-declaration-small.png"/>

Toda a estrutura é chamada de conjunto de regras (regra). 

* Seletor(Selector) Seleciona o(s) elemento(s) a serem estilizados. 

* Declaração(Declaration) Especifica quais das propriedades do elemento você quer estilizar. 

* Propriedades(Property) Forma pela qual você estiliza umelemento HTML. Em CSS, você escolhe quais propriedades você deseja afetar com sua regra. 

* Valor da propriedade(Property value) À direta da propriedade, depois dos dois pontos, nós temos o valor de propriedade

Outras partes importante da sintaxe: 

° Cada linha de comando deve ser envolvida em chaves ({}).
° Dentro de cada declaração, você deve usar dois pontos (:) para separar a propriedade de seus valores.
° Dentro de cada conjunto de regras, você deve usar um ponto e vírgula (;) para separar cada declaração da próxima.

# Selecionando múltiplos elementos 

Podemos selecionar vários elementos e aplicar um único conjunto de regras a todos eles, separando por vírgulas. POr exemplo:

p,
li,
h1 {
  color: red;
}

# Diferentes tipos de seletores 

° Seletor de elemento:
  Seleciona o(s) Elementos HTML de determinado tipo.
  p Seleciona <p>

° Seletor de ID:
  Seleciona o elemento na página com o ID específicado. boa prática é usar um elemento por ID (e claro, um ID por elemento) mesmo que seja permitido usar o mesmo ID para vários elementos. 
  #my-id Seleciona <p id="my-id"> ou <a id="my-id">

° Seletor de classe:
  Seleciona o(s) elemento(s) na página com a classe específicada (várias instâncias de classe podem aparecer em uma página)
  .my-class Seleciona <p class="my-class"> e <a class="my-class">

° Seletor de Atributo:
  O(s) elemento(s) na página com o atributo especificado. 
  img[src] Seleciona <img src="myimage.png"> mas não <img>

° Seletor de pseudo-classe:
  O(s) elemento(s) específicado(s), mas somente quando estiver no estado especificado. Ex.: com o mouse sobre ele. 
  a:hover Seleciona <a>, mas somente quando o mouse está em cima do link.  

# Fontes e texto

As fontes devem ser escolhidas com coerencia, definir tamanho e a familia <font-size> <font-family>

# Caixas, caixas, é tudo sobre caixas.

Uma coisa que notamos sobre escrever CSS é que muito disso é sobre caixas - indicar seu tamanho, cor, posição, etc. Muitos dos elementos HTML podem ser pensados como caixas umas em cima das outras. 

O layout CSS é baseado principalmente no modelo de caixas. Cada um dos blocks que ocupam espaço na sua página tem propriedades como essas: 

° padding, o espaço ao redor do conteúdo.
° border, a linha sólida do lado de fora do padding.
° margin, o espaço externo a um elemento.
° width, (largura de um elemento). 
° background-color, a cor atrás do conteúdo de um elemento e do padding. 
° color, a cor do conteúdo de um elemento (geralmente texto).
° text-shadow: cria uma sombra no texto dentro de um elemento. 
° display: define a maneira de dispor uma elemento. 

Nota: As instruções acima assumem que você está usando uma imagem menor que a largura definida no corpo (600 pixels). Se sua imagem for maior, ela irá transbordar o corpo e vazar para o restante da página. Para corrigir isso, você pode 1) reduzir a largura da imagem usando um editor gráfico (em inglês) ou 2) dimensionar a imagem usando CSS definindo a propriedade width no elemento <img> com um valor menor (por exemplo, 400 px;

Nota: Não se preocupe se você ainda não entender display: block; ou a distinção entre em nível de bloco / em linha. Você entenderá ao estudar CSS com mais profundidade. Você pode descobrir mais sobre os diferentes valores de exibição disponíveis em nossa página de referência sobre display.