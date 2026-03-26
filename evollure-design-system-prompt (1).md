# IDENTIDADE VISUAL — Evollure Landing Pages

> **Este documento é o DNA visual completo da Evollure para criação de landing pages.**
> Qualquer IA que ler este documento deve gerar páginas com a identidade Evollure — não um template recolorido.
> O resultado deve ser indistinguível de algo feito por um estúdio de design premium.

---

## CONTEXTO DA MARCA

- **Nome:** Evollure
- **Wordmark:** "Evollure" em PP Neue Montreal Regular (weight 400), letter-spacing -1px. NUNCA em caixa alta. NUNCA em bold.
- **Ícone (Orbital Knot):** Três elipses rotacionadas (0°, 60°, 120°) com opacidade decrescente (100%, 65%, 35%) convergindo num ponto central sólido. SVG inline — NUNCA usar imagem.
- **Tagline:** IA aplicada a negócios
- **O que é:** AI Sales Agency com 3 produtos — Intelligence (análise de calls), Reach (SDR + CRM), Prospect (prospecção multicanal)
- **Tom de voz:** Direto. Pesado. Sem enfeite. Resultado > tecnologia. Nunca fale de IA como feature — fale do resultado que ela entrega.
- **Sensação:** "Isso é premium. Isso é sério. Essa empresa sabe o que faz."
- **O que NÃO parecer:** Template Framer/Webflow recolorido. LP genérica de SaaS. Site institucional tedioso. Página de vendas clickbait. Nada com cores de arco-íris.
- **Referência de energia:** A confiança do Linear + a ousadia do Vercel Ship + a elegância editorial cinematográfica da Academia Lendária + os posts originais da Evollure (renderizações 3D, figuras futuristas, xadrez, Porsche com plantas, tipografia bold com itálico ember)

---

## Stack Técnica

