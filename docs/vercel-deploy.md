---
sidebar_position: 10
---

# Deploy na Vercel

Este projeto é um site estático do Docusaurus. A Vercel pode construir e publicar automaticamente a partir do GitHub.

## Configuração do Projeto
- Framework: "Other" (ou detectado automaticamente)
- Node.js: 18+
- Install Command: `yarn`
- Build Command: `yarn build`
- Output Directory: `build`

## Como Atualizar o Deploy
- Via Git: cada push na branch principal (ou PR) dispara um build na Vercel.
- Via Dashboard: no projeto, clique em "Deployments" → "Redeploy" para reexecutar o último build.
- Via PR: cada PR gera um Preview Deployment com URL única para revisão.

## Variáveis de Ambiente
- Este site é estático e não requer segredos por padrão. Se adicionar integrações, configure em Project Settings → Environment Variables e faça "Redeploy".

## Dicas
- Verifique logs do build em Deployments → Logs.
- Se mudar `docusaurus.config.js` (URL/baseUrl), ajuste também as configurações do domínio na Vercel.
- Rollback: promova um deployment anterior com "Promote to Production".

## CLI (opcional)
- Instale: `npm i -g vercel`
- Login: `vercel login`
- Deploy Preview: `vercel`
- Produção: `vercel --prod`

