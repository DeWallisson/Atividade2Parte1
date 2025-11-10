# Atividade2 - Manipulação de String e Json.

## Questão 1 - Explique o que é JSON e por que ele se tornou tão popular para troca de dados entre aplicações.

JSON é um formato de texto leve e independente de qualquer linguagem, ele é utilizado para armazenar e transportar dados. Ele é praticamente suportado por todas as linguagens de programação como por exemplo: Python, Java, C#, etc. Podemos dizer que ele tem um formato de mudança de dados universal.
O JSON se tornou o formato padrão para troca de informações entre sistemas front end e back end tendo diversas vantagens. A estrutura é fácil de criar e compreender, facilitando o desenvolvimento e manutenção do texto. É mais fácil para as máquinas converterem a string JSON em objetos como também fazer o inverso, isso ajuda a ter um processamento mais rápido e também por ser independente de linguagem, ele funciona como uma "linguagem comum" que permite que diferentes sistemas se comuniquem de maneira eficiente.

## Questão 2 - Qual a diferença fundamental entre JSON.stringify() e JSON.parse()? Dê um exemplo prático de quando usar cada um.

Os métodos JSON.stringify() e JSON.parse() lidam com a conversão entre o formato de objeto do JavaScript e a string JSON, ou seja, JSON.stringify() converte um objeto JS em uma string JSON e o JSON.parse() faz exatamente o inverso, transforma uma string JSON em um objeto.

### Exemplo 1:

``` js
// Objeto JavaScript

    const usuario = {
    nome: "Júlia",
    idade: 25,
    sexo: "feminino"
};

// Usando JSON.stringify() para converter o objeto JS em uma string JSON

const usuarioJSON = JSON.stringify(usuario);
console.log(usuarioJSON);

// Saída esperada: '{"nome":"Júlia","idade":25,"sexo":"feminino"}'
```

### Exemplo 2:

``` js
// JSON.parse() para converter a string JSON de volta para um objeto JavaScript

const string = '{"nome":"Júlia","idade":25,"sexo":"feminino"}'; 
const usuarioObjeto = JSON.parse(string);

console.log(usuarioObjeto.idade);

// Saída: 25 (agora é um objeto nativo do JavaScript)
```

## Questão 3 - Considerando a string "JavaScript é baseada em ECMA Script", quais métodos você usaria para:
● Verificar se contém a palavra "Script";

● Remover a palavra "JavaScript" e gerar uma nova string;

● Substituir "baseada" por "tem origem"


Utilizando alguns métodos que o JavaScript oferece conseguimos resolver facilmente esses problemas.

str.includes("Script") é um método que procura exatamente essa sequência de caracteres na string.

``` js

let str = "JavaScript é baseada em ECMAScript";
str.includes("Script");
 
//Saída esperada: true

```

str.replace("JavaScript ", "") esse método encontra a primeira ocorrência de "JavaScript " e substitui por uma string vazia ("").

``` js

let str = "JavaScript é baseada em ECMAScript";
str.replace("JavaScript ", ""); 

//Saída esperada: "é baseada em ECMAScript"

```

Com o mesmo método str.replace vamos conseguir resolver o terceiro problema, mas com os parâmetros diferentes ("baseada", "tem origem") encontra a palavra "baseada" e a substitui pela palavra "tem origem".

``` js

let str = "JavaScript é baseada em ECMAScript";
str.replace("baseada", "tem origem"); 

//Saída esperada: "JavaScript é tem origem em ECMAScript"

```

## Questão 4 - Qual a vantagem de usar template strings (``) em vez de concatenação com + para criar strings complexas?

A principal vantagem da template string é que ela permite a inclusão direta de variáveis e expressões JavaScript que estejam dentro da string usando a sua sintaxe ${expressão}. O código fica muito mais limpo e legível, eliminando a necessidade de fechar e reabrir aspas e usar o operador + repetidamente.

### Exemplo 1:

``` js
let nome = 'Wallisson';
let nota = 7;

// Concatenação usando +
let mensagem = 'O aluno ' + nome + ' tirou a nota ' + nota + ' na prova.';

console.log(mensagem);
// Saída: O aluno Wallisson tirou a nota 7 na prova.

```

### Exemplo 2:

``` js
let nome = 'Wallisson';
let nota = 7;

// Template String usando a crases e ${}
let mensagem = 'O aluno ${nome} tirou a nota ${nota} na prova.';

console.log(mensagem);
// Saída: O aluno Wallisson tirou a nota 7 na prova.

```
