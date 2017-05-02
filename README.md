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
var myArray = [“maça”, “uva”, “abacate”, “laranja”, “tomate”];
SQ.searchInArray(myArray, “uva”);
//retorna true
SQ.searchInArray(myArray, “ate”, true);
//retorna [“abacate”, “tomate”]
```

## removeFromArray (arrayToSearch: array, termToRemove: string)

Remove um valor dentro de uma array retornando uma nova array

Exemplo:

```javascript
var myArray = [“maça”, “uva”, “abacate”];
SQ.removeFromArray(myArray, “uva”);
//retorna [“maça”, “abacate”]
```
