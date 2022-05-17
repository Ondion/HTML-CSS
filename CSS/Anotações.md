# Referenciando o CSS  

[*_Documentação do CSS_*](http://www.w3.org/Style/CSS/) 

**External CSS:**  
 * Método de *_link_*, basta adicionar no head da pagina a tag: `<link rel=¨stylesheet¨ href="styles.css">` lembrando que é necessário respeitar o caminho até o arquivo CSS. Para o HTML4 ou anterior, existe uma pequena variação: `<link rel="stylesheet" href="styles.css" type=¨text/css¨>`  
 A vantagem de usar o método externo é a facilidade de "linkar" varias páginas HTML em um único arquivo CSS. Lembrando, também, que é possivel usar diversos arquivos CSS em um mesmo projeto.
  *  Médoto *_@import_*, usado para anexar diversas páginas CSS em apenas uma que será usada no projeto, exemplo: 
```
  styles.css
  @import url('/styles/layout.css');
  @import url('/styles/buttons.css');

  index.html
    <head>
        <style> @import url("/css/styles.css"); </style>
    </head>
```
**Inline CSS:**  
adiciona o style diretamente na tag do arquivo HTML, o método não é indicado por poluir o código e não poder ser reaproveitado em outro momento, logo, seria necessário aicionar elementos CSS em todas as tags HTML, segue exemplo de *_inline_* CSS:
 * `<p style="color: red;> paragrafo vermelho!"</p>`

**Internal CSS:**  
adiciona o style dentro da tag HTML head, é útil quando não existe uma grande quantidade de elementos CSS para serem adicionados, também não pode ser reaproveitado em outras páginas. Exemplo de HTML com CSS interno:
```
<head>
    <style>
        h1 {
            color: green;
            background-color: blue;
        }

        h2 {
            color: yellow;
        }
    </style>
</head>
```

**Comentário**
O comando para comentário é: /* Escreva aqui o comentário */

# Seletores
Segue a lista de seletores mais usados no CSS:
 * Type Selector - Usado diretamente nas tags do HTML, exemplo:`<h1>` Ao usar o type selector, todas as tags de mesmo nome irão sobre a modificação adicionada no bloco.
 * Universal Selector - Usado para aplicar um estilo em todas as tags HTML do documento. A sintaxe é: `*{}`
 * Class Selector - Adiciona estilo a tag por meio de classes previamente adicionadas, Exemplo: `<p class="classe_css">`. No arquivo CSS: `.classes_CSS{}` É possivel também usar multiplas classes em uma mesma tag, Exemplo: `<p class="classe_css"` `"outra_CSS">`
 * ID Selector  - É usado de forma individual por tag, deve sempre ser único no HTML, exemplo: `<p id="id_css"> `e no arquivo style: `#id_css{}` Outro ponto, fora do CSS, o ID pode ser usado para "linkar" conteúdo dentro da página.  
 *_Exemplo:_*  
 ``` 
<a href="#exemplo">Link para outro ponto da página</a>
...
...
...
<section id="exemplo">O link vai parar aqui!</section>
 ```
  
*_Declaração de bloco, sintaxe do CSS:_*  
```
Selector >>> img {
              width: 300px;   <<< Declaração do bloco
            }
```
  
**Comentários no CSS**  
*_Usamos o modelo: ```/* Corpo do comentário */```._*