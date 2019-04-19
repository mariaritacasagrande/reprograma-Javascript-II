# Semana 7 - Java Script II
Turma 7 | Front-end | 2019 | Semana 7 | JavaScript II

![](https://d2v4zi8pl64nxt.cloudfront.net/javascript-seo/5948abfc0e2df5.02876591.gif)

Este é o material da semana 7 de front-end. Aqui você encontra pastas numeradas com os dias de aula que teremos.

Dentro de cada pasta estão os exercicios que vamos desenvolver ao longo da semana.

### Dúvidas
Para tirar dúvidas, leve para a sala de aula, mande mensagem para a professora ou abra um issue aqui no repositório.

### *Este é nosso indice completo de atividades:*

# Guia Rápido - revisão

* [Aula 1 - Revisão](#)
    *    [Variaveis](#)
         *    [Sobre Variaveis](#)
         *    [Escopo de variavel](#)
         *    [Tipos](#)
                *    [Numeros](#)
                *    [Strings](#)
                *    [Booleanos](#)
                *    [null e undefined](#)
        * [Conversão](#)
    *   [Condicionais](#)
        *   [Condicional - if / else](#)
            *   [Operador Condicional Ternário](#)   
        *   [Condicional - switch](#)
    *   [Laços de Repetiçõo](#)
        *   [for (para)](#)
        *   [do…while(faça … enquanto)](#)
        *   [while (enquanto)](#)
    * [Arrays](#)
    * [Funções](#)
    * [Objetos](#)
    

# JavaScript II

* [Aula 2 - While, Do While e For](#aula-1)
    * [While](#aula-1)
    * [Do While](#)
    * [For](#)
    * [Exercicios](#)

* [Aula 3 - Objetos](#)
    * [O que são Objetos?](#)
    * [Criando objetos](#)
    * [Acessando propriedades e métodos](#)
    * [Alterando e adicionando propriedades](#)
    *  [Deletando propriedades](#)
    
    
* [Aula 4 - Eventos](#)
    * [O que são eventos?](#))
    * [Como usar os eventos em JavaScript](#)
    * [Evento Inline](#)
    * [Usando evento externo](#)
    * [Exemplos](#)
        *   [onLoad ](#)
        *   [onChange](#)
        *   [onMouseOver e onMouseOut](#)
        *  [onmousedown, onmouseup e onclick](#)

* [Exercícios](#)
  
* [Para saber mais](#)


***
# Aula 1

## O básico da sintaxe de JavaScript 
*Um guia rápido e básico da linguagem JavaScript.*

### Variáveis
As variáveis são declaradas com a palavra chave var, como segue:
```
var i;
var sum;
```
Também é possível declarar varias variáveis com a mesma palavra chave var:
```
var i, sum;
```
E pode-se combinar a declaração da variável com sua inicialização:
```
var i = 0, j = 0, k = 0;
var nome = "Fulano";
```
Antes de usar uma variável em um programa JavaScript, você deve declará-la.

### Sobre Variaveis 

Existem três tipos de declarações em JavaScript.

**var**
Declara uma variável, opcionalmente, inicializando-a com um valor.
**let**
Declara uma variável local de escopo do bloco, opcionalmente, inicializando-a com um valor.
**const**
Declara uma constante de escopo de bloco, apenas de leitura.

### Escopo de Variavel
Quando você declara uma váriavel fora de qualquer função, ela é chamada de variável global, porque está disponível para qualquer outro código no documento atual. Quando você declara uma variável dentro de uma função, é chamada de variável local,  pois ela está disponível somente dentro dessa função.

JavaScript antes do ECMAScript 6 não possuía escopo de declaração de bloco; pelo contrário, uma variável declarada dentro de um bloco de uma função é uma variável local (ou contexto global) do bloco que está inserido a função. Por exemplo o código a seguir exibirá 5, porque o escopo de x está na função (ou contexto global) no qual x é declarado, não o bloco, que neste caso é a declaração if. 

```
if (true) {
  var x = 5;
}
console.log(x);  // 5
```
Esse comportamento é alterado, quando usado a declaração let introduzida pelo ECMAScript 6.

```
if (true) {
  let y = 5;
}
console.log(y);  // ReferenceError: y não está definido
```

### Tipos
Os tipos em JavaScript podem ser divididos em duas categorias:

* tipos primitivos
* tipos de objeto

Os tipos primitivos incluem números, strings e valores booleanos.

Os valores especiais null e undefined são valores primitivos mas não são números, nem string e nem booleanos.

Qualquer valor em JavaScript que não seja número, string, booleano, null ou undefined é um objeto.

O typeof é um operador unário colocado antes de seu operando, o qual pode ser de qualquer tipo. Seu valor é uma string que especifica o tipo do operando.
```
typeof "foo"; // 'string'
typeof 123;   // 'number'
```
### Números

Ao contrário de muitas linguagens, JavaScript não faz distinção entre valores inteiros e valores em ponto flutuante. Todos os números em JavaScript são representados como valores em ponto flutuante.

Literais inteiros:
```
0
1
100
```
Literais em ponto flutuante:
```
3.14
100.09
0.33333
```
#### Strings

Para incluir uma string literal em um programa JavaScript, basta colocar os caracteres da string dentro de um par combinado de aspas simples ou duplas.
```
"" string de cumprimento zero
'teste'
"outro teste"
```
Para concatenar strings utilizamos o operador +.
```
var msg = "Ola " + "mundo"; // "Ola mundo"
msg = "Bem vindo ao meu blog, " + name;
```
A propriedade length determina o tamanho da string.
```
"palavra".length // 7
```
#### Booleanos
Os valores booleanos são representados por *true* e *false*.

#### null e undefined
A palavra chave *null* indica a ausência de um valor.

Mas também há um segundo valor que indica ausência de valor: *undefined*.

O valor indefinido (undefined) representa uma ausência mais profunda, é o valor de variáveis que não foram inicializadas.

### Conversão
A linguagem é muito flexível quanto aos tipos de valores que exige.

As variáveis em JavaScript são não tipadas. Você pode atribuir um valor de qualquer tipo a uma variável e, posteriormente, atribuir um valor de tipo diferente para a mesma variável.

JavaScript converte valores de um tipo para outro de forma livre.

Se um programa espera uma string, por exemplo, e você fornece um número, ele converte o número em string automaticamente.

Se você usa um valor não booleano onde é esperado um booleano, JavaScript converte adequadamente.

## Condicionais

Estruturas condicionais Javascript são como estruturas condicionais na maioria das linguagens de programação existentes, as utilizamos para verificar uma condição e definir se algo deve ou não acontecer.

Um bom exemplo disso, e que não tem nada a ver com programação, é a linguagem que utilizamos para nos comunicar, repare:

**Se o sol sair hoje, vou nadar.**

Temos uma condição (*se o sol sair hoje*) para executar uma ação (*vou nadar*) dependendo do resultado dessa condição. Se verdadeira, a ação é executada.

### Condicional - if / else
A estrutura condicional permite avaliar uma condição e, a partir dela, executar diferentes linhas de código. 

 ![](https://arquivo.devmedia.com.br/naoexclusivo/EduardoSpinola/Documentacao/ifelse/img/if.png)

```
if (n == 1) {
    // executa este bloco if
} else if () {
    // executa este bloco else if
} else {
    // executa este bloco else
}
```

#### Operador Condicional Ternário

É possível obter resultados semelhantes usando o operador condicional ternário condition ? expr1 : expr2.

```
resultado = (a > b) ? "a é maior que b" : "b é maior que a";
```
O código acima é equivalente ao de baixo:
```
if (a > b) {
    resultado = "a é maior que b";
} else {
    resultado = "b é maior que a";
}
```

### Condicional - switch
A estrutura condicional switch permite executar um bloco de código diferente de acordo com cada opção (cada case) especificada. Seu uso é indicado quando os valores a serem analisados nessas condições são pré-definidos.

```
switch(action) {
    case 'draw':
        drawit();
        break;
    case 'eat':
        eatit();
        break;
    default:
        donothing();
}
```

## Laço de Repetição

Laços oferecem um jeito fácil e rápido de executar uma ação repetidas vezes.

### for (para)
Um laço for é repetido até que a condição especificada seja falsa.

```
for (var i = 0; i < 5; i++) {
    //  Vai executar 5 vezes
}
```

### do...while (faça ... enquanto)
A instrução do...while repetirá até que a condição especificada seja falsa.

```
do
  declaracao
while (condicao);
```

### while (enquanto)
Uma declaração while executa suas instruções, desde que uma condição especificada seja avaliada como verdadeira. Segue uma declaração while: 
```
while (condicao)
  declaracao
```

### Arrays
Em JavaScript, arrays são um tipo especial de objeto que representam um conjunto ordenado de valores numerados.
```
var a = new Array();
a[0] = "dog";
a[1] = "cat";
a[2] = "hen";
a.length // 3
```
Uma forma mais conveniente de utilização de um array, na verdade a mais usada:
```
var a = ["dog", "cat", "hen"];
a.length // 3
```
### Funções

Uma função é um objeto que tem código executável associado. Uma função pode ser chamada para executar esse código executável e retornar um valor calculado.
```
function add(x, y) {
    var total = x + y;
    return total;
}
```
### Objetos
Um objeto em JavaScript é um conjunto não ordenado de valores nomeados.

Para criar um objeto vazio:
```
var obj = {};
```
Podemos criar um objeto com propriedades e métodos:
```
var obj = {
    name: "Carrot",
    "for": "Max",
    details: {
        color: "orange",
        size: 12
    }
}
```
E acessar as propriedades dessa forma:
```
obj.details.color      // orange
obj["details"]["size"] // 12
```
Funções também se comportam como objetos, veja o exemplo abaixo.
```
function Person(name, age) {
    this.name = name;
    this.age = age;
}
```
Instanciamos o objeto.
```
var obj = new Person("You", 36);
```
Alteramos os valores das propriedades.
```
obj.name = "Simon";
obj.name; // print 'Simon'
```
***
# Aula 2

![](https://boluda.com/files/objetos-javascript.png)

## O que são Objetos?

### Programação orientada a objetos

Objetos são como uma espécie de "super variáveis" que armazenam uma "coleção de valores" referenciados por nome, e que podem ser recuperados para serem utilizados em diversas outras partes de um programa. Em JavaScript praticamente qualquer tipo de dado é um objeto.

Cada item dessa "coleção de valores", é chamado de propriedade. Cada propriedade é composta por um par de "nome: valor". Quando uma propriedade armazena uma função, ela se torna o que chamamos de método.

## Criando objetos
Agora que já sabemos o que são objetos, vamos ver um pouco sobre como trabalhar com eles. Primeiramente vamos conhecer duas maneiras de se criar objetos.

### Notação literal

A maneira mais simples (e recomendável) de se criar objetos em JavaScript é usando o que chamamos de notação literal. Um objeto literal é composto por um par de chaves "{ }", que envolve uma ou mais propriedades. Cada propriedade segue o formato "nome: valor" e devem ser separadas por vírgula.

Para entender bem, nada melhor que um exemplo. Imagine que você vai criar um programa para organizar álbuns de vários cantores e bandas. Aqui vamos criar um objeto para armazenar informações sobre um álbum da banda Metallica, depois você pode praticar criando objetos com suas bandas favoritas. Então, mãos a obra!

```
let album = {
  title: "Metallica (Black Album)",
  released: 1991,
  showInfo: function() {
    alert("Título do álbum: " + this.title + "Lançado em: " + this.released);
  }
};
````

Conseguiu entender o que o código acima faz? Veja, é bem simples: primeiro criamos uma variável chamada "album". Depois criamos um objeto - note a abertura e fechamento das chaves: { e }. Então adicionamos duas propriedades e um método ao nosso objeto, que são: "title", "released" e "showInfo". Nas propriedades nós armazenamos o título e ano de lançamento do álbum, e no método temos uma função que irá exibir as informações sobre o álbum em uma "caixa de alerta" para o usuário. Mais fácil do que parece, não é mesmo?

### Função construtora

Outra maneira de criar objetos em JavaScript é utilizando uma função construtora. Se quisermos criar o mesmo objeto que criamos anteriormente, só que usando uma função construtora para isso, basta escrever o seguinte código:

```
let album = new Object();
album.title = "Metallica (Black Album)";
album.released = 1991;
album.showInfo = function() {
  alert("Título do álbum: " + this.title + "Lançado em: " + this.released);
};

```

Como você pôde notar, a sintaxe ficou um pouco diferente. Aqui devemos utilizar a palavra-chave new seguida pela função construtora Object() ao invés de abrir e fechar chaves. Depois nós adicionamos as propriedades e métodos utilizando album.title, album.released e album.showInfo e atribuimos os valores à elas ao invés de colocar os pares de "nome: valor".

### Acessando propriedades e métodos

Após ter criado um objeto, você vai precisar acessar os valores que ele armazena. Podemos acessar (ou se preferir: "recuperar") os valores guardados em um objeto, de duas maneiras: utilizando notação de ponto ou notação de colchetes. Veja um exemplo:
```
// notação de ponto
album.title // Retorna: Metallica (Black Album)
 
// notação de colchetes
album["title"] // Retorna: Metallica (Black Album)

```

Repare que no código acima, acessamos a mesma propriedade de duas maneiras diferentes. Geralmente é recomendável que você utilize a notação de ponto - album.title - por ser mais simples de ler e escrever.

Como os métodos são funções, você deve adicionar um par de parênteses - () - quando for acessá-los. Fora isso, nada de diferente. Veja no exemplo abaixo:

```
// notação de ponto
album.showInfo() // Exibe alerta:
// Título do álbum: Metallica (Black Album) Lançado em: 1991
 
// notação de colchetes
album["showInfo"]() // Exibe alerta:
// Título do álbum: Metallica (Black Album) Lançado em: 1991

```

### Alterando e adicionando propriedades

#### Alterando

Vez por outra vamos precisar alterar os valores armazenados nas propriedades de nossos objetos. Fazer isso também é bem tranquilo. Basta acessar a propriedade que deseja alterar, utilizando a notação de ponto que acabamos de conhecer, e atribuir o novo valor à ela. Quer um exemplo?
```
album.title = "Powerslave";
album.released = 1984;
```

O que aconteceu no código acima? Isso mesmo. Alteramos o título do álbum e o ano de lançamento. Agora nosso objeto armazena informações sobre um outro álbum de outra banda.

Para fixar, antes de prosseguir a leitura (supondo que você esteja lendo e digitando os códigos para treinar), altere os valores de title e released para Metallica (Black Album) e 1991 novamente.

#### Adicionando

Bom, agora que o título do nosso álbum voltou a ser "Metallica (Black Album)", que tal adicionar uma lista com os títulos das faixas do álbum? Sim, nós podemos adicionar novas propriedades e métodos aos nossos objetos mesmo após ter criado eles. A sintaxe é a mesma utilizada para alterar valores, que nós acabamos de ver.

Objetos podem armazenar qualquer tipo de dado válido em JavaScript, então, para criar uma lista com os títulos das faixas de nosso álbum, basta seguir o exemplo abaixo:
```
// Aqui adicionamos um array com os nomes de algumas faixas do álbum.
// Para praticar você pode adicionar todas as 12 faixas.
album.tracks = ["Enter Sandman", "Sad but True", "Holier Than Thou", "The Unforgiven"];
```

#### Deletando propriedades

Você pode deletar uma propriedade ou método de um objeto utilizando o operador delete seguido pelo nome da propriedade. Vamos testar?

```
typeof album.showInfo // "function"
 
delete album.showInfo // deleta o método showInfo
 
typeof album.showInfo // "undefined"
```
***
# Aula 3

## Eventos

![](https://codropspz-tympanus.netdna-ssl.com/codrops/wp-content/uploads/2015/04/blur_modal.gif)

## O que são eventos?
Os eventos são basicamente um conjunto de ações que são realizadas em um determinado elemento da página web, seja ele um texto, uma imagem, ou uma div, por exemplo. Muitas das interações do usuário que está visitando sua página com o conteúdo do seu site podem ser consideradas eventos.

Existe uma infinidade de eventos definidos para uso em JavaScript, abaixo podemos ver alguns dos principais e mais utilizados:

*onBlur*	remove o foco do elemento
*onChange*	muda o valor do elemento
*onClick*	o elemento é clicado pelo usuário
*onFocus*	o elemento é focado
*onKeyPress*	o usuário pressiona uma tecla sobre o elemento
*onLoad*	carrega o elemento por completo
*onMouseOver*	define ação quando o usuário passa o mouse sobre o elemento
*onMouseOut*	define ação quando o usuário retira o mouse sobre o elemento
*onSubmit*	define ação ao enviar um formulário

## Como usar os eventos em JavaScript

Existem diversas maneiras de se aplicar esses eventos aos elementos HTML, são elas:
* Inline
* Em um arquivo externo, usando um manipulador de eventos

### Evento Inline

Vamos ver um exemplo de como usar um evento de maneira inline em JavaScript. Dessa forma é preciso que tudo seja definido diretamente na tag do elemento, dessa forma:

*Listagem 1:* Eventos inline JavaScript
```
<!DOCTYPE html>
<html>
<head>
<title>Usando o evento onClick no Javascript</title>
</head>
<body>
 
<h1 onclick="this.innerHTML='Isso acontece quando usamos o evento onClick!'">Clique nesse link para testar o evento onClick!</h1>
 
</body>
</html>

```

No exemplo anterior nós vimos de maneira inline como utilizar o evento onclick.

## Usando evento externo
Para chamar um evento externo iremos precisar de um manipulador de eventos, nesse caso vamos usar o event listener que adiciona ou remove um evento sobre qualquer elemento. O Event Listener disponibiliza duas funções principais, são elas:

* addEvent - Adiciona uma função que será disparada quando ocorrer determinado evento no objeto.
* removeEvent - Remove um listener previamente adicionado em um objeto e retorna true em caso de sucesso.

Agora vamos ver um exemplo de como utilizar o Event Listener.

*Listagem 2:* Usando Event Listener
```
<script type="text/javascript" src="/path/to/event-listener.js"></script>
 
<form>
    <input type="text" name="a" />
    <input type="submit" />
</form>
 
<script type="text/javascript">
var f = document.forms[0];
addEvent(f, "submit", function( e ) { alert(f.a.value);return false; });
addEvent(f.a, "keyup", function( e ) { f.a.value=f.a.value.toUpperCase(); });
</script>
```

Dessa forma nosso formulário fica limpo e sem código JavaScript, sendo feita toda a validação de forma externa.

### Alguns exemplos
No exemplo 1 vimos como utilizar o evento onClick, abaixo iremos ver alguns mais exemplos de eventos e como usá-los.

### onLoad
O evento onload pode ser usado quando queremos que algo seja carregado junto com o carregamento da página.

*Listagem 3:* usando evento onLoad
```
<!DOCTYPE html>
<html>
<head>
<title>Usando eventos no Javascript</title>
</head>
<body onload="checkCookies()">
 
<script>
function checkCookies()
{
if (navigator.cookieEnabled==true)
    {
    alert("Cookies são permitidos")
    }
else
    {
    alert("Cookies não são permitidos")
    }
}
</script>
 
<p>Irá aparecer um alert dizendo se os cookies estão ou não liberados em seu navegador</p>
</body>
</html>

``` 

### onChange
O evento onChange é utilizado para que seja realizada determinada ação após alguma mudança. No exemplo abaixo iremos fazer essa mudança acontecer ao clicarmos fora do input text.

*Listagem 4:* Evento onChange
```
<!DOCTYPE html>
<html>
<head>
<title>Usando eventos no Javascript</title>
<script>
function myFunction()
{
var x=document.getElementById("fname");
x.value=x.value.toUpperCase();
}
</script>
</head>
<body>

 
Insira seu Nome: <input type="text" id="fname" onchange="myFunction()">
<p>
Ao clicarmos fora do input text o texto escrito nele ficará todo em caixa alta.</p>
 
</body>
</html>

```

### onMouseOver e onMouseOut
Esses eventos são responsáveis pelas ações que o usuário faz com o mouse, passando o mouse no elemento e tirando o mouse do elemento, respectivamente.

*Listagem 5:* Eventos onmouseover e onmouseout
```
<!DOCTYPE html>
<html>
<head>
<title>Usando eventos no Javascript</title>
</head>
<body>
 
<div onmouseover="mOver(this)" onmouseout="mOut(this)"
style="background-color:#D94A38;width:120px;height:20px;padding:40px;">Passe o mouse em mim</div>
 
<script>
function mOver(obj)
{
obj.innerHTML="Obrigado"
}
 
function mOut(obj)
{
obj.innerHTML="Passe o mouse em mim"
}
</script>
 
</body>
</html>
```

### onmousedown, onmouseup e onclick
Nesse exemplo iremos ver como trabalhar com o clique, o segurar o clique e o soltar do clique.

*Listagem 6:* Eventos onmousedown, onmouseup e onclick

```
<!DOCTYPE html>
<html>
<head>
<title>Usando eventos no Javascript</title>
</head>
<body>
 
<div onmousedown="mDown(this)" onmouseup="mUp(this)" style="background-color:#D94A38;width:90px;height:20px;padding:40px;">Clique aqui</div>
 
<script>
function mDown(obj)
{
obj.style.backgroundColor="#1ec5e5";
obj.innerHTML="Solte o clique"
}
 
function mUp(obj)
{
obj.style.backgroundColor="#D94A38";
obj.innerHTML="Obrigado"
}
</script>
 
</body>
</html>
```
