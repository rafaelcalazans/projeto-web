# Anatomia de um elemento HTML 

site-teste/imagens/gato-rabujento-pequeno.png

// exemplo do index.html //

° <!DOCTYPE html> = não precisa se preocupar, mas tem que ter em todo HTML.

° <html></hmtl> elemento que envolve todo o conteúdo da página.

° <head></head> elemento recipiente, mas não é conteudo visivel. Pode descrição que você quer que aparece no resultados de busca, CSS para dar estilo ao conteudo , declaração de conjuntos de caracteres.

° <meta charset="utf-8"> elemento que define o conjunto de caracteres que seu documento deve usar. Essencialmente, agora ele pode manipuçar qualquer conteúdo textual. Não há razão para não definir

° <title></title> elemento que define o título da sua pagína. 

° <body></body> elemento que você quer mostrar ao público. 

# Aninhando elementos

<p>Meu gatinho é <strong>muito</strong> mal humorado.</p>

Precisamos certificar que os elementos estejam adequandamente aninhados, temos que fechar o primeiro elemento <strong> depois
o elemento <p>

<p>Meu gatinho é <strong>muito mal humorado.</p></strong>
<--! acima o exemplo incorreto !-->

# Elemento vazios

Alguns elementos não possuem conteúdo e são chamados de elementos vazios. Considere o elemento <img>. 

<img src="imagens/firefox-icon.png" alt="Minha imagem de teste" />

Ele contém dois atributos, mas não há tag </img> de fechamneto. 
E não há conteúdo interno. Sua proposta é incorporar uma imagem
na paágina HTML no lugar que o código aparece.

<img src="images/firefox-icon.png" alt="Minha imagem de teste" />
 Atributo "SRC" (source) incorpora uma imagem 
 Atributo "ALT" (alternative), especifica um texto descritivo. O ideal é fornecer informações suficientes para ter uma boa ideia do que a imagem mostra. 

 # Marcando o texto
                            Cabeçalhos 
 Os elementos permitem especificar certas partes do conteúdo, são títulos ou subtítulos, contem 6 níveis de título <h1> - <h6>

 <!-- 4 níveis de título -->
<h1>Meu título principal</h1>
<h2>Meu título de alto nível</h2>
<h3>Meu subtítulo</h3>
<h4>Meu segundo subtítulo</h4>

Nota: Qualquer coisa em HTML entre <!-- e --> é um comentário HTML. O navegador ignora comentários enquanto renderiza o código. Em outras palavras, eles não são visíveis na página – apenas no código. Os comentários HTML são uma forma de escrever notas úteis sobre seu código ou lógica.

                            Parágrafo
<p> elemento de parágrafos

<p>Este é um parágrafo simples</p>

                            Listas

Lista de marcação sempre consistem em pelo menos 2 elementos. ordenadas e não ordenadas.

1 - Listas não ordenadas <ul> a ordem dos itens não importa.
2 - Listas ordenadas <ol> a ordem dos itens importa.

Cada item dentro das listas é posto dentro de um elemento <li> (item de lista).

EXEMPLO: tornar uma parte de um parágrafo numa lista:

<p>
  Na Mozilla, somos uma comunidade global de tecnólogos, pensadores e
  construtores trabalhando juntos ...
</p>

Podemos fazer assim: 

<p>Na Mozilla, somos uma comunidade global de</p>

<ul>
  <li>tecnólogos</li>
  <li>pensadores</li>
  <li>construtores</li>
</ul>

<p>trabalhando juntos ...</p>

                    LINK

<a> (âncora) Transforma o texto do seu parágrafo em um link
HREF é um atributo (refereência em hipertexto) "a", seguindo pelo link que deseja. 

<a href="https://www.mozilla.org/pt-BR/about/manifesto/"
  >Mozilla Manifesto</a>

https:// e http:// são protocolos, devemos sempre utilizar  
















