# Aula 09 - Projeto React 02

## Introdução

Nesta aula foi estudado como deixar uma aplicação React interativa e conectada a dados externos. O foco foi entender como o componente guarda informações com `useState`, como trabalha com formulários, como sincroniza efeitos com `useEffect`, como busca dados de APIs e como organiza a navegação entre páginas com React Router.

## Conteúdos abordados

- State e `useState`
- Diferença entre variável comum e estado
- Hooks no React
- Formulários e campos controlados
- Manipulação de eventos `onChange` e `onSubmit`
- `preventDefault()` em formulários
- `useEffect` e dependências
- Função de limpeza de um efeito
- Consumo de APIs com `fetch`
- Requisições `GET` e `POST`
- Tratamento de erros e cuidados com APIs
- React Router: `BrowserRouter`, `Routes`, `Route` e `Link`
- Parâmetros de rota com `useParams()`

## Exemplo de funcionamento

Um componente com `useState` guarda um valor e atualiza a tela sempre que ele muda:

```jsx
import { useState } from "react";

function Contador() {
  const [contador, setContador] = useState(0);

  return (
    <section>
      <p>Valor: {contador}</p>
      <button onClick={() => setContador(contador + 1)}>
        Incrementar
      </button>
    </section>
  );
}
```

Já o `useEffect` pode buscar dados de uma API quando o componente é exibido. O array vazio `[]` indica que o efeito roda na montagem do componente:

```jsx
useEffect(() => {
  async function carregar() {
    const resposta = await fetch("https://jsonplaceholder.typicode.com/posts");
    if (!resposta.ok) throw new Error("Erro na consulta");
    const dados = await resposta.json();
    setPublicacoes(dados);
  }
  carregar();
}, []);
```

## Objetivo da aula

Entender como uma aplicação React mantém estado, reage ao usuário, consome dados de APIs e organiza suas telas por rotas, para depois aplicar esses conceitos em um projeto próprio.

---

## Slides da Aula

[Visualizar slides da Aula 09](./slides-aula-09.pdf)
