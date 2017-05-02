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

## removeFromObjectArray (arrayToSearch: array, key: string: termToRemove: string)

Remove um valor dentro de uma array retornando uma nova array

Exemplo:

```javascript
var minhaArray = [
  {id: 1, nome: ‘maça’},
  {id: 1, nome: ‘maça’}, 
  {id: 2, nome: ‘uva},
];

SQ.removeFromObjectArray(minhaArray, “id”, 2);
//retorna [{id: 1, nome: ‘maça’}]
```

## addClass (className: string)

Adiciona uma classe ao elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“p”).addClass(“.negrito”);
```

## removeClass (className: string)

Remove uma classe ao elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“p”).removeClass(“.negrito”);
```

## toggleClass (className: string)

Adiciona se o elemento não estiver com a classe e remove a classe se o elemento já estiver com a classe setada.

Exemplo:

```javascript
SQ(“p”).toggleClass(“.negrito”);
```

## on (eventName: string, ontrigger: Function)

Adiciona um evento a um elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“#btnSalvar”).on(“click”, function(){
  Alert(‘ola eu sou um botão!’);
});
```

## off (eventName: string)

Remove um evento que foi adicionado ao listener do elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“#btnSalvar”).off(“click”);
```

## remove (selector?: string )

Remove o elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“#container”).remove(“p”);
```
OU
```javascript
SQ(“p”).remove();
```
