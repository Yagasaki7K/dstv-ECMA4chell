<p align="center">
  <a href="https://github.com/ApertureLaboratory">
    <img alt="Aperture Laboratories - Chell Series" src="https://github.com/ApertureLaboratory/4chell/blob/main/.github/ChellSeries.png" />
    </a>    
</p>

<p align="center">
  <h2 align="center">Introdução e Conceitos Práticos do ECMAScript (ES6) | IICA</h2>
  
  <p align="center">
    <br />
    <a href="#Sumário"><strong>Explore o sumário »</strong></a>
    <br />
    <br />
    <a href="https://github.com/Yagasaki7K/react4chell/issues">Reportar um problema</a>
    ·
    <a href="https://github.com/Yagasaki7K/react4chell/issues">Solicitar uma funcionalidade</a>
  </p>
</p>

## Sobre o Projeto
Nesse artigo você irá aprender os conceitos e a introdução básica de várias partes do ECMAScript, atualmente em sua versão 6 (ES6), conceitos como: Módulos; Async/Await; Promisses; Estrutura de Dados e mais... Esse será um artigo completo contendo **28** tópicos - até a última atualização, então salve esse artigo nos favoritos ou dê um star para rever os conceitos sempre que quiser mais tarde!

Esse artigo possuí o selo IICA - Introdução, Instalação e Criação do Aplicativo.

