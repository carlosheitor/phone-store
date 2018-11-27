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

Opacity

-Regra de transparência do elemento. Varia entre 0 e 1.

- Temos respiros no nosso design (Respiros internos e externos):
  - Respiros externos (MARGIN): Quando tenho dois elementos e quero distanciar um do outro, então buscamos o respiro externo (margin). Logo, espaçamento entre dois elementos.
  - Respiros internos (PADDING): se você quiser que o conteúdo dentro do elemento se afaste das extremidades, então estou buscando um respiro interno (padding).
