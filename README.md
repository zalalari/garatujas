## HTML - HyperText Markup Language (Linguagem de Marcação de Hipertexto)
HTML é, como o nome diz, uma linguagem de marcação. Ou seja, nós a utilizamos para estruturar uma página web, o visual da página. Ele organiza o conteúdo da página web para que possa ser consumido por todo tipo de usuário, incluindo aqueles com deficiências. 
No HTML existem as chamadas tags(etiquetas), que tem o tipo de conteúdo e sua função na página definidos. Por exemplo, `<h1>` é usado para títulos principais, `<p>` para parágrafos, `<a>` para links, entre outros. O HTML também permite a inclusão de atributos nas tags para fornecer informações adicionais sobre os elementos, como `class`, `id`, `src`, etc.
As tags ficam dentro de colchetes `<>`, `<p>`por exemplo. O início de uma tag começa somente com os colchetes, `<strong>`, e utiliza a barra (/) para fecha-la, `</strong>`.

>**NOTA** 
Sempre que o negrito ou itálico tiver significado no conteúdo, prefira `<strong>` e `<em>`. Use `<b>` e `<i>`apenas quando a intenção for exclusivamente estética.
>

### Estrutura básica de um documento HTML

```html
<!DOCTYPE html>
<html lang="pt-BR">

<head>
   <meta charset="UTF-8">
   <title>Título da Página</title>
   <!-- Links para arquivos CSS e scripts JavaScript podem ser adicionados aqui -->
</head>
<body>
   <!-- Conteúdo visível da página é adicionado aqui -->
</body>
</html>
```
  
Todo documento HTML começa com `<!DOCTYPE html>`, que define que usaremos a linguagem HTML. Ele é dividido em duas partes principais: `<head>` e `<body>`.  
O `<head>` contém informações sobre a página, como título, estilos (CSS) e metadados, que não aparecem no visual do site.  
O `<body>` contém todo o conteúdo visível da página, como textos, imagens, links e outros elementos.
Todo o código HTML deve estar dentro da tag `<html>`, que representa a raiz do documento. O lang="pt-BR" define o idioma da página. A tag `<meta charset="UTF-8">` representa os caracteres que serão utilizados. Já a tag `<title>+` define o título da página, que aparece na aba do navegador e nos resultados da busca.

### Atributos HTML

OS atributos do HTML são usados para dar informações adicionais aos elementos (tag) do HTML, eles são postos dentro da tag de abertura e consistem em um nome e um valor, separados por um sinal de igual `=`. Os atributos são usados para definir propriedades específicas de um elemento, como sua aparência, comportamento ou funcionalidade. Por exemplo, o atributo `href` em `<a>` define o destino de um link, enquanto o atributo `src` em `<img>` indica a fonte da imagem. Os atributos são essenciais para controlar o comportamento e a personalização dos elementos HTML, tornando as páginas mais interativas.

## CSS - Cascading Style Sheets (Folhas de Estilo em Cascata)

O CSS é uma linguagem de estilo, ela é usada para controlar a aparência de uma página web. Ela permite que você defina um estilo para as tags do HTML, como cores, fontes, margens, espaçamento, entre outros.
O HTML e o CSS são coisas diferentes, o HTML define a estrutura do conteúdo e o CSS seu estilo, tornando o site mais organizado e facilitando futuras manutenções.
O CSS contém seletores, os seletores são responsáveis por selecionar as tags do HTML, tags que terão um estilo será aplicado. O CSS contém também as declaracões que são responsaveis para definir como a tag será mudada. As declarações são divididas em duas partes: A propriedade, que indica o que será alterado (por exemplo, cor, tamanho, espaçamento), e o valor, que define como essa alteração será aplicada.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
   <meta charset="UTF-8">
   <title>Exemplo de CSS</title>
   <link rel="stylesheet" href="styles.css">
</head>
<body>
   <h1>Olá, Mundo!</h1>
   <p>Este é um exemplo de CSS.</p>
</body>
</html>
```
Nesse exemplo temos um documento HTML simples. O arquivo CSS, `styles.css` é conectato a esse documento usando a tag `<link>`dentro da tag `<head>`, onde ficam os metasdados que não aparecem no visual do site. 

```css
/* styles.css */
body {
  background-color: #f0f0f0;
  font-family: Arial, sans-serif;
}

h1 {
  color: #333333;
  text-align: center;
}

p {
  color: #666666;
  font-size: 18px;
  margin: 20px;
}
```
O conteúdo do arquivo `styles.css` pode ser como o exemplo acima.

Sem o CSS a página seria exibida no estilo padrão do navegador no qual a página foi aberta. Chamamos isso de user agent stylesheet, que é o estilo padrão aplicado pelo navegador aos elementos HTML. O CSS permite que você substitua esse estilo padrão da maneira que você quiser.

### Sintaxe do CSS

A sintaxe do CSS é composta por regras de estilo, onde cada regra é formada por um seletor, que seleciona a tag que terá um estilo aplicado, e um bloco de declarações, que indica o que e como será mudado o elemento.

```css
seletor {
  propriedade: valor;
  propriedade: valor;
  /* ... */
}
```

> **⚠️ Nota:**
>
> O seletor pode ser um nome de elemento HTML, uma classe, um ID ou uma combinação desses. As propriedades de estilo são palavras-chave que definem o aspecto visual dos elementos, como `color`, `font-size`, `background-color` etc. Os valores são atribuídos às propriedades para especificar o estilo desejado, como `red`, `16px`, `#f0f0f0` etc. Cada declaração dentro do bloco de declarações deve ser separada por um ponto e vírgula `;`, e o bloco de declarações deve ser encerrado com uma chave `}`.

