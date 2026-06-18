# Template de Landing Page — Estilo Editorial Luxury

Este é um template Astro de landing page one-page, com estilo editorial/luxo, responsivo, otimizado para negócios locais de beleza, estética e serviços premium.

## Como usar

1. Descompacte este arquivo em uma nova pasta.
2. Rode no terminal:
   ```bash
   npm install
   npm run dev
   ```
3. Abra `http://localhost:4321/` no navegador.
4. Edite `src/pages/index.astro` e a pasta `public/` conforme o guia em `INSTRUCOES-PERSONALIZACAO.md`.
5. Quando terminar:
   ```bash
   npm run build
   ```
   O site estático será gerado na pasta `dist/`.

## Estrutura de pastas

```
site-template/
├── src/pages/index.astro   # Página única com todos os placeholders
├── public/
│   ├── images/
│   │   ├── hero.jpg        # Foto principal da hero/header
│   │   └── galeria/
│   │       ├── cliente-01.jpg ... cliente-06.jpg
│   ├── videos/
│   │   └── sobre.mp4       # Vídeo curto da seção "Sobre"
│   └── favicon.ico
├── package.json
├── astro.config.mjs
└── INSTRUCOES-PERSONALIZACAO.md
```

## Tecnologias

- Astro 5
- CSS variáveis (sem frameworks CSS)
- Google Fonts: Bodoni Moda, Pinyon Script, Quattrocento Sans
- Schema.org / JSON-LD para SEO local

## Licença de uso

Uso exclusivo para criação de sites de clientes. Não redistribuir como template aberto.
