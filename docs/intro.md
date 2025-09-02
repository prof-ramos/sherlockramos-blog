---
sidebar_position: 1
---

# Introdução ao Tutorial

Vamos conhecer o **Docusaurus em menos de 5 minutos**.

## Primeiros passos

Comece **criando um novo site**.

Ou **experimente o Docusaurus agora** em **[docusaurus.new](https://docusaurus.new)**.

### O que você vai precisar

- [Node.js](https://nodejs.org/en/download/) versão 18.0 ou superior:
  - Ao instalar o Node.js, recomenda-se marcar todas as opções relacionadas a dependências.

## Gere um novo site

Gere um novo site Docusaurus usando o **template classic**.

O template clássico será adicionado automaticamente ao seu projeto após executar o comando:

```bash
npm init docusaurus@latest my-website classic
```

Você pode executar esse comando no Prompt de Comando, Powershell, Terminal ou qualquer terminal integrado do seu editor.

O comando também instala todas as dependências necessárias para rodar o Docusaurus.

## Inicie seu site

Execute o servidor de desenvolvimento:

```bash
cd my-website
npm run start
```

O comando `cd` troca o diretório atual. Para trabalhar com o site recém-criado, navegue até a pasta no terminal.

O comando `npm run start` compila o site localmente e o serve por um servidor de desenvolvimento em http://localhost:3000/.

Abra `docs/intro.md` (esta página) e edite algumas linhas: o site **recarrega automaticamente** e exibe suas mudanças.
