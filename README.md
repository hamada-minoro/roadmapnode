# Apostila Completa: APIs com Node.js e TypeScript

## Etapa 1: Fundamentos de Programação com JavaScript

### Objetivo
Aprender os conceitos básicos de programação usando JavaScript puro, desenvolvendo o raciocínio lógico necessário para programar APIs futuramente.

### Conteúdo

#### 1. Variáveis e Tipos Primitivos
- `var`, `let`, `const`
- Tipos: `string`, `number`, `boolean`, `null`, `undefined`
```js
let nome = "João";
const idade = 30;
let ativo = true;
```

#### 2. Operadores
- Aritméticos: `+`, `-`, `*`, `/`, `%`
- Comparação: `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
- Lógicos: `&&`, `||`, `!`

#### 3. Controle de Fluxo
- `if`, `else if`, `else`
```js
if (idade > 18) {
  console.log("Maior de idade");
} else {
  console.log("Menor de idade");
}
```

- `switch`
```js
switch(dia) {
  case 'segunda':
    console.log("Início da semana");
    break;
  default:
    console.log("Outro dia");
}
```

#### 4. Laços de Repetição
- `for`
- `while`
- `do...while`
```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

#### 5. Arrays e Objetos
```js
let numeros = [1, 2, 3];
let pessoa = { nome: "Ana", idade: 25 };
```

- Métodos de array: `map`, `filter`, `reduce`
```js
let dobrados = numeros.map(n => n * 2);
```

#### 6. Funções
- Declaração
- Expressão
- Arrow function
```js
function soma(a, b) {
  return a + b;
}

const subtrai = (a, b) => a - b;
```

#### 7. Escopo e `this`
- Escopo de função vs escopo de bloco
- Como `this` funciona em funções tradicionais e arrow functions

### Exercício Final
Criar um script JS que:
- Armazena uma lista de usuários
- Permite adicionar, listar e remover usuários com `prompt()` e `console.log()`

---

## Etapa 2: Fundamentos de TypeScript

### Objetivo
Adicionar tipagem estática ao JavaScript para aumentar a segurança e previsibilidade do código.

### Conteúdo

#### 1. Instalação e configuração
- Instalar TypeScript globalmente: `npm install -g typescript`
- Criar arquivo `tsconfig.json`: `tsc --init`

#### 2. Tipos Primitivos Tipados
```ts
let nome: string = "Lucas";
let idade: number = 20;
let ativo: boolean = true;
```

#### 3. Arrays e Objetos Tipados
```ts
let numeros: number[] = [1, 2, 3];
let pessoa: { nome: string; idade: number } = {
  nome: "Maria",
  idade: 30,
};
```

#### 4. Union e Intersection Types
```ts
let resultado: string | number;
resultado = 10;
resultado = "ok";

type Pessoa = { nome: string };
type Funcionario = Pessoa & { cargo: string };
```

#### 5. Type Alias e Interface
```ts
type Usuario = {
  nome: string;
  email: string;
};

interface Produto {
  nome: string;
  preco: number;
}
```

#### 6. Funções Tipadas
```ts
function somar(a: number, b: number): number {
  return a + b;
}
```

#### 7. Enums e Literais
```ts
enum Status {
  Ativo = "ativo",
  Inativo = "inativo"
}

let situacao: Status = Status.Ativo;
```

#### 8. Generics Básico
```ts
function identidade<T>(valor: T): T {
  return valor;
}
```

#### 9. Compilador e tsconfig.json
- `target`, `strict`, `noImplicitAny`, `outDir`
- Compilar: `tsc`

#### 10. Trabalhando com módulos
```ts
export function saudacao(nome: string): string {
  return `Olá, ${nome}`;
}

import { saudacao } from "./utils";
```

### Exercício Final
Criar uma aplicação TypeScript que:
- Possui uma função de cadastro de usuários
- Valida tipos com `interface` ou `type`
- Imprime os dados com funções tipadas

---

## Etapa 3: Node.js com TypeScript

### Objetivo
Aprender a rodar código TypeScript no Node.js e organizar projetos backend.

### Conteúdo

#### 1. Introdução ao Node.js
- O que é o Node
- `npm init` e estrutura de projeto

#### 2. Executando TypeScript com Node
- Instalar `typescript`, `ts-node`, `nodemon`
```bash
npm install -D typescript ts-node nodemon
```

#### 3. Criando scripts com `ts-node`
```json
"scripts": {
  "dev": "nodemon src/index.ts"
}
```

#### 4. Módulos
- Import e export ES6
```ts
import { soma } from "./utils";
```

#### 5. Estrutura recomendada de projeto
```
src/
├── utils/
├── services/
├── index.ts
```

### Exercício Final
Criar um script em TS que recebe dados de um JSON e imprime no terminal um relatório formatado.

(continua nas próximas etapas...)