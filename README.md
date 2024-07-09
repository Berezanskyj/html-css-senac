
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