### Seletores CSS

Os seletores são responsáveis por selecionar as tags do HTML, tags que terão um estilo será aplicado. A lógica dos seletores é baseada na estrutura do documento HTML, e eles permitem que você aplique estilos a elementos específicos ou a grupos de elementos com base em suas características, como tipo, classe, ID, atributos, entre outros.

Para aplicar estilos a esses elementos usando CSS, podemos usar diferentes tipos de seletores. Por exemplo:

1. Seletor de tipo: para selecionar todos os elementos de um determinado tipo, como `<h1>`, `<p>`, `<a>` etc. Exemplo: `h1 { color: blue; }` aplicaria a cor azul a todos os elementos `<h1>` na página.
2. Seletor de classe: para selecionar elementos com uma classe específica. Exemplo: `.titulo { font-size: 24px; }` aplicaria um tamanho de fonte de 24 pixels a todos os elementos com a classe "titulo".
3. Seletor de ID: para selecionar um elemento com um ID específico. Exemplo: `#paragrafo1 { color: red; }` aplicaria a cor vermelha apenas ao elemento com o ID "paragrafo1".
4. Seletor de atributo: para selecionar elementos com um atributo específico ou um valor de atributo específico. Exemplo: `a[href="#"] { text-decoration: none; }` removeria o sublinhado de todos os links que têm um atributo `href` com o valor "#".
5. Pseudo-classes: para selecionar elementos com base em seu estado ou posição na hierarquia do documento. Exemplo: `p:first-child { font-weight: bold; }` aplicaria negrito ao primeiro parágrafo dentro de seu elemento pai.

   Considere esse exemplo:

```html
<main>
  <section>
   <p>Este é um parágrafo dentro de uma seção...</p>
  </section>
</main>
```
Se adicionarmos esse seletor, `main section p { color: green; }` no CSS, somente o conteúdo da tag `<p>>` estaria na cor verde, porque estariamos usando um seletor de decendente. O seletor de decendentes, nesse caso, seleciona paragrafos que estão dentro de uma seçâo, que por sua vez esta dentro do `<main>`.

> **⚠️ Nota:**
>
> Os espaços entre os seletores indicam uma relação de descendência, ou seja, o seletor `main section p` seleciona todos os elementos `<p>` que são descendentes de um elemento `<section>`, que por sua vez é um descendente de um elemento `<main>`. Isso permite que você aplique estilos de forma mais específica, garantindo que apenas os elementos desejados sejam afetados pelas regras de estilo.

### Tipos de Seletores CSS

Existem diversos seletores CSS que permitem escolher elementos HTML de formas diferentes. A tabela a seguir apresenta os principais tipos, funcionando como um guia rápido para entender como eles operam. Embora existam outros seletores, foque nesses mais comuns, pois são os mais usados e essenciais para aprender CSS.

| Tipo de Seletor               | Exemplo&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Descrição |
|------------------------------ | -------------------------------- | --------- |
| Seletor de Tipo               | `nome_elemento { }`              | Seleciona todos os elementos de um determinado tipo. Exemplo: `p { color: blue; }` seleciona todos os parágrafos e aplica a cor azul. |
| Seletor de Classe             | `.nome_classe { }`               | Seleciona elementos com uma classe específica. Exemplo: `.titulo { font-size: 24px; }` seleciona todos os elementos com a classe "titulo" e aplica um tamanho de fonte de 24 pixels. |
| Seletor de ID                 | `#nome_id { }`                   | Seleciona um elemento com um ID específico. Exemplo: `#paragrafo1 { color: red; }` seleciona o elemento com o ID "paragrafo1" e aplica a cor vermelha. |
| Seletor de Atributo           | `elemento[atributo="valor"] { }` | Seleciona elementos com um atributo específico ou um valor de atributo específico. Exemplo: `a[href="#"] { text-decoration: none; }` seleciona todos os links que têm um atributo `href` com o valor "#" e remove o sublinhado. |
| Pseudo-classes                | `elemento:pseudo-classe { }`     | Seleciona elementos com base em seu estado ou posição na hierarquia do documento. Exemplo: `p:first-child { font-weight: bold; }` seleciona o primeiro parágrafo dentro de seu elemento pai e aplica negrito. |

Seletores de descendentes, filhos e irmãos:

| Tipo de Seletor               | Exemplo&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Descrição |
|------------------------------ | -------------------------------- | --------- |
| Seletor de Descendente        | `elemento1 elemento2 { }`        | Seleciona elementos que são descendentes de um elemento específico. Exemplo: `main section p { color: green; }` seleciona todos os parágrafos que estão dentro de uma seção, que por sua vez está dentro do elemento principal `<main>`, e aplica a cor verde. |
| Seletor de Filho              | `elemento1 > elemento2 { }`      | Seleciona elementos que são filhos diretos de um elemento específico. Exemplo: `main > section { background-color: lightgray; }` seleciona todas as seções que são filhos diretos do elemento principal `<main>` e aplica um fundo cinza claro. |
| Seletor de Irmão Adjacente    | `elemento1 + elemento2 { }`      | Seleciona um elemento que é imediatamente precedido por outro elemento específico. Exemplo: `h1 + p { margin-top: 0; }` seleciona o parágrafo que vem imediatamente após um título `<h1>` e remove a margem superior. |
| Seletor de Irmão Generalizado | `elemento1 ~ elemento2 { }`      | Seleciona elementos que são irmãos de um elemento específico, independentemente de sua posição. Exemplo: `h1 ~ p { color: gray; }` seleciona todos os parágrafos que são irmãos de um título `<h1>` e aplica a cor cinza. |

