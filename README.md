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

## trigger (eventName: string)

Dispara um evento no elemento selecionado pelo SQ.

Exemplo:

```javascript
SQ(“#btnFiltrar”).trigger(“click”);
```

## seachInArray (arrayToSearch: array, term: string, getArray: Boolean)

Procura um valor dentro de uma array retornando um Boolean ou uma Array

Exemplo:

```javascript
Var minhaArray = [“maça”, “uva”, “abacate”, “laranja”, “tomate”];
SQ.searchInArray(minhaArray, “uva”);
//retorna  true
SQ.searchInArray(minhaArray, “ate”, true);
//retorna  [“abacate”, “tomate”]
```