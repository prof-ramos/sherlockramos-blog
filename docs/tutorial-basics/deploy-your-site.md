---
sidebar_position: 5
---

# Faça o deploy do seu site

O Docusaurus é um **gerador de site estático** (também chamado de **[Jamstack](https://jamstack.org/)**).

Ele compila seu site como **arquivos estáticos de HTML, JavaScript e CSS**.

## Faça o build do site

Gere seu site **para produção**:

```bash
npm run build
```

Os arquivos estáticos são gerados na pasta `build`.

## Publique seu site

Teste seu build de produção localmente:

```bash
npm run serve
```

A pasta `build` será servida em [http://localhost:3000/](http://localhost:3000/).

Agora você pode publicar a pasta `build` **quase em qualquer lugar**, com facilidade e **gratuitamente** ou a custo muito baixo (leia o **[Guia de Deploy](https://docusaurus.io/docs/deployment)**).
