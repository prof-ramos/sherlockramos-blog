---
sidebar_position: 1
---

# Gerencie versões da documentação

O Docusaurus pode gerenciar múltiplas versões da sua documentação.

## Crie uma versão dos docs

Publique a versão 1.0 do seu projeto:

```bash
npm run docusaurus docs:version 1.0
```

A pasta `docs` será copiada para `versioned_docs/version-1.0` e `versions.json` será criado.

Sua documentação agora terá 2 versões:

- `1.0` em `http://localhost:3000/docs/` para os docs da versão 1.0
- `current` em `http://localhost:3000/docs/next/` para a **documentação futura, ainda não lançada**

## Adicione um seletor de versão

Para navegar entre versões, adicione um seletor de versões.

Modifique o arquivo `docusaurus.config.js`:

```js title="docusaurus.config.js"
export default {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: 'docsVersionDropdown',
        },
        // highlight-end
      ],
    },
  },
};
```

O seletor de versão aparecerá na sua navbar:

![Docs Version Dropdown](./img/docsVersionDropdown.png)

## Atualize uma versão existente

É possível editar documentos versionados em suas respectivas pastas:

- `versioned_docs/version-1.0/hello.md` atualiza `http://localhost:3000/docs/hello`
- `docs/hello.md` atualiza `http://localhost:3000/docs/next/hello`
