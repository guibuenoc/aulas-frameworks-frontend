# Aula 07 - Frameworks CSS

## Introdução

Nesta aula foi estudado o CSS como ferramenta para controlar a aparência e o layout das páginas web, indo além de cores e fontes. Em seguida, foi apresentado o conceito de framework CSS, que reúne padrões, classes e componentes prontos para acelerar o desenvolvimento de interfaces.

O foco foi entender a diferença entre escrever CSS manualmente e usar uma abordagem utility-first, como a do Tailwind CSS.

## Conteúdos abordados

- Estrutura básica do CSS (seletor, propriedade e valor)
- Formas de aplicação do CSS: in-line, interno e externo
- Propriedades essenciais: color, background-color, font-family, font-size, margin, padding, border, width, height, display, position, top, right, bottom, left e text-align
- Box model (content, padding, border e margin)
- Classes e IDs
- Flexbox (flex-direction, justify-content, align-items, flex-wrap e gap)
- Layouts responsivos
- O que é um framework CSS
- Problema do CSS manual
- Tailwind CSS e a abordagem utility-first
- Instalação do Tailwind (Play CDN e Tailwind CLI)
- Tailwind IntelliSense

## Exemplo de funcionamento

O mesmo estilo pode ser escrito de duas formas. Com CSS puro, cria-se uma regra separada:

```css
.botao {
  background: #2563eb;
  color: white;
  padding: 12px 24px;
  border-radius: 8px;
}
```

Com Tailwind, as classes utilitárias são aplicadas direto no HTML, sem criar regra CSS separada:

```html
<button class="bg-blue-600 text-white px-6 py-3 rounded-lg">
  Enviar
</button>
```

Cada classe representa uma responsabilidade: `bg-blue-600` define a cor de fundo, `px-6 py-3` define o espaçamento interno e `rounded-lg` define as bordas arredondadas.

## Objetivo da aula

Entender como o CSS controla a estrutura e a aparência das páginas, e como os frameworks CSS, especialmente o Tailwind CSS, ajudam a construir interfaces responsivas de forma mais rápida e padronizada.

---

## Slides da Aula

[Visualizar slides da Aula 07](./slides-aula-07.pdf)
