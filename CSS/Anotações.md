# Referenciando o CSS  
External CSS:  
 * Método de *_link_*, basta adicionar no head da pagina a tag: `<link rel=¨stylesheet¨ href="styles.css">` lembrando que é necessário respeitar o caminho até o arquivo CSS. Para o HTML4 ou anterior, existe uma pequena variação: `<link rel="stylesheet" href="styles.css" type=¨text/css¨>`  
 A vantagem de usar o método externo é a facilidade de "linkar" varias páginas HTML em um único arquivo CSS. Lembrando, também, que é possivel usar diversos arquivos CSS em um mesmo projeto.
  *  Médoto *_@import_*, usado para anexar diversas páginas CSS em apenas uma que será usada no projeto, exemplo: ```**styles.css**
  @import url('/styles/layout.css');
  @impor url('/styles/buttons.css');

  **index.html**
    <head>
        <style> @import url("/css/styles.css"); </style>
  ```