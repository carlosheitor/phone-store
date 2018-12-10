#HTML5

É uma linguagem de marcação que tem as seguintes responsabilidades:

- Conteúdo;
- Semântica (tags);
- Estrutura

* `<h1>` - heading 1 - 6
  Usamos ele quando queremos definir títulos

- `<a>` - Link (a - anchor)
  Usamos ela para definir a navegação do usuário. Se você tem um texto que você quer que o usuário clique e ele vá para outro lugar, você pode usar essa tag junto com o o atributo `href`. Exemplo de um `a` que o usuário é direcionado para o site do google.com:

```
<a href="https://google.com">Produtos</a>

```

Float

- É criado um novo contexto na página e o elemento que sofreu com o Float é levado a esse novo contexto. Dessa forma, os elementos que estão abaixo ocupam aquele espaço deixado pelo elemento levado ao novo contexto. Nesse caso, o elemento pai não conhece mais esse elemento filho. Ignorando-o. Lembrando que o pai cresce (altura) de acordo com os elementos filhos que estão em seu contexto. Se em uma determinada situação, os dois filhos estão flutuando, então a altura é zerada e o pai "some" não é visualizado na tela.

- Para o pai reaparecer, ou seja, o elemento pai irá recalcular o contexto (apenas em caso de float): devemos utilizar a propriedade:
  `overflow: hidden`

  - overflow trata o conteúdo que vaza ao elemento. Quando usamos o hidden escondemos esse conteúdo que seja maior que o elemento (conteúdo que vaza).

- O elemento flutuado (float) nunca esconde conteúdo dos elementos que "sobem" para a posição deixada vazia no contexto da página. Logo, todo conteúdo estará visível, apesar do elemento flutuado estar "por cima".

- Quando utilizamos o float, o tamanho do elemento flutuado fica igual ao tamanho conteúdo desse elemento. Logo, o que define height e width é o conteúdo, caso não coloquemos na mão.

- Clear: both/right/left ?? isso exprime que o elemento que usa essa prop, caso tenha um elemento flutuando ao seu lado direito, esquerdo ou os dois, ele desce. Ele não ficará ao lado de um elemento flutuando.

Opacity

-Regra de transparência do elemento. Varia entre 0 e 1.

- Temos respiros no nosso design (Respiros internos e externos):
  - Respiros externos (MARGIN): Quando tenho dois elementos e quero distanciar um do outro, então buscamos o respiro externo (margin). Logo, espaçamento entre dois elementos.
  - Respiros internos (PADDING): se você quiser que o conteúdo dentro do elemento se afaste das extremidades, então estou buscando um respiro interno (padding).

Pq usar class ou id (seletores)?

- quando queremos replicar o comportamento em vários elementos da página, então usamos a class. No caso do ID, não podemos replicar em mais de um elemento, só podemos identificar um! ID é um por página (boa prática);

- Outro seletor são as tags!

#Display

- tag anchor tem display INLINE que tem os seguintes comportamentos:

  - permite que os elementos ficam um ao lado do outro por padrão (na mesma linha);
  - não conseguimos definir a altura (heigth) e largura (width);
  -

- tag anchor tem display BLOCK que tem os seguintes comportamentos:
  - esse permite colocar a altura e largura, mas repara que o elemento vai um para baixo do outro;
- não deixa na mesma linha (padrão);

-DISPLAY INLINE BLOCK:

- Nós temos o melhor dos dois mundos:

  - permite definir width e height;
  - deixa elementos na mesma linha;

- Alinhamento:

  - Quando temos uma única linha dentro de uma caixa (ou quando não ultrapassamos a largura do elemento) para alinhar verticalmente ao centro do botão, por exemplo, utilizamos a prop line-height igualando o valor com o valor da altura da caixa, dessa forma o elemento fica no centro.

  - O que é refatoração: você escreve melhor o código, ou seja, melhora a qualidade do código sem adicionar nenhuma nova funcionalidade;

* Nomenclatura de elementos (componentes):

  - usar o padrão de escrever com dois nomes.
  - lembra de renomear o nome do arquivo com o nome do componente mãe. Ex: header

  * POSITION: Absolute:
    - cria um novo contexto, tal como o float;
    - pq diminui a largura assim que colocamos o position absolute, é pq assim como no float quem passa a definir a largura é o conteúdo do elemento;
    - propriedade que podemos usar: top, left / bottom, right. Mas pq em pares: pois cada uma mexe com os mesmos elementos. O top e bottom mexem com eixo x e right e left com o eixo y. Dessa forma, conseguimos mover o elemento em relação a página;
    - utilizando a porcentagem conseguimos posicionar o elemento em relação ao pai do elemento, porém lembrando que nivela pelo lado(propriedade) escolhido de cima do elemento;


    * Transform
     - translate: move em relação ao eixo do elemento;


     * Dicas
      - Width e Height, quando usamos a porcentagem, utilizamos como referência o pai;
      - o que é Call To Action ? é o botão de ação. É o botão que você realmente quer que o usuário clique. Nesse projeto é o botão comprar. Também conhecido como CTA. Nesse projeto o botão adicionar o carrinho seria o nosso botão secundário;
      - elementos que estão inline serão alinhados pela base da linha (baseline). Claro, se você não tiver setado o alinhamento vertical; Para tal, temos a propriedade vertical-align que alinha elementos display inline;
      - VARIAÇÃO NO CSS: toda classe que começa com o traço no CSS é uma variação. Mas o que é esse troço de VARIAÇÃO: ela precisa de uma base e depois dessa base é adicionado um recurso que fará uma diferença com aquela base;
      - Quando estamos descrevendo algo existe uma tag específica para isso, chamada: description list (<dl>); e para o título desses itens de descritivos é chamada de (<dt>); e para definir o que estou escrevendo é o <dd>; Isso torna seu código mais semântico e legível.
      - utilizar o seletor direto é mais perfomático. Fica mais "baratao" para o navegador;

- BOX-SIZING
  - Padrão é o content-box (o conteúdo é o que defini a largura e altura, tanto que qdo colocamos um border aumentamos o tamanho real dessas propriedades. O width aumenta de acordo com as border laterais e o heigth de acordo com as border top e bottom). Quando você coloca border-box, você informa que a borda é parte da caixa e o width e o heigth de dentro da caixa são subtraídos dos valores das bordas, porém permanece intacto os valores definidos no width e heigth. Por conta desse subtrair, muitas vezes precisamos diminuir o line-height do elemento pelos valores da borda para alinhar elementos inline;
