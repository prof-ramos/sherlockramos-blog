---
sidebar_position: 11
title: Checklist de Deploy
---

# Checklist de Deploy na Vercel

Lista de verificações para garantir um deploy seguro e otimizado na Vercel.

## ✅ Pré-Deploy

### Configuração do Projeto
- [ ] `vercel.json` configurado com otimizações
- [ ] `.vercelignore` criado para excluir arquivos desnecessários
- [ ] Variáveis de ambiente configuradas (se necessário)
- [ ] URL e baseUrl corretos no `docusaurus.config.js`

### Validação Local
- [ ] `yarn build` executa sem erros
- [ ] `yarn postbuild` valida a criação do `build/index.html`
- [ ] `yarn lint:links` confirma que não há links quebrados
- [ ] `yarn serve` testa o build localmente

### Conteúdo e SEO
- [ ] Todos os posts do blog têm frontmatter completo
- [ ] Imagens otimizadas (WebP quando possível)
- [ ] Meta tags e descrições configuradas
- [ ] Sitemap.xml será gerado automaticamente

## ✅ Deploy

### Primeira Configuração na Vercel
- [ ] Repositório conectado ao GitHub
- [ ] Framework detectado como "Other" ou deixar automático
- [ ] Build Command: `yarn build`
- [ ] Output Directory: `build`
- [ ] Install Command: `yarn install --frozen-lockfile`
- [ ] Node.js versão 18+ selecionada

### Configurações de Performance
- [ ] Headers de cache configurados no `vercel.json`
- [ ] Headers de segurança aplicados
- [ ] Compressão Brotli/Gzip habilitada (automática)
- [ ] Edge caching configurado para assets

### Monitoramento
- [ ] Build logs verificados por erros
- [ ] Lighthouse score > 90 (Performance, Accessibility, SEO)
- [ ] Teste de velocidade realizado
- [ ] Analytics configurado (opcional)

## ✅ Pós-Deploy

### Validação em Produção
- [ ] Site carrega corretamente na URL da Vercel
- [ ] Navegação entre páginas funcionando
- [ ] Blog posts carregando com formatação correta
- [ ] Busca funcionando (se configurada)
- [ ] Responsividade testada em dispositivos móveis

### SEO e Indexação
- [ ] `robots.txt` acessível
- [ ] `sitemap.xml` acessível e válido
- [ ] Meta tags verificadas com ferramentas SEO
- [ ] Google Search Console configurado (opcional)

### Configuração de Domínio (se aplicável)
- [ ] Domínio personalizado configurado
- [ ] SSL/TLS funcionando (automático na Vercel)
- [ ] Redirecionamentos configurados (www vs não-www)
- [ ] DNS propagado completamente

## 🔧 Comandos Úteis

```bash
# Build e validação local
yarn vercel:build

# Validar links
yarn lint:links

# Deploy preview (CLI)
vercel

# Deploy para produção (CLI)
vercel --prod

# Desenvolvimento local simulando Vercel
yarn vercel:dev
```

## 🚨 Resolução de Problemas Comuns

### Build Falha
- Verificar logs no dashboard da Vercel
- Testar `yarn build` localmente
- Verificar versão do Node.js
- Confirmar que dependências estão instaladas

### Links Quebrados
- Executar `yarn lint:links`
- Verificar paths relativos vs absolutos
- Confirmar estrutura de pastas do `docs/` e `blog/`

### Performance Lenta
- Verificar tamanho das imagens
- Revisar configurações de cache no `vercel.json`
- Analisar com Lighthouse
- Verificar se assets estão sendo servidos via CDN

### Problemas de SEO
- Validar `sitemap.xml` e `robots.txt`
- Verificar meta tags nas páginas
- Confirmar estrutura de URLs
- Testar com Google Rich Results Test