# Instruções de Personalização

Substitua todos os placeholders `{{...}}` no arquivo `src/pages/index.astro` e os arquivos de mídia em `public/` pelas informações do novo negócio.

## 1. Dados do negócio (placeholders no topo do HTML)

| Placeholder | O que preencher | Exemplo |
|-------------|-----------------|---------|
| `{{NOME_DO_NEGOCIO}}` | Nome oficial do negócio | `Studio Beleza Exemplo` |
| `{{NOME_PROPRIETARIA}}` | Nome da profissional/proprietária | `Nome da Profissional` |
| `{{TAGLINE_HERO}}` | Frase curta de destaque na hero | `O poder de uma mulher começa pelo olhar ✨` |
| `{{SOBRE_PARAGRAFO_1}}` | Primeiro parágrafo da seção Sobre | Texto pessoal sobre a profissional |
| `{{SOBRE_PARAGRAFO_2}}` | Segundo parágrafo da seção Sobre | Texto sobre experiência e cuidado |
| `{{CTA_FINAL_TEXTO}}` | Texto curto da seção final | `Entre em contato pelo WhatsApp...` |

## 2. Contato e links

| Placeholder | O que preencher | Exemplo |
|-------------|-----------------|---------|
| `{{URL_DO_SITE}}` | Domínio do novo site | `https://dominiqueneves.com.br` |
| `{{INSTAGRAM_LINK}}` | Link completo do Instagram | `https://www.instagram.com/seuinstagram/` |
| `{{WHATSAPP_LINK}}` | Link do wa.me com número e mensagem | `https://wa.me/5521999999999?text=Ol%C3%A1...` |
| `{{TELEFONE_LINK}}` | Número com código do país | `+5521999999999` |
| `{{TELEFONE_FORMATADO}}` | Número formatado para exibição | `(21) 99999-9999` |
| `{{GOOGLE_MAPS_LINK}}` | Link do Google Maps do endereço | `https://maps.google.com/?q=...` |
| `{{GOOGLE_MAPS_EMBED}}` | URL do iframe do Google Maps | `https://maps.google.com/maps?q=...&output=embed` |

> **Dica:** para gerar o link do WhatsApp, use um encoder de URL. A mensagem padrão é: `Olá, vim através do site e gostaria de mais informações!`

## 3. Endereço

| Placeholder | Exemplo |
|-------------|---------|
| `{{ENDERECO_RUA_NUMERO}}` | `Rua Exemplo, 123 - sala 456` |
| `{{BAIRRO}}` | `Bairro Exemplo` |
| `{{CIDADE}}` | `Rio de Janeiro` |
| `{{ESTADO}}` | `RJ` |
| `{{CEP}}` | `00000-000` |

## 4. Arquivos de mídia

Coloque os arquivos na pasta `public/` com os nomes exatos abaixo. Mantenha as dimensões recomendadas para não distorcer o layout.

### Hero / Sobre
- `public/images/hero.jpg` — foto principal da profissional ou do ambiente. Recomendado: **460×613 px** (retrato).
- `public/images/sobre-mim.jpg` — foto da seção Sobre. Recomendado: **520×693 px** (retrato).

### Galeria
Coloque de 1 a 6 fotos em `public/images/galeria/`:
- `cliente-01.jpg` a `cliente-06.jpg`
- Recomendado: **400×500 px** cada (retrato).
- Se quiser menos fotos, remova as tags `<img>` correspondentes em `src/pages/index.astro`.

### Favicon
- Substitua `public/favicon.ico` e `public/favicon.svg` pelos do novo negócio.

## 5. Depoimentos

Troque os placeholders:
- `{{CLIENTE_1}}` a `{{CLIENTE_5}}` pelos nomes reais.
- `{{DEPOIMENTO_1_TEXTO}}` a `{{DEPOIMENTO_5_TEXTO}}` pelos textos dos depoimentos.

## 6. Serviço

Este template foi otimizado para um único serviço principal: **Extensão de Cílios**.

Caso o novo negócio ofereça mais serviços, duplique o bloco do card em `src/pages/index.astro` e ajuste os textos. Se quiser manter apenas um serviço, edite apenas o título e a copy do card existente.

## 7. Horários de funcionamento

Ajuste os placeholders de horário na seção "Quando nos encontrar":
- `{{HORARIO_SEGUNDA}}` a `{{HORARIO_DOMINGO}}`

No Schema.org (JSON-LD no `<head>`), ajuste `{{SCHEMA_OPENING_HOURS}}` no formato:
```
Mo 08:00-18:00, Tu 08:00-19:00, We 08:00-18:00, Th 08:00-18:00, Fr 08:00-19:00, Sa 08:00-18:00
```

## 8. Cores (opcional)

As cores principais estão nas CSS variables no topo do arquivo:

```css
:root {
  --bg-primary: #f9f1f2;
  --bg-secondary: #f3e5e7;
  --bg-dark: #1a0508;
  --accent: #9e2a3e;
  --accent-light: #d4a5a5;
  --gold: #c9a961;
  --text-dark: #1a0508;
  --text-light: #f9f1f2;
}
```

Ajuste essas cores para a identidade visual do novo cliente.

## 9. Verificação antes do build

Antes de rodar `npm run build`, certifique-se de que:
- [ ] Nenhum `{{PLACEHOLDER}}` ficou sem substituir.
- [ ] Todos os arquivos de imagem existem em `public/`.
- [ ] Os links de WhatsApp, Instagram e Google Maps estão corretos.
- [ ] O endereço e telefone estão atualizados.
- [ ] Os horários de funcionamento estão corretos no Schema.org e na seção de horários.
- [ ] O favicon foi trocado.

## 10. Build e deploy

```bash
npm install
npm run build
```

A pasta `dist/` conterá o site pronto para upload em qualquer hospedagem estática.
