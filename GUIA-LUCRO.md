# Guia para lucrar com o Cobre Certo

Este guia lista o que já está pronto no site e o que depende de ação manual sua (contas/aprovações).

## 1) Google Search Console (manual)
1. Acesse https://search.google.com/search-console
2. Adicione propriedade **Prefixo do URL**: `https://projectsbywell.github.io/cobre-certo/`
3. Verificação: use a tag HTML (descomente a meta `google-site-verification` no `index.html`, faça commit/push) ou outro método.
4. Envie o sitemap: `https://projectsbywell.github.io/cobre-certo/sitemap.xml`
5. Em "Inspeção de URL", peça indexação da home e das páginas principais.

## 2) Mais conteúdo (em andamento)
- Meta: 20-30 páginas úteis com intenção de busca clara.
- Já existem: 3 ferramentas + 14 guias + páginas legais.
- Próximas ideias: "modelo de contrato MEI simples", "como cobrar por hora vs projeto", "como fazer proposta comercial", "controle de clientes grátis", "como evitar calote", "DAS MEI o que é e como organizar" (informativo, com disclaimer).

## 3) AdSense (manual, depende de aprovação)
1. Crie conta em https://www.google.com/adsense
2. Adicione o site e coloque o código de verificação no `<head>` (há placeholder comentado no `index.html`).
3. Crie `ads.txt` na raiz com a linha fornecida pelo AdSense, ex: `google.com, pub-XXXXXXXXXXXXXXXX, DIRECT, f08c47fec0942fa0`
4. Só ative anúncios após aprovação. Não clique nos próprios anúncios.

## 4) Tráfego (manual/contínuo)
- Compartilhe guias úteis em comunidades de autônomos/MEI (grupos, Reddit BR, fóruns), sem spam.
- Use Search Console para ver queries com impressão e CTR baixo; melhore título/descrição.
- Crie links internos entre guias relacionados (já iniciado).
- Considere domínio próprio depois (melhora confiança).

## 5) Segurança nível Cloudflare (recomendado)
GitHub Pages fornece HTTPS, mas não aplica headers HTTP customizados do `_headers`.

### Opção A - Cloudflare Pages (grátis)
1. Acesse Cloudflare Dashboard > Pages > Connect to Git.
2. Selecione o repo `projectsbywell/cobre-certo`.
3. Build: nenhum (site estático). Output directory: `/` (raiz).
4. Deploy. O arquivo `_headers` será aplicado.
5. Opcional: ativar WAF, Bot Fight Mode, HSTS no dashboard.

### Opção B - Netlify
Similar: importar repo, publish directory `/`, `_headers` aplicado.

## Checklist técnico pronto no repo
- [x] HTTPS (GitHub Pages)
- [x] Meta CSP/referrer/nosniff/permissions-policy
- [x] `_headers` para Cloudflare/Netlify
- [x] `robots.txt` e `sitemap.xml`
- [x] Canonical/OG/Twitter/JSON-LD (home)
- [x] Páginas legais: Privacidade, Termos, Sobre
- [x] Favicon
- [x] 404
- [x] Ferramentas client-side reais
- [ ] Verificação GSC (ação manual)
- [ ] Conta/ad code AdSense (ação manual)
- [ ] Migração Cloudflare Pages para headers HTTP reais (ação manual)
- [ ] Domínio próprio (opcional)