- Tailwind CSS para toda estilização (NUNCA criar arquivos .css separados exceto @keyframes)
- shadcn/ui como base quando aplicável, customizados via className
- Framer Motion para animações de scroll e micro-interações (ou CSS puro se preferir bundle menor)
- Todos os valores visuais definidos como TOKENS SEMÂNTICOS no tailwind.config
- NUNCA usar valores hardcoded — sempre tokens semânticos
- NUNCA usar cores/radius/sombras padrão do Tailwind — apenas tokens deste documento
- A IA que implementa é RESPONSÁVEL por criar SVGs originais e composições visuais únicas
- A paleta usa UMA cor accent (Ember #E8570F) + neutros Carbon. NÃO crie arco-íris.

---

## Setup Necessário

### Fontes

| Fonte | Uso | Importação |
|---|---|---|
| PP Neue Montreal Regular (400) | Logo/wordmark "Evollure" | CDNFonts: `https://fonts.cdnfonts.com/css/pp-neue-montreal` |
| PP Neue Montreal Bold (700) | Headlines hero, títulos de seção, números grandes | Mesmo import acima |
| PP Neue Montreal Bold Italic (700i) | Destaques em ember dentro de headlines | Mesmo import acima |
| IBM Plex Mono (400/500) | Labels, badges, dados, metadata, código | Google Fonts: `IBM+Plex+Mono:wght@400;500` |

### Libs adicionais

| Lib | Pra quê | Instalação |
|---|---|---|
| `framer-motion` | Animações de scroll e entrada | `npm i framer-motion` |

---

## A Alma da LP

Uma jornada dark e cinematográfica. Cada seção é um ato narrativo — com tensão, respiro e clímax visual. Tipografia pesada nos headlines, itálico ember nas palavras-chave, espaço negativo generoso. O visitante não lê a página — ele é conduzido por uma experiência. Dados como arma. Resultado como prova. Silêncio como luxo.

**Frase-guia:** "90% silêncio, 10% fogo."

---

## Decisões de Identidade

### RITMO E ESTRUTURA

#### Ritmo de Scroll
**O que:** Alternância rigorosa entre seções densas (com composições visuais narrativas) e seções de respiro (espaço negativo, tipografia grande, simplicidade). O scroll tem "atos" como um filme.
**Por que:** Contraste gera impacto. Monotonia gera abandono. A Evollure é cinematográfica — cada corte de seção é intencional.
**Como:** Alternância de fundos (void → carbon-900 → void), alternância de densidade (hero denso → social proof limpo → features denso → quote respiro → CTA clímax), alternância de layout (split → centralizado → assimétrico).
**Nunca:** Todas as seções com a mesma energia. Todas as seções com fundo idêntico. Seções empilhadas como slides de PowerPoint.

#### Layout Global
**O que:** Máximo 960px de conteúdo. Seções full-width com conteúdo contido. Split layouts no hero (texto esquerda, visual direita). Features alternadas (texto-visual, visual-texto). CTAs centralizados.
**Por que:** A Evollure é editorial — respeita margens, hierarquia e respiro como uma revista de design.
**Como:** Container max-width 960px. Padding lateral 32px. Padding vertical entre seções 80-120px. Seções de respiro com 160px+ de padding.
**Nunca:** Conteúdo colado na borda. Seções comprimidas sem respiro. Grid de 12 colunas com tudo preenchido.

#### Navegação
**O que:** Nav fixa no topo. Fundo transparente que ganha fundo solid (void com blur) ao scrollar. Logo Orbital Knot + wordmark "Evollure" à esquerda. Links mínimos à direita. CTA ember no canto direito.
**Por que:** Nav minimalista = premium. O conteúdo é o protagonista.
**Como:** Position fixed, backdrop-filter blur(12px), transição suave de transparente para var(--c900) com 80% opacity. Z-index alto. Height 64px.
**Nunca:** Nav robusta com muitos links. Mega-menus. Nav colorida. Nav que some e aparece de forma abrupta.

#### Transições entre Seções
**O que:** Divisores sutis — linha de 1px com gradiente que desaparece nas bordas (transparent → c700 → transparent). Mudança de fundo entre seções para criar "atos".
**Por que:** Continuidade visual sem interrupção brusca. O scroll flui como uma narrativa.
**Como:** Div de 1px com background linear-gradient. Ou mudança de background-color entre seções.
**Nunca:** Bordas grossas. Separadores decorativos. Transições de cor abruptas sem motivo.

### LINGUAGEM VISUAL

#### Tipografia
**O que:** PP Neue Montreal é a arma. Headlines em Bold (700) com tracking negativo (-0.8px a -2px). Números enormes. Palavras-chave em Bold Italic + cor ember. Corpo em Regular (400). Labels em IBM Plex Mono uppercase com letter-spacing 3px.
**Por que:** A Academia Lendária provou que Neue Montreal Bold com itálico nos destaques é imediatamente premium e reconhecível. O contraste entre peso 800 do título e peso 400 do corpo cria hierarquia brutal.
**Como:**
- `text-hero`: 42-56px, weight 800, letter-spacing -1px a -2px, line-height 1.1-1.2
- `text-section-title`: 28-36px, weight 800, letter-spacing -0.8px, line-height 1.2-1.3
- `text-section-subtitle`: 18-20px, weight 400, color c200, line-height 1.7
- `text-body`: 14-16px, weight 400, color c300, line-height 1.8
- `text-caption`: IBM Plex Mono, 9-10px, weight 500, uppercase, letter-spacing 3px, color ember ou c400
- `text-cta`: 14px, weight 700, letter-spacing -0.2px
- `text-number`: 48-72px, weight 800, letter-spacing -2px a -3px (números como arma visual)
- `text-highlight`: Bold Italic, color ember — ÚNICO recurso de ênfase nos headlines
**Nunca:** Fontes serif. Fontes decorativas. Neue Montreal em caixa alta para o logo. Fonte light/thin em headlines. Corpo em bold. Itálico sem ser ember.

#### Paleta de Cores
**O que:** Carbon (preto real) como fundação + Ember (#E8570F) como única cor quente. 90% carbon/cinzas, 10% ember. Ponto final.
**Por que:** Uma cor = identidade. Múltiplas cores = barulho. Linear usa só violeta. Supabase usa só verde. Evollure usa só ember.
**Como:** Ver tokens abaixo. Ember aparece APENAS em: CTAs primários, dados críticos, palavras-chave em itálico, núcleo do Orbital Knot, hovers ativos, badges de status.
**Nunca:** Ember como fundo de seções inteiras. Gradientes multicoloridos. Mais de uma cor accent. Ember em elementos decorativos sem propósito.

#### Geometria e Formas
**O que:** Cantos RETOS em botões e frames principais. Bordas de 1px em c700 para cards e containers. Sem border-radius em CTAs.
**Por que:** A Evollure é afiada, precisa, sem arredondamento desnecessário. Cantos retos comunicam seriedade e autoridade.
**Como:** border-radius 0px em botões e CTAs. Cards podem ter 2-4px máximo se necessário. Badges: border-radius 100px (pill). Inputs: 0px.
**Nunca:** Cantos arredondados grandes (16px+). Pill buttons. Glassmorphism. Neumorphism.

#### Profundidade e Efeitos
**O que:** Flat absoluto. Profundidade vem APENAS da hierarquia de cinzas (void → c900 → c800 → c700) e da opacidade. Sem sombras. Sem gradientes coloridos. Glow ember pontual (radial-gradient com ember-dim rgba(232,87,15,.08)) apenas no hero e CTA final.
**Por que:** Sombras e gradientes são de template. A Evollure constrói profundidade com camadas de cinza e espaço negativo.
**Como:** Cards: background c900, border 1px c700. Hover: border-color ember, translateY(-3px). Glow: radial-gradient com ember em 6-8% opacity, 300-500px de spread.
**Nunca:** Box-shadow. Drop-shadow. Gradientes em backgrounds de seção. Glassmorphism. Blur em cards.

#### Micro-interações
**O que:** Sutis e intencionais. Hover em botões: background swap (ember → white, com color invert). Hover em cards: borda muda pra ember + translate up 3px. Links: underline animado. Scroll: fade-up + stagger nos elementos.
**Por que:** Micro-interações premium são sentidas, não vistas. Exagero = barulho.
**Como:** Transitions de 0.25s ease. Fade-up de 20px com opacity 0→1. Stagger de 0.1s entre elementos irmãos. Botão CTA: hover inverte cores com transition 0.25s.
**Nunca:** Animações longas (>0.6s). Bounce. Shake. Glow pulsante permanente. Parallax exagerado. Animações que bloqueiam scroll.

### DRAMATURGIA VISUAL

#### Atmosfera Global
**O que:** Grid sutil de linhas finas (1px, opacity 3-5%) sobre o fundo void, evocando precisão técnica e dados. O grid aparece em seções alternadas, nunca em todas.
**Temática:** A Evollure analisa dados de vendas — o grid representa a estrutura por trás dos insights. Ordem no caos.
**Tratamento:** Linhas em c700 com opacity 4%. Espaçamento de 60-80px. Aparece apenas no hero e na seção de features. Desaparece nas seções de respiro.

#### Composições Narrativas por Seção

##### Hero
**Comunica:** A promessa principal — "Seu time vende. A Evollure mostra onde o dinheiro está sendo perdido."
**Composição visual:** Split layout. Headline à esquerda com Neue Montreal Bold, tamanho massivo. Palavras-chave em itálico ember. À direita, uma composição SVG conceitual que representa a análise de calls — ondas sonoras estilizadas sendo decompostas em dados (barras, nós, conexões), simbolizando voz → inteligência.
**Cena detalhada:** Layout dividido 55/45. Esquerda: headline 48-56px em 2-3 linhas, a palavra-chave principal na segunda linha em bold italic ember. Subtítulo abaixo em c200, 18px, max 2 linhas. Dois botões abaixo: CTA primário ember ("Agendar Demo") + CTA secundário outline ("Como funciona"). Direita: composição SVG 450x400px mostrando 3 ondas sonoras horizontais (representando calls) que se transformam em um grafo de 5 nós conectados (representando insights). As ondas usam stroke ember em opacity decrescente (100%, 60%, 30%). Os nós são círculos de 20px em c600 com stroke ember, conectados por linhas curvas em c500 com dash-animation sutil (30s loop). O nó central é maior (32px) com fill ember representando o Orbital Knot em miniatura. Opacity geral da composição: 85%. No mobile: layout empilhado, headline primeiro (42px), SVG embaixo em 300x250px com versão simplificada (2 ondas, 3 nós).
**Viabilidade:** CÓDIGO PURO (SVG inline + CSS animations)
**Alternativa simplificada:** Apenas as ondas sonoras estilizadas sem o grafo de nós.

##### Social Proof
**Comunica:** "Empresas reais confiam na Evollure."
**Composição visual:** Seção de respiro — limpa, espaçosa, sem composição complexa. Uma linha de logos de clientes em opacity 40% com hover que sobe pra 100%. Acima, um label em IBM Plex Mono: "EMPRESAS QUE CONFIAM NA EVOLLURE".
**Cena detalhada:** Fundo c900. Padding vertical generoso (120px). Label mono centralizado em cima (ember, 9px, letter-spacing 3px). Abaixo, row de 5-6 logos em grayscale, opacity 40%, espaçados uniformemente. Hover: opacity 100%, transition 0.3s. Se não houver logos reais: usar marquee sutil com nomes de empresas em mono, opacity 30%.
**Viabilidade:** CÓDIGO PURO + ASSETS EXTERNOS (logos dos clientes)

##### Features
**Comunica:** "É assim que a Evollure transforma suas vendas."
**Composição visual:** NÃO usar 3 cards lado a lado. Cada feature é uma CENA alternada — texto à esquerda/visual à direita, depois inverte. Cada feature tem uma composição SVG/CSS única que MOSTRA o que ela faz.
**Cena detalhada por feature:**
- **Intelligence — Análise de calls:** Layout texto-esquerda, visual-direita. O visual é um "dashboard" estilizado em SVG: um retângulo de fundo c800 com borda c700 simulando uma tela. Dentro: 4 barras horizontais de alturas diferentes representando scores de critérios do Cérebro Comercial. As barras são ember em opacity decrescente. Acima das barras, um label mono "SCORE: 7.8" em ember. Um indicador circular no canto (tipo gauge) preenchido em 78%. Tudo em SVG, sem imagem externa. Animação scroll-triggered: as barras crescem da esquerda conforme a seção entra no viewport.
- **Reach — SDR com IA:** Layout visual-esquerda, texto-direita. O visual é um fluxo de mensagens estilizado: 3 balões de chat empilhados (retângulos arredondados em c800 com borda c700) com linhas de "texto" simuladas (retângulos finos em c500). Uma seta curva conecta o último balão a um ícone de "check" em ember. Representa: mensagem enviada → qualificada → convertida.
- **Prospect — Prospecção multicanal:** Layout texto-esquerda, visual-direita. O visual é um diagrama de 3 canais: três linhas paralelas horizontais (WhatsApp, LinkedIn, Email — representadas por ícones simplificados) que convergem num funil estilizado (dois paths que se juntam) terminando num ponto ember. Animação: as linhas se desenham (path draw-on) conforme entra no viewport.
**Viabilidade:** CÓDIGO PURO (SVG + CSS + scroll-triggered animations)

##### Métricas / Prova em Números
**Comunica:** "Os números provam. Sem achismo."
**Composição visual:** Seção de impacto com números enormes. 4 métricas em grid. Números em Neue Montreal Bold 48-64px com cor ember. Labels em mono. Fundo void com glow ember sutil centralizado.
**Cena detalhada:** Fundo void. Glow ember centralizado (radial-gradient, 400px spread, opacity 6%). Grid de 4 colunas. Cada métrica: número grande em cima (64px, weight 800, tracking -2px, ember ou white alternado), label mono embaixo (9px, c400, uppercase). Os números fazem count-up animation quando entram no viewport (0 → valor final em 1.5s, ease-out). Dividers verticais de 1px em c700 entre colunas. No mobile: grid 2x2.
**Viabilidade:** CÓDIGO PURO (CSS grid + JS counter + intersection observer)

##### Como Funciona
**Comunica:** "É simples. 3 passos."
**Composição visual:** NÃO usar 3 caixas numeradas. Usar um path SVG vertical que serpenteia pela seção, conectando os 3 steps como uma timeline visual. Cada step é um nó no path com texto ao lado alternando esquerda/direita.
**Cena detalhada:** Um path SVG vertical centralizado na seção (stroke ember, 2px, dash-animation de draw-on conforme scroll). Três nós circulares no path (24px, fill ember). Ao lado de cada nó, um bloco de texto: número em mono (01, 02, 03), título em bold 20px, descrição em regular 14px c300. Steps alternam esquerda/direita do path. O path se desenha conforme o scroll (stroke-dashoffset controlado por scroll position). No mobile: path alinhado à esquerda, texto sempre à direita.
**Viabilidade:** CÓDIGO PURO (SVG path + scroll-driven stroke-dashoffset)

##### CTA Final
**Comunica:** "Chega de perder dinheiro. Comece agora."
**Composição visual:** Seção de clímax com energia máxima. Headline enorme centralizado com itálico ember. Glow ember mais forte que no resto da página. Botão CTA grande.
**Cena detalhada:** Fundo void. Glow ember centralizado (radial-gradient, 500px spread, opacity 10% — o mais forte da página). Headline 42-48px centralizado, 2-3 linhas, palavra-chave em italic ember. Subtítulo 16px c200. Botão CTA grande (padding 16px 48px, background ember, color white, font-weight 700, border-radius 0). O Orbital Knot SVG aparece acima do headline em opacity 15%, tamanho grande (200px), como marca d'água atmosférica. No mobile: headline 32px, padding reduzido.
**Viabilidade:** CÓDIGO PURO

---

## Tokens de Design

### Cores — Fundos
| Token | Valor | Uso |
|---|---|---|
| `surface-page` | #050505 | Fundo principal (void) |
| `surface-section-alt` | #0A0A0A | Fundo alternado de seções |
| `surface-card` | #0A0A0A | Cards e containers |
| `surface-elevated` | rgba(10,10,10,0.85) | Nav on scroll, modais (com backdrop-blur) |
| `surface-hero` | #050505 | Fundo do hero (com glow ember) |
| `surface-input` | #111111 | Inputs e form fields |

### Cores — Texto
| Token | Valor | Uso |
|---|---|---|
| `text-primary` | #FFFFFF | Headlines, títulos |
| `text-secondary` | #999999 | Subtítulos, corpo |
| `text-muted` | #555555 | Captions, labels, metadata |
| `text-on-accent` | #FFFFFF | Texto sobre fundo ember |
| `text-highlight` | #E8570F | Palavras-chave em itálico nos headlines |

### Cores — Accent (UMA COR)
| Token | Valor | Uso |
|---|---|---|
| `accent-primary` | #E8570F | CTAs, links, highlights, badges, núcleo do Orbital Knot |
| `accent-hover` | #F07A3E | Hover state do accent (ember-400) |
| `accent-subtle` | rgba(232,87,15,0.08) | Glow backgrounds, tints pontual |
| `accent-glow` | rgba(232,87,15,0.06) | Radial gradients atmosféricos |

### Cores — Carbon (escala completa)
| Token | Valor | Uso |
|---|---|---|
| `carbon-void` | #050505 | Fundo mais escuro |
| `carbon-950` | #0A0A0A | Fundo alternado |
| `carbon-900` | #111111 | Cards, inputs |
| `carbon-800` | #1A1A1A | Bordas, dividers |
| `carbon-700` | #242424 | Bordas secundárias |
| `carbon-600` | #333333 | Bordas hover |
| `carbon-500` | #555555 | Texto muted |
| `carbon-400` | #777777 | Texto terciário |
| `carbon-300` | #999999 | Texto secundário |
| `carbon-200` | #BBBBBB | Texto corpo |
| `carbon-100` | #DDDDDD | Texto claro |

### Cores — Terra (auxiliar para warmth)
| Token | Valor | Uso |
|---|---|---|
| `terra-900` | #2C1810 | Fundo terroso profundo (uso pontual) |
| `terra-700` | #5C3520 | Acentos terrosos |
| `terra-500` | #99603C | Texto terroso |
| `terra-300` | #D4A882 | Detalhes quentes |
| `terra-100` | #F5E4D4 | Highlights terrosos |

### Cores — Warm Gray (alternativa ao Carbon puro)
| Token | Valor | Uso |
|---|---|---|
| `warm-900` | #1C1917 | Fundo com warmth |
| `warm-700` | #3B3634 | Bordas com warmth |
| `warm-500` | #78716C | Texto com warmth |
| `warm-300` | #D6D3D1 | Texto claro com warmth |

### Cores — Ember (escala completa)
| Token | Valor | Uso |
|---|---|---|
| `ember-900` | #7A2E08 | Tom mais escuro de ember |
| `ember-700` | #C4420A | Ember escuro |
| `ember-500` | #E8570F | ★ Ember principal |
| `ember-400` | #F07A3E | Hover, estados ativos |
| `ember-300` | #F5A273 | Destaques suaves |
| `ember-200` | #F9C9A8 | Tints |
| `ember-100` | #FCE4D4 | Backgrounds sutis (light mode) |

### Cores — Status
| Token | Valor | Uso |
|---|---|---|
| `status-success` | #22C55E | Confirmação |
| `status-error` | #EF4444 | Erro |
| `status-info` | #4DA3FF | Informação |
| `status-warning` | #FACC15 | Alerta |

### Tipografia
| Token | Valor | Uso |
|---|---|---|
| `font-display` | 'PP Neue Montreal', sans-serif | Headlines, títulos, wordmark |
| `font-body` | 'PP Neue Montreal', sans-serif | Texto corrido, descrições |
| `font-mono` | 'IBM Plex Mono', monospace | Labels, dados, badges, código |
| `text-hero` | 42-56px / weight 800 / tracking -1px a -2px / line-height 1.1 | Headline do hero |
| `text-section-title` | 28-36px / weight 800 / tracking -0.8px / line-height 1.2 | Título de seção |
| `text-section-subtitle` | 18-20px / weight 400 / color c200 / line-height 1.7 | Subtítulo |
| `text-body` | 14-16px / weight 400 / color c300 / line-height 1.8 | Texto corrido |
| `text-caption` | 9-10px / IBM Plex Mono / weight 500 / uppercase / tracking 3px | Labels, metadata |
| `text-cta` | 14px / weight 700 / tracking -0.2px | Texto de botões |
| `text-number` | 48-72px / weight 800 / tracking -2px a -3px | Métricas de impacto |
| `text-wordmark` | 22-56px / weight 400 / tracking -0.5px a -1px | Logo "Evollure" |

### Bordas
| Token | Valor | Uso |
|---|---|---|
| `border-default` | 1px solid #1A1A1A | Contornos padrão de cards |
| `border-subtle` | 1px linear-gradient(transparent, #1A1A1A, transparent) | Divisores entre seções |
| `border-hover` | 1px solid #E8570F | Hover state |

### Geometria
| Token | Valor | Uso |
|---|---|---|
| `radius-card` | 0px (ou 2-4px máximo) | Cards e containers |
| `radius-button` | 0px | Botões/CTAs — SEMPRE retos |
| `radius-input` | 0px | Inputs |
| `radius-badge` | 100px | Badges/tags (pill) |

### Sombras
| Token | Valor | Uso |
|---|---|---|
| `shadow-card` | none | Sem sombra — profundidade via cinzas |
| `shadow-nav` | none (usa backdrop-blur) | Nav fixa |
| `shadow-float` | none | Sem elementos flutuantes com sombra |

### Espaçamento
| Token | Valor | Uso |
|---|---|---|
| `section-padding-y` | 80px | Padding vertical padrão de seções |
| `section-padding-y-lg` | 120-160px | Padding de seções de "respiro" |
| `content-max-width` | 960px | Largura máxima do conteúdo |
| `content-padding-x` | 32px | Padding lateral |

---

## Componentes-Chave — Overrides

| Componente | Especificação |
|---|---|
| `<Button>` CTA primário | bg ember-500, color white, padding 12px 32px, font-weight 700, border-radius 0, hover: bg white color void, transition 0.25s |
| `<Button>` secundário | bg transparent, color white, border 1px carbon-600, padding 12px 32px, border-radius 0, hover: border-color ember, color ember |
| `<Badge>` | IBM Plex Mono 9px, uppercase, tracking 1.5px, padding 4px 14px, border-radius 100px, bg ember com 10% opacity, color ember-400 |
| `<Input>` | bg carbon-900, border 1px carbon-700, color white, padding 12px 16px, border-radius 0, focus: border-color ember |
| `<Card>` | bg carbon-950, border 1px carbon-800, padding 24px, border-radius 0-4px, hover: border-color ember + translateY(-3px), transition 0.3s |
| `Nav` | position fixed, bg transparent → surface-elevated on scroll, backdrop-filter blur(12px), height 64px, z-index 50 |

---

## Orbital Knot SVG (Logo/Ícone)

Usar SEMPRE inline SVG. Nunca imagem. O SVG é:

```
Três <ellipse> com cx="60" cy="60" rx="42" ry="18":
- Primeira: stroke da cor desejada, stroke-width 4, sem rotação, opacity 1
- Segunda: mesmos atributos mas stroke-width 3.5, transform="rotate(60 60 60)", opacity 0.65
- Terceira: mesmos atributos mas stroke-width 3, transform="rotate(120 60 60)", opacity 0.35
- Centro: <circle> cx="60" cy="60" r="6" fill da cor desejada
ViewBox: 0 0 120 120
```

Variações de cor:
- **Ember on void:** stroke/fill #E8570F (uso principal)
- **White on ember:** stroke/fill #FFFFFF sobre fundo ember
- **Black on white:** stroke/fill #050505 sobre fundo branco

---

## Animações de Scroll (Diretrizes)

Tom geral: **sutis, elegantes, lentas.** Nada rápido ou bouncy.

| Seção/Elemento | Tipo | Descrição |
|---|---|---|
| Hero headline | entrada | Fade up 20px + opacity 0→1, 0.6s ease-out, delay staggered 0.1s por linha |
| Hero SVG | entrada | Fade in + scale 0.95→1, 0.8s ease-out, delay 0.3s após headline |
| Social proof logos | entrada | Fade in staggered 0.15s entre cada, opacity 0→0.4 |
| Feature SVGs | scroll-triggered | Path draw-on conforme viewport, 1.5s ease-in-out |
| Métricas números | scroll-triggered | Count-up de 0 ao valor final, 1.5s ease-out |
| How it Works path | scroll-driven | stroke-dashoffset controlado por scroll position |
| CTA final | entrada | Fade up + glow ember pulse sutil (opacity 6%→10%→6%, 3s loop) |
| Cards | entrada | Fade up 20px + stagger 0.1s entre cards |

---

## Responsividade — Princípios

- **Desktop (1280+):** Dramaturgia completa — split layouts, composições SVG em tamanho cheio, tipografia massiva, espaço negativo generoso. O grid sutil aparece. Números em 64-72px.
- **Tablet (768-1279):** Layouts empilham gradualmente. SVGs reduzem para 80% do tamanho. Headlines reduzem 15-20%. Padding vertical mantém generosidade. Grid sutil desaparece.
- **Mobile (< 768):** A ESSÊNCIA sobrevive: preto real + ember como fogo pontual + tipografia bold + itálico nos destaques. SVGs simplificam (menos nós, menos linhas) ou viram versões compactas. Headlines 32-38px. Números 40-48px. Layout 100% single column. O que NÃO se perde: a cor ember, o peso tipográfico, o espaço negativo entre seções, o Orbital Knot no nav.

---

## Regra de Ouro

Ao criar qualquer seção de LP da Evollure:

1. **Siga TODAS as decisões de identidade** (ritmo + linguagem + dramaturgia) deste documento
2. **Use tokens semânticos** — NUNCA valores crus
3. **UMA cor accent: Ember #E8570F** — base Carbon neutra + Ember pontual (10% máximo)
4. **Cada seção importante DEVE ter uma COMPOSIÇÃO NARRATIVA** — SVG/CSS que reforça o ARGUMENTO da seção, não decoração genérica
5. **O scroll DEVE ter RITMO** — alternância de energia entre seções (denso→respiro→denso)
6. **NÃO substitua composição por decoração genérica** — blobs e partículas são atmosfera, não narrativa
7. **A IA implementadora é RESPONSÁVEL por criar SVGs e composições visuais ORIGINAIS** baseados nas descrições acima
8. **"90% silêncio, 10% fogo."** — O ember é brasa controlada. Se estiver em mais de 10% da interface, está errado.
9. **Cantos RETOS** em botões e frames. Sem border-radius.
10. **Itálico ember = único recurso de ênfase** nos headlines. Não use underline, não use cor diferente, não use caixa alta.
11. **Wordmark "Evollure" = Neue Montreal Regular (400).** NUNCA bold no logo. Headlines usam Bold. Logo usa Regular. Essa distinção é a marca.

## Teste Final

Coloque a LP ao lado de um template Framer/Webflow popular. A diferença deve ser óbvia em TRÊS níveis:
- **RITMO:** O scroll tem alternância de energia, seções não uniformes, "atos" narrativos com respiro entre elas
- **LINGUAGEM:** Neue Montreal Bold + itálico ember + IBM Plex Mono + cantos retos + UMA cor (ember) + preto real = personalidade inconfundível
- **DRAMATURGIA:** Cada seção importante tem uma composição visual ÚNICA (ondas→dados no hero, dashboard estilizado em features, path animado em how it works) — não decoração genérica

Se as seções tiverem blobs e gradientes mas NÃO tiverem composições narrativas únicas → INCOMPLETO.
Se a LP usar 2+ cores accent ao invés de Ember + neutros → ERRADO.
Se todas as seções tiverem a mesma energia → SEM RITMO.
Se o wordmark "Evollure" estiver em Bold/800 → ERRADO. É Regular/400.
