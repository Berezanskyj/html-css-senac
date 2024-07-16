
# Introdução ao HTML e CSS

**Aprendendo HTML e CSS**
> Repositório feito para os estudos de HTML e CSS do curso de TDS do Senac Tech


## CSS Inline

CSS inline é aplicado diretamente aos elementos HTML usando o atributo `style`.

```html
<p style="color: red; margin: 20px;">Parágrafo formatado com CSS em linha.</p>
````

## CSS Interno
CSS interno é definido dentro de um bloco `<style>` na seção `<head>` do documento HTML. Este método é útil para definir estilos que são específicos para um único documento HTML.

```html
<head>
    <style>
        p {
            color: blue;
            margin: 20px;
        }
    </style>
</head>
```

## CSS Externo
Para utilizar arquivos CSS externos em uma página HTML, o documento HTML deve conter um link para um arquivo de estilos na seção `<head>`. Este método é preferido para projetos maiores, pois permite separar o conteúdo HTML da apresentação.

```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

####  Estrutura de arquivo:
```shell
project-folder/
│
├── index.html
└── styles.css
```

## Seletor de classe
O seletor de classe é uma maneira de aplicar estilos a elementos específicos no HTML. Você define uma classe no seu HTML e depois usa o CSS para estilizar todos os elementos que têm essa classe. No CSS, utiliza-se um ponto `.` seguido pelo nome da classe enquanto no HTML utiliza-se o comando `class=`
#### Exemplo no HTML
```html
<p class="exemplo-classe">
        Este é um parágrafo dentro de uma div com a classe "exemplo-classe".
    </p>
```
#### Exemplo no CSS
```css
.exemplo-classe {
    color: blue;
    background-color: lightgray;
    padding: 10px;
    border: 1px solid black;
}
```

### Unidades de medidas em CSS

```%``` -> percentual em relação ao elemento pai  
```em``` -> relação ao tamanho da fonte atual  
```pt``` -> pontos, smelhantes ao tamanhos utilizados no software Word    
```px``` -> pixel, é o tamanho de um pixel na tela do dispositivo


# Uso da Tag <table> no HTML
A tag ```<table>``` no HTML é utilizada para criar tabelas que organizam dados em linhas e colunas. Ela é especialmente útil para exibir informações tabulares de forma estruturada e clara.

## Estrutura Básica
A estrutura básica de uma tabela HTML envolve várias tags aninhadas, cada uma com uma função específica:

* ```<<table>```<: Define o início e o fim de uma tabela.
* ```<<tr>```<: Define uma linha da tabela.
* ```<<th>```<: Define uma célula de cabeçalho em uma tabela. Normalmente, é usada dentro de uma linha de cabeçalho (<thead>).
* ```<<td>```<: Define uma célula padrão em uma tabela.

### Exemplo de Código
```html
<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Idade</th>
      <th>Profissão</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Maria</td>
      <td>30</td>
      <td>Engenheira</td>
    </tr>
    <tr>
      <td>João</td>
      <td>45</td>
      <td>Médico</td>
    </tr>
  </tbody>
</table>
```
###  Resultado

| Nome   | Idade | Profissão |
| ------ |------ | ----------|
| Maria  | 30    | Engenheira|
| João   | 47    | Médico    |

### Explicação do Exemplo

* `<table>`: Inicia a tabela.
* `<thead>`: Define o cabeçalho da tabela.
* `<tr>`: Dentro do <thead>, define uma linha que contém células de cabeçalho <th>.
* `<th>`: Define cada célula de cabeçalho com os títulos "Nome", "Idade" e "Profissão".
* `<tbody>`: Define o corpo da tabela, onde os dados reais serão inseridos.
* `<tr>`: Cada linha de dados é definida com uma tag <tr>.
* `<td>`: Define cada célula de dados com os valores correspondentes, como "Maria", "30" e "Engenheira".

## Atributos Comuns
* `border`
Define a largura da borda da tabela.
### Exemplo
```html 
<table border="1">
  ...
</table>
```

* `cellpadding` e `cellspacing`
Controlam o espaçamento interno das células e o espaçamento entre as células, respectivamente.
### Exemplo
```html 
<table cellpadding="10" cellspacing="5">
  ...
</table>
```

* `colspan` e `rowspan`
Permitem que uma célula se estenda por várias colunas ou linhas.
### Exemplo
```html 
<tr>
  <td colspan="2">Célula que ocupa duas colunas</td>
</tr>
<tr>
  <td rowspan="2">Célula que ocupa duas linhas</td>
</tr>
```

## Estilização
Para uma estilização mais avançada, CSS pode ser aplicado diretamente às tabelas.

### Exemplo com CSS

```css
<style>
  table {
    width: 100%;
    border-collapse: collapse;
  }
  th, td {
    border: 1px solid black;
    padding: 8px;
    text-align: left;
  }
  th {
    background-color: #f2f2f2;
  }
</style>

<table>
  ...
</table>
```