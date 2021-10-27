## Vetores JS

### Declaração de um vetor/array:

```js
var vetor = []
```

### Atribuição de valores à um vetor/array:

```js
var vetor = ['valor0', 'valor1', 1234]
```

### Mostrando um valor de um array no console:
```js
console.log(vetor[1])//'valor1'
console.log(vetor[0])//'valor0'
console.log(vetor[3])//1234
```

### Mostrar o tamanho de um array:
```js
console.log(vetor.lenght) // 3
```


### Adicionar um item novo no array:

```js
vetor.push("mais um item") //['valor0', 'valor1', 1234, 'mais um item']
```


## Tipos de variáveis:

### Var
  - Variável que é definida globalmente, ou no escopo inteiro de uma função, independente do escopo.

### Let
  - Variável semelhante ao var, porém ela não é global e se limita ao seu escopo em que ela foi delcarada.

### const
  - Variável imutavel (não muda seu valor), uma vez definida, esse valor não é alterado, tem as mesmas características do let, não tem escopo global, se limita ao escopo que ela foi declarada.


## O que são Escopos:

  - Escopo é um bloco de código, da para identifica-los com uma abertura e fechamento de chave:

```js
{ // inicio do escopo

  // Qualquer código colocado aqui dentro vai ser do escopo, variáveis let e const aqui dentro, vao existir apenas aqui dentro

} // fim do escopo


// exemplo

{
  let a = 'umavariavel'
}

console.log(a) // erro pq a variável não foi definida


// exemplo 2

let a = 1

{
  let a = 2
}

console.log(a) // O console vai mostar 1


// Exemplo 3

let a = 1

{
  a = 2
}

console.log(a) // 2, agora mostra 2 pq não estamos criando uma nova variável, e sim mudando o valor da existente.


```


## O que é hoisting?

Vamos supor que queremos chamar uma variável antes de declarar ela, assim:

```js
    console.log(algumacoisa)
    var algumacoisa = 'A'
```
Quando o console executar, vai dizer que o algumacoisa foi declarada mas não tem nenhum valor atribuido, isso por que o javascript quando executa o código faz isso aqui por padrão:

```js
    var algumacoisa
    console.log(algumacoisa)
    algumacoisa = 'A'
```

Ele sempre vai jogar a declaração da variável para cima, e atribuição a ela aonde tecnicamente declaramos no código.

##
