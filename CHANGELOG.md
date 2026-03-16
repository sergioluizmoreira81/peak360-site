# Changelog — Peak360 Site

## v1.1.0 — 2026-03-15
### Migração para pipeline de build com Vite
- Removidos CDNs de Tailwind CSS, React e Babel do `index.html`
- Configurado Vite 5 + @vitejs/plugin-react como bundler
- Tailwind CSS compilado via PostCSS (não mais CDN em tempo real)
- React 18 e ReactDOM importados via npm, não via `<script>` externo
- Criados arquivos de configuração: `vite.config.js`, `tailwind.config.js`, `postcss.config.js`
- Componente principal movido para `src/App.jsx`
- Estilos globais e diretivas Tailwind em `src/index.css`
- Assets estáticos (logo, robots.txt, sitemap.xml) movidos para `public/`
- Adicionado `.gitignore` excluindo `node_modules/` e `dist/`
- Cloudflare Pages configurado: build command `npm run build`, output `dist/`
- Resultado: JS ~162 KB minificado, CSS ~18 KB purgado, sem warnings de produção

---

## v1.0.0 — 2026-03-01
### Lançamento inicial (CDN)
- Site institucional completo com React + Tailwind via CDN
- Seções: Header, Hero, Sobre, Serviços, Plataforma 360°, StoryMaker, Galeria, Contato, Footer
- Menu hambúrguer responsivo para mobile
- Paleta: preto / sky-400 / branco
- WhatsApp: (41) 99214-3374 com mensagem pré-preenchida
- Instagram: @peak.360
- Logo peak360.jpeg no header e hero
- Block `<noscript>` com conteúdo estático para indexação pelo Google
- SEO: meta description, keywords, robots, canonical, Open Graph, sitemap.xml, robots.txt
- Hospedagem: Cloudflare Pages (peak360.com.br)
- DNS configurado via Cloudflare

---

## Próximas evoluções previstas
- Galeria com fotos reais de eventos
- Seção de depoimentos de clientes
- Formulário de orçamento (nome, tipo de evento, data, cidade)
- Página de obrigado pós-formulário
- Google Analytics / Meta Pixel
- Favicon e Open Graph image personalizada
