---
sidebar_position: 1
---

# Crie uma Página

Adicione arquivos **Markdown ou React** em `src/pages` para criar uma **página independente**:

- `src/pages/index.js` → `localhost:3000/`
- `src/pages/foo.md` → `localhost:3000/foo`
- `src/pages/foo/bar.js` → `localhost:3000/foo/bar`

## Crie sua primeira página React

Crie um arquivo em `src/pages/my-react-page.js`:

```jsx title="src/pages/my-react-page.js"
import React from 'react';
import Layout from '@theme/Layout';

export default function MyReactPage() {
  return (
    <Layout>
      <h1>My React page</h1>
      <p>This is a React page</p>
    </Layout>
  );
}
```

Uma nova página estará disponível em [http://localhost:3000/my-react-page](http://localhost:3000/my-react-page).

## Crie sua primeira página Markdown

Crie um arquivo em `src/pages/my-markdown-page.md`:

```mdx title="src/pages/my-markdown-page.md"
# My Markdown page

This is a Markdown page
```

Uma nova página estará disponível em [http://localhost:3000/my-markdown-page](http://localhost:3000/my-markdown-page).
