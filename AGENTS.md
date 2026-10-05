# AGENTS.md — Jhessica Confeitaria Artesanal

Regras deste projeto para qualquer agente (Claude Code, Codex, Antigravity). O `CLAUDE.md` importa este arquivo; mantenha as regras gerais aqui.

## Projeto

- O que é: site da confeitaria Jhessica em Cozinha Saudável, vitrine de bolos e doces com pedido pela sacola enviado no WhatsApp.
- Cliente: Jhessica Confeitaria Artesanal
- Tipo: site — baixo (site de apresentação, sem login nem pagamento online)
- Público e tom dos textos: Gentil, acolhedor e caseiro.

## Stack

- Astro 7 (estático), TypeScript, CSS próprio com tokens (modo dia e noite), ícones Iconify
- App em: `jhess-site/` (os comandos rodam lá)
- Hospedagem: GitHub Pages de teste (https://jontinhaa.github.io/jhessica-site1/), deploy por `jhess-site/.github/workflows/deploy.yml`; produção.
- Usaremos a vercel futuramente para publicar de fato e usar um domínio .com

## Comandos

- Desenvolvimento: `cd jhess-site && npm run dev`
- Build: `cd jhess-site && npm run build` (roda também `scripts/checar-css-build.mjs`)

## Comandos de verificação

O pente-fino roda estes comandos, nesta ordem, antes de entregar. Todos precisam passar.

1. `cd jhess-site && npm run check`
2. `cd jhess-site && npm test`
3. `cd jhess-site && npm run build`

## Estrutura

- `jhess-site/src/data/` — `site.ts` (marca, contato, seções, menu) e `cardapio.ts` (produtos e preços)
- `jhess-site/src/components/` — `layout`, `sections`, `pedido`, `ui`
- `jhess-site/src/lib/pedido/` — lógica pura e testada (itens, preços, prazos, mensagem de WhatsApp)
- `jhess-site/src/scripts/` — sacola (localStorage), folha, tilt
- `jhess-site/src/styles/` — `tokens.css` e `global.css`
- `jhess-site/tests/` — `npm test` (node:test)
- `.briefing/` e `design_system1.html`, `design_system2.html` — direção de arte e design system de referência
- Convenções detalhadas e pendências de lançamento: `jhess-site/CLAUDE.md`

## Convenções

- Dependência nova só com justificativa no pedido e aprovação do usuário.
- Textos visíveis em português do Brasil, no tom definido acima.
- Movimento só com CSS nativo (sticky e scroll-driven animations), sem GSAP/Lenis, e sempre respeitando `prefers-reduced-motion`.
- Elemento com timeline `view()` não pode ter ancestral com `overflow: hidden` (o ancestral vira o contêiner da timeline e o progresso trava); usar `overflow: clip`.
- Preço sempre recalculado de `cardapio.ts`; promessa ao cliente (sem glúten, sem leite…) só com dado confirmado.
- Endereço completo de retirada nunca entra no repositório, só o bairro.
- Nunca prometer que um produto é seguro para celíacos.

## Design system

- Fonte da verdade: `jhess-site/src/styles/tokens.css`, `jhess-site/src/styles/global.css` e `design_system2.html`
- Use os tokens e as classes do design system; nada de cor, espaçamento, raio, sombra ou fonte fixos no código.
- Breakpoints: 1180 (menu), 1024 (hero), 860 (uma coluna, foto primeiro) e 640 (celular).

## Segurança e dados

- Nunca ler nem editar `.env`; os nomes das variáveis ficam em `.env.example`, sem valores reais.
- Segredo nunca vai para variável com prefixo público (`PUBLIC_`, `NEXT_PUBLIC_`, `VITE_`, `EXPO_PUBLIC_`).
- Nada de dado pessoal em log, URL, analytics ou commit.
- Formulários coletam só o necessário para a finalidade; nada de CPF ou data de nascimento "por garantia".
- Link para WhatsApp ou e-mail monta a mensagem no navegador; o site não guarda dados de clientes.
- Promessas do texto (prazos, preços, ingredientes, garantias) seguem o que o cliente confirmou.
- O endereço completo da Jéssica não entra no código nem no Git.

## Git

- Commits em Conventional Commits, em português (por exemplo `feat(pedido): adiciona resumo da sacola`).
- Não fazer commit nem push sem o usuário pedir.

## Escritório

- Ao fim de cada entrega, o pente-fino automático revisa as mudanças com os revisores e pede aprovação; correções só depois do "aplica".
- Só ajustes mecânicos (formatação, typo, import sem uso) são corrigidos sem perguntar.
- Achados que se repetem viram regra neste arquivo pela `/escritorio:retro`.
