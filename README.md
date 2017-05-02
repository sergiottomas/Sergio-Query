# Sergio-Query
Biblioteca inspirada no JQuery para Browsers antigos como IE8

## SQ(selector: string)
Seleciona e retorna um elemento da arvore do DOM.

Exemplo:

```html
<div id=”container”>
  <p>Simples texto</p>
</div>

<script>
  SQ(“#container”); //Retorna: <div id="container"></div>
  SQ(“#container p”); //Retorna: <p>Simples texto</p>
</script>
```
