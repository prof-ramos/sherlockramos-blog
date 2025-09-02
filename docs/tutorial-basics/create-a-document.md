---
sidebar_position: 2
---

# Crie um Documento

Documentos são **grupos de páginas** conectadas por:

- uma **sidebar**
- **navegação anterior/próximo**
- **versionamento**

## Crie seu primeiro doc

Crie um arquivo Markdown em `docs/hello.md`:

```md title="docs/hello.md"
# Hello

This is my **first Docusaurus document**!
```

Um novo documento estará disponível em [http://localhost:3000/docs/hello](http://localhost:3000/docs/hello).

## Configure a Sidebar

O Docusaurus **cria automaticamente uma sidebar** a partir da pasta `docs`.

Adicione metadados para customizar o rótulo e a posição na sidebar:

```md title="docs/hello.md" {1-4}
---
sidebar_label: 'Hi!'
sidebar_position: 3
---

# Hello

This is my **first Docusaurus document**!
```

Também é possível criar a sidebar explicitamente em `sidebars.js`:

```js title="sidebars.js"
export default {
  tutorialSidebar: [
    'intro',
    // highlight-next-line
    'hello',
    {
      type: 'category',
      label: 'Tutorial',
      items: ['tutorial-basics/create-a-document'],
    },
  ],
};
```
