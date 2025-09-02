---
sidebar_position: 2
---

# Traduza seu site

Vamos traduzir `docs/intro.md` para francês.

## Configure o i18n

Modifique `docusaurus.config.js` para adicionar suporte ao locale `fr`:

```js title="docusaurus.config.js"
export default {
  i18n: {
    defaultLocale: 'en',
    locales: ['en', 'fr'],
  },
};
```

## Traduza um doc

Copie o arquivo `docs/intro.md` para a pasta `i18n/fr`:

```bash
mkdir -p i18n/fr/docusaurus-plugin-content-docs/current/

cp docs/intro.md i18n/fr/docusaurus-plugin-content-docs/current/intro.md
```

Traduza `i18n/fr/docusaurus-plugin-content-docs/current/intro.md` para francês.

## Inicie seu site localizado

Inicie seu site no locale francês:

```bash
npm run start -- --locale fr
```

Seu site localizado estará acessível em [http://localhost:3000/fr/](http://localhost:3000/fr/) e a página `Getting Started` estará traduzida.

:::caution

Em desenvolvimento, você pode usar apenas um locale por vez.

:::

## Adicione um seletor de idioma

Para navegar entre idiomas, adicione um seletor de locale.

Modifique o arquivo `docusaurus.config.js`:

```js title="docusaurus.config.js"
export default {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: 'localeDropdown',
        },
        // highlight-end
      ],
    },
  },
};
```

O seletor de idioma aparecerá na sua navbar:

![Locale Dropdown](./img/localeDropdown.png)

## Faça o build do site localizado

Gere o site para um locale específico:

```bash
npm run build -- --locale fr
```

Ou gere o site incluindo todos os locales de uma vez:

```bash
npm run build
```
