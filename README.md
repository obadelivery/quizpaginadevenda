# Caminho de São Cipriano — Fluxo Completo (Quiz → Pop-up → Vendas)

Landing page interativa unificada em um único projeto.

## Fluxo do site

1. **Quiz** — Três perguntas sequenciais (arquivo original do quiz).
2. **Resultado intermediário** — Resumo da obra + botão para a página de vendas.
3. **Página de vendas (pop-up)** — Tela de boas-vindas com o botão **Adquirir agora** que leva para o link da InfinitePay.

Tudo roda em uma única página (SPA), sem recarregar o navegador.

## Executar localmente

```bash
npm install
npm run dev
```

Abra o endereço que o Vite mostrar no terminal (geralmente `http://localhost:3000`).

## Gerar versão de produção (para Vercel / GitHub)

```bash
npm run build
```

A pasta `dist` será gerada. É ela que você sobe na Vercel (ou configura o projeto para build automático).

## Deploy na Vercel

1. Suba este projeto no GitHub.
2. Na Vercel: **New Project** → importe o repositório.
3. Framework preset: **Vite**.
4. Build Command: `npm run build`
5. Output Directory: `dist`
6. Deploy.

## Alterar o link de compra

Abra `src/main.js` e altere a constante:

```js
const purchaseUrl = 'https://loja.infinitepay.io/ciprianopoderoso/wwd3652-privacy-nuds';
```

## Estrutura principal

- `src/main.js` — Todo o fluxo (quiz → resultado → página de vendas)
- `src/style.css` — Estilos responsivos completos
- `index.html` — Entrada do app
- `package.json` — Scripts de desenvolvimento e build

## Observações

- A imagem de fundo usa o caminho de armazenamento do projeto original. Se a imagem não carregar no deploy, substitua `saintImage` em `src/main.js` por uma URL pública ou coloque a imagem em `/public` e use um caminho relativo.
- O conteúdo é apresentado como material de caráter cultural, religioso e popular.