Esse artigo foi escrito baseado nos vídeos do [Filipe Morelli](https://www.youtube.com/channel/UCh1mfPKMBS0wZz_E5RRFQ_A) sobre o ECMAScript

## Sumário

- [Introdução](#introdução)
- [Instalação e Variáveis](#instalação-e-variáveis)
- [Operadores](#operadores)
- [Operadores Relacionais e Lógicos](#operadores-relacionais-e-lógicos)
- [Operadores de Bit à Bit](#operadores-de-bit-à-bit)
- [Operadores de atribuição](#operadores-de-atribuição)
- [Estrutura condicional](#estrutura-condicional)
- [Estrutura de repetição](#estrutura-de-repetição)
- [Funções](#funções)
- [Void](#void)
- [String](#string)
- [Number](#number)
- [Boolean](#boolean)
- [Math](#math)
- [Array](#array)
- [Objetos](#objetos)
- [Date](#date)
- [Eventos de tempo](#eventos-de-tempo)
- [RegEx](#regex)
- [Collections Sets](#collections-sets)
- [Strict Mode](#strict-mode)
- [Módulos em NodeJS](#módulos-em-nodejs)
- [Promises](#promises)
- [Tratamento de Erros](#tratamento-de-erros)
- [Classes em ES5](#classes-em-es5)
- [Classes](#classes)
- [Métodos](#métodos)
- [Herança](#herança)
- [Como contribuir?](#como-contribuir)

# Introdução
ECMAScript (ES) é uma especificação do Javascript, padronizada pela ECMAScript International. Ele é usado por aplicativos para habilitar o script do lado do cliente - ou do servidor usando NodeJS. A especificação é influenciada por linguagens de programação como PHP, Python, Java etc. Idiomas como JavaScript, JScript e ActionScript são regidos por esta especificação para evitar várias versões diferenciadas e uma padronização mais profissionalizada.

Antes de começarmos, saiba que é recomendado você ter o básico de Javascript, já que o ECMAScript em si, é uma evolução padronizada do Javascript. Se tiver conhecimentos em Orientações à Objeto é um bom avanço.

O Javascript foi desenvolvido por Brendan Eich, um desenvolvedor da Netscape Communications Corporation, em 1995. O Javascript começou a vida com o nome Mocha e foi chamado brevemente por LiveScript, antes de ser renomeado oficialmente para Javascript, o motivo desse nome era o hype do Java na época e decidiram se aprofundar nisso um pouco, surfar nesse hype, hoje, carregamos o fardo de ser comparados com Java o tempo inteiro, principalmente quem não conhece nada sobre as linguagens.

O Javascript é uma linguagem de script que é executada pelo navegador em conjunto com o HTML para desenvolver páginas com interações com seus usuários.

As implementações que o ES6 trás para o Javascript envolve novos recursos como:
- Suporte para constantes;
- Bloco de escopo;
- Funções lambda / Arrow Functions;
- Manipulação Estendida de Parâmetros;
- Templates de strings;
- Propriedades aprimoradas do objeto;
- Atribuição de desestruturação;
- Módulos;
- Classes;
- Iteradores;
- Funções Geradoras;
- Coleções (Map, Set);
- Novos métodos construídos para várias classes;
- Promises;

# Instalação e Variáveis
Um dos primeiros requisitos que você precisa ter instalado em sua máquina é o [NodeJS](https://nodejs.org/en/download/), um ambiente de desenvolvimento em Javascript que permite baixar módulos e executar código Javascript em um servidor. Com ele instalado você tem acesso ao `npm` ou se preferir, você pode instalar o Yarn após a instalação do NodeJS e usar o pacote `yarn` para instalar os módulos. Para dúvidas com Yarn, você pode [seguir a documentação](https://yarnpkg.com/getting-started/install) e seguir a configuração corretamente.

Verifique seu sistema operacional e instale a versão LTS do NodeJS (a mais segura e estável) e procure a maneira mais confortável de instalar o NodeJS a sua máquina.

Com ele instalado, você consegue criar novos projetos como React, NextJS e fazer a configuração e instalação de novos módulos em seu projeto.

Após instalado, é só ir até o terminal do seu sistema operacional e escrever `node -v` para ver se a versão do NodeJS instalada em seu computador está correta e se também, está instalado corretamente.

---

Sobre os comentários, existem duas maneiras de você comentar no seu código, o que é de suma importância, você pode utilizar `// comentários` para uma linha ou `/* comentários */` para múltiplas linhas.

Sobre as variáveis, existia apenas uma maneira de se declarar uma variável no ES5, que seria utilizando o `var NomedaVariavel = valor`, mas já com a versão do ES6 que é a mais reconhecida, você pode utilizar `const NomedaVariavel = valor` ou `let NomedaVariavel = valor` para declarar uma constante ou variável, vale lembrar que constantes são valores que são definidos apenas uma vez e não podem ser alterados, enquanto as variáveis são valores que podem ser alterados.

Atualmente a grande discussão do momento é quando usar `var` e quando usar `let`. O `var` é uma variável de escopo global, então quando você chama ela dentro de uma função e exporta ela, ela consegue ser lida e agir naturalmente, enquanto o `let`, isso não funciona, já que ela é de escopo local, funciona apenas quando estiver rodando dentro de uma determinada função e depois ela "morre".

E para testar isso, nós vamos usar os termos práticos. Você pode criar um arquivo chamado `teste.js` e escrever o código abaixo:

```
var nome = 'João';
var sobrenome = 'Gabriel';

var nomeCompleto = nome + ' ' + sobrenome;
console.log(nomeCompleto)

```

ao executar esse arquivo, retornaremos o nome `João Gabriel` no console. Mas como executar ele? Inicialmente você pode utilizar o terminal do VSCode ou usar o próprio terminal do seu sistema e ir até a pasta, em seguida, você pede para o node executar o arquivo e o resultado dele mostrará no próprio terminal, para executá-lo, basta você escrever `node teste.js` e o resultado será impresso.

A maneira em que o código foi escrito, foi seguindo o padrão do ES5.

Já seguindo o padrão do ES6, usamos o exemplo para facilitar o entendimento do que é um `const` e `let`:

```
// Usando const
const PI = 3,14
console.log (PI) // 3,14

PI = 3,15 // ERRO - Não é possível alterar uma constante

// Usando let
var PI = 3,14
console.log (PI) // 3,14

function getMorePI() {
    let PILocal = PI + 3,15
    console.log (PILocal) // 6,29
}

console.log (PILocal) // ERRO - PILocal não foi definido

```

# Operadores
Operadores em Javascript são símbolos especiais que envolvem um ou mais operandos com a finalidade de produzir um determinado resultado.

Quais os operadores JavaScript?
Os operadores podem ser aritméticos como soma, subtração e divisão; de comparação como a igualdade; operadores sobre cadeias de caracteres como o de concatenação de strings e, por fim, operadores lógicos JavaScript como o ‘and’ e o ‘or’. Abaixo um exemplo de como utilizar operadores aritméticos como Adição, Subtração, Multiplicação, Divisão, Resto da divisão, Exponenciação, Incremento e Decremento

```
let x = 10
let y = 3

console.log(x + y) // 13 (Adição)
console.log(x - y) // 7 (Subtração)
console.log(x * y) // 30 (Multiplicação)
console.log(x / y) // 3.333 (Divisão)
console.log(x % y) // 1 (Resto da divisão)
console.log(x ** y) // 1000 (Exponenciação)
console.log(++x) // 11 (Incremento | x = x + 1)
console.log(--x) // 9 (Decremento | x = x - 1)

```

# Operadores Relacionais e Lógicos
Lorem

# Operadores de Bit à Bit
Lorem

# Operadores de atribuição
Lorem

# Estrutura Condicional
Lorem

# Estrutura de Repetição
Lorem

# Funções
Lorem

# Void
Lorem

# String
Lorem

# Number
Lorem

# Boolean
Lorem

# Math
Lorem

# Array
Lorem

# Objetos
Lorem

# Date
Lorem

# Eventos de tempo
Lorem

# RegEx
Lorem

# Collections Sets
Lorem

# Strict Mode
Lorem

# Módulos em NodeJS
Lorem

# Promises
Lorem

# Tratamento de Erros
Lorem

# Classes em ES5
Lorem

# Classes
Lorem

# Métodos
Lorem

# Herança
Lorem

## Como Contribuir

Contribuições fazem com que a comunidade open source cresça, evoluia e você tenha reconhecimento por ter ajudado em um projeto tão maravilhoso
Todas contribuições são **extremamente apreciadas e avaliadas**

1. Realize um Fork do projeto
2. Crie um branch com a nova feature (`git checkout -b feature/nome-do-artigo`)
3. Realize o Commit (`git commit -m 'Adicionado novo item na enciclopédia'`)
4. Realize o Push no Branch (`git push origin feature/nome-do-artigo`)
5. Abra um Pull Request

## Autores do Artigo

- **Anderson "Yagasaki" Marlon** - _Dev Front-end e Graduado no CC50 de Harvard_ - [@Yagasaki7k](https://twitter.com/Yagasaki)
- Contribuidores - [Lista de contribuidores](https://github.com/Yagasaki7K/react4chell/graphs/contributors)