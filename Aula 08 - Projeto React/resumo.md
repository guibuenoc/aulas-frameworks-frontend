# Aula 08 - Projeto React

## Introdução

Nesta aula foi feita uma revisão de JavaScript e, em seguida, foi apresentado o React como biblioteca para construir interfaces por meio de componentes. A ideia principal foi entender como a interface é descrita com JSX, dividida em componentes, alimentada com props e atualizada de forma eficiente pelo Virtual DOM.

## Conteúdos abordados

- Revisão de JavaScript: inserção no HTML, variáveis, tipos de dados, operadores, condicionais, repetições, funções, arrays e objetos
- Manipulação do DOM: seleção de elementos, alteração de conteúdo e eventos
- DOM e Virtual DOM
- JSX: sintaxe e expressões JavaScript dentro do HTML
- Componentes: criação, composição e reutilização
- Props: passagem de dados do componente pai para o filho
- Listas e keys: renderização de coleções de dados com `map()` e `filter()`
- Renderização condicional: `if`, `return` e operador ternário

## Exemplo de funcionamento

Um componente React é uma função que retorna JSX. Com props, o mesmo componente pode exibir conteúdos diferentes:

```jsx
function CardConceito({ titulo, descricao }) {
  return (
    <article>
      <h2>{titulo}</h2>
      <p>{descricao}</p>
    </article>
  );
}

function App() {
  return (
    <main>
      <CardConceito titulo="JSX" descricao="Sintaxe para descrever interfaces." />
      <CardConceito titulo="Props" descricao="Dados recebidos por componentes." />
    </main>
  );
}
```

Na renderização de listas, o `map()` transforma cada item de um array em um elemento, e a `key` ajuda o React a identificar cada item:

```jsx
const alunos = [
  { id: 101, nome: "Ana" },
  { id: 102, nome: "Bruno" },
  { id: 103, nome: "Caio" }
];

function ListaAlunos() {
  return (
    <ul>
      {alunos.map((aluno) => (
        <li key={aluno.id}>{aluno.nome}</li>
      ))}
    </ul>
  );
}
```

## Objetivo da aula

Entender como uma aplicação React é organizada em componentes, como os dados circulam entre eles por meio de props e como o React atualiza a interface, para depois aplicar esses conceitos em um projeto próprio.

---

## Slides da Aula

[Visualizar slides da Aula 08](./slides-aula-08.pdf)