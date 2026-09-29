# Briefing · Design System 2 (design_system2.html)

## Objetivo
Design system vivo da confeitaria artesanal da Jhessica: tokens, tipografia, superfícies, componentes, layout, movimento e ícones, com modo claro ("Dia · Merengue") e modo escuro ("Noite · Ganache").
Referências principais: Asagiri (parallax, fluidez, Lenis + GSAP) e Nereo (hero escura dividida 7/5 com cards de vidro). Apoio: Clarix, Follow, Sable e Aura.

## Público e tom de voz
Clientes que encomendam bolos e doces para aniversários, casamentos e presentes. Tom caloroso, preciso e sem pressa: fala de tempo de forno, medidas e ingredientes, nunca de "experiência premium". Português do Brasil.

## Identidade visual
- Cores dia: papel #F6EFE4, creme #FBF6EE, cacau (texto) #2B1D17, caramelo #B8742F, caramelo escuro para texto #8F5520, frutas vermelhas #8E2F3C.
- Cores noite: ganache #140D0A, chocolate #1C130F, creme (texto) #F5EADB, caramelo #D9A45B, frutas vermelhas #C85A68.
- Fontes: Newsreader 300–500 com eixo óptico (títulos, itálico nos destaques; a Cormorant foi descartada porque solta o circunflexo de ê/â/ô), Hanken Grotesk (texto e rótulos), Archivo condensada 800 (faixas e cartazes), La Belle Aurore (anotações e assinaturas à mão).

## Guia de estilo das imagens (vale para TODAS)
Fotografia editorial de confeitaria artesanal, como num lookbook impresso de uma pequena confeitaria ou numa revista independente de gastronomia.
- Câmera: lente 50 mm para planos de mesa, 85 mm para detalhes; altura da mesa ou levemente acima (cerca de 30 graus).
- Luz dia: luz natural de janela lateral vinda da esquerda, manhã, sombras suaves e longas.
- Luz noite: uma única luminária de tungstênio quente vinda da direita, fundo caindo para marrom-chocolate quase preto.
- Cenário real: mesa de madeira antiga com marcas de faca, linho cru amassado, papel manteiga com vincos, boleira de cerâmica esmaltada creme feita à mão, talheres de latão gastos.
- Imperfeições naturais: migalhas, farinha espalhada, pingos de calda, cobertura levemente irregular, grão de filme leve.
- Mãos (quando houver): mãos reais de confeiteira, unhas curtas sem esmalte, pele com textura, avental de linho cru.
- Paleta: creme, cacau, caramelo, com acento de frutas vermelhas. Saturação natural, contraste suave.
- Proibido: texto, letras, logos, marcas d'água, desfoque de fundo artificial exagerado, brilho plástico, saturação alta, simetria perfeita, mãos deformadas.
- Formato: PNG. Proporção indicada em cada item.

## Itens e caminhos (salvar em assets/images/ds2/)
1. `assets/images/ds2/hero-noite.png` · 16:9 · Bolo alto de chocolate de três camadas com ganache brilhante escorrendo e framboesas frescas no topo, sobre boleira de cerâmica creme. O bolo fica no terço direito do quadro; os 55% da esquerda são espaço vazio escuro (parede e mesa na sombra), para receber texto. Luz noite.
2. `assets/images/ds2/hero-dia.png` · 16:9 · Mesma composição do item 1 (se possível use a imagem do item 1 como referência: mesmo bolo, mesmo ângulo, bolo no terço direito), agora com luz dia: toalha de linho clara, parede creme com a luz da janela desenhando um retângulo suave à esquerda. Nada estourado.
3. `assets/images/ds2/interludio-acucar.png` · 16:9 · Close de mãos polvilhando açúcar de confeiteiro com uma peneira pequena sobre um bolo simples, a nuvem fina de açúcar visível contra o fundo escuro. Luz lateral recortando o pó. Bolo no centro-direita.
4. `assets/images/ds2/produto-bolo-cenoura.png` · 4:5 · Bolo de cenoura brasileiro com calda de chocolate grossa e brilhante, uma fatia retirada mostrando o miolo laranja fofo, sobre papel manteiga. Luz dia.
5. `assets/images/ds2/produto-torta-limao.png` · 4:5 · Torta de limão siciliano com merengue maçaricado em picos irregulares, raspas de limão, um pedaço cortado ao lado com garfo de latão. Luz dia.
6. `assets/images/ds2/produto-brigadeiros.png` · 4:5 · Brigadeiros artesanais em forminhas de papel pardo, alguns com granulado belga, outros com cacau em pó, arrumados de forma irregular numa caixa de papelão kraft aberta. Luz dia.
7. `assets/images/ds2/produto-bem-casados.png` · 4:5 · Bem-casados embrulhados em papel crepom creme, amarrados com fita de algodão, um aberto mostrando o recheio de doce de leite e o açúcar da casquinha. Luz dia.
8. `assets/images/ds2/atelie-ingredientes.png` · 4:5 · Ingredientes sobre a mesa de madeira: ovos caipiras numa tigela de cerâmica, saco de farinha dobrado, bloco de manteiga no papel, favas de baunilha, um limão siciliano cortado, colher de pau com farinha. Luz dia.
9. `assets/images/ds2/processo-peneirar.png` · 3:4 · Mãos peneirando farinha numa tigela, a poeira de farinha visível num feixe de luz da janela. Luz dia.
10. `assets/images/ds2/processo-bater.png` · 3:4 · Mãos batendo claras em neve com um batedor de arame numa tigela de cerâmica, picos firmes, avental de linho ao fundo. Luz dia.
11. `assets/images/ds2/processo-assar.png` · 3:4 · Vista pela porta de vidro de um forno doméstico: duas formas redondas com massa crescendo, luz laranja do forno, reflexo sutil no vidro. Luz noite.
12. `assets/images/ds2/processo-confeitar.png` · 3:4 · Mãos com saco de confeitar aplicando buttercream em espirais num bolo sobre um prato giratório de ferro esmaltado. Luz dia.

## Textos
Escritos diretamente no design_system2.html (documentação, não há lista de itens em JSON).

## Status das imagens (29/09/2026)
Pendentes. O Gemini respondeu `503 MODEL_CAPACITY_EXHAUSTED` no Pro e no Flash. O design_system2.html já aponta para `assets/images/ds2/<nome>.webp` e mostra placeholders desenhados enquanto o arquivo não existe. Quando a foto chega, ela cobre o placeholder sem mudar o código.

Depois de gerar (lotes de 3: itens 1–3, 4–6, 7–9, 10–12), converter para WebP na raiz do projeto:

    python -c "from PIL import Image;import glob;[Image.open(f).convert('RGB').save(f[:-4]+'.webp',quality=82,method=6) for f in glob.glob('assets/images/ds2/*.png')]"

Conferir a hero nos dois temas: o bolo precisa ficar no terço direito (object-position 74% 50%), porque os cards de vidro flutuam por cima dele.
