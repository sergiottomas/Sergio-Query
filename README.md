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
No exemplo acima é removido dentro do elemento com ID "container" todos os elementos "p"

Para remover o elemento selecionado pelo SQ baste utilizar o remove desta forma:

```javascript
SQ(“p”).remove();
```

Todos os elementos "p" serão removidos.

## each (callback: Function)

Iterage com cada elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“p”).each(function(element, index){
  element.addClass(“negrito”);
});
```

## val (value: string)

Insere um valor no elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“#txtNome”).val(“Sergio de Souza Tomas”);
```

## text (text: string)

Insere um texto no elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“#btnEnviar”).text(“Enviar”);
```

## html (html: string)

Insere um html no elemento selecionado pelo SQ

Exemplo:

```javascript
SQ(“.msg_erro”).html(“<p>Houve um erro nesta operação</p>”);
```

## append (html: string | HTMLElement)

Insere um html no elemento selecionado pelo SQ ou uma String

Exemplo:

```javascript
SQ(“.msg_erro”).html(“<p>Houve um erro nesta operação</p>”);
```
Resultado:

```html
<div id=”container”>
  <p>Texto já existente</p>
  <p>Este é um texto</p>
</div>
```

## prepend (html: string | HTMLElement)

Insere um elemento dentro do elemento selecionado pelo SQ na ultima posição do indice

Exemplo:

```javascript
SQ(“#container”).append(“<p>Este é um texto</p>”);
```

Resultado:

```html
<div id=”container”>
  <p>Mais um texto</p>
  <p>Texto já existente</p>
  <p>Este é um texto</p>
</div>
```

## find (selector: string)

Seleciona um elemento após ser selecionado pelo SQ

Exemplo:
HTML:

```html
<div id=”container”>
  <p>Mais um texto</p>
  Página7
  <p>Texto já existente</p>
  <p>Este é um texto</p>
</div>
```
JS

```javascript
SQ(“#container”).find(“p”)
//resultado [<p>Mais um texto</p>, <p>Texto já existente</p>,<p>Este é um exto</p>]
```


