# Especificação de Layout: Emagrecimento Moderno & Terapias Injetáveis

## Metadados Globais
- **Fonte Principal (Headings):** DM Serif Display (Weight 400, Italic opcional)
- **Fonte Secundária (Body):** DM Sans (Weights 300, 400, 500, 600)
- **Vibe:** Médico Premium, Moderno, Científico, Autoridade.
- **Paleta de Cores Base:**
  - `bg-dark`: #050505 (Fundo principal)
  - `bg-panel`: #111111 (Fundo de cards/seções secundárias)
  - `gold-primary`: #D4AF37 (Destaques, botões, ícones)
  - `gold-light`: #F9E596 (Gradientes e brilhos)
  - `gold-dark`: #AA771C (Sombras douradas, hover states)
  - `text-main`: #F2F2F2 (Textos principais)
  - `text-muted`: #A0A0A0 (Descrições e textos secundários)
- **Caminho das imagens dos eventos (Exemplos):**
  - `/images/EVENO GOIÂNIA/GOIÂNIA_1.JPG`, `GOIÂNIA_4.JPG`
  - `/images/EVENTO SÃO PAULO/SP1.jpg`, `SP6.jpg`
  - `/images/EVENTO SÃO LUÍS/SLZ_3.jpg`

---

## Seção 1: Hero (Já implementada, documentando padrão)

### Arquétipo e Constraints
- **Arquétipo:** Hero Dominante
- **Constraints:** Imagem com Overlay (Vignette e Fade Bottom), Mistura de Pesos Tipográficos, Botão com Hover Lift.
- **Justificativa:** Cria impacto visual extremo, integrando a foto (`BANNER.jpg`) ao layout de forma suave (immersive background), destacando a oferta inicial.

### Conteúdo
- **Badge:** 📍 ALPHAVILLE – SP | 📅 08 E 09 DE MAIO
- **Headline:** Emagrecimento Moderno & [Terapias Injetáveis] (Destaque dourado)
- **Subheadline:** O treinamento presencial que prepara médicos para dominar o tratamento atualizado da obesidade e as terapias metabólicas avançadas.
- **Bullets:** ✔ Curso intensivo, ✔ Teoria + Prática, ✔ Hands-on, ✔ Certificação
- **CTA:** QUERO GARANTIR MINHA VAGA

### Layout
- `min-height: 100vh`, padding top 100px.
- Wrapper da imagem ocupa 60% da direita absolute, com linear-gradients nas bordas para blendar com o `bg-dark`.
- Conteúdo (`max-width: 650px`) alinhado à esquerda e sobreposto com z-index.

### Tipografia
- Badge: Letras maiúsculas, 0.75rem, bold, spacing 2px.
- Título: `clamp(3.2rem, 6vw, 5.5rem)`, line-height 1.05, text-shadow para legibilidade.
- Subtítulo: 1.25rem, cor `#cccccc`.

### Cores
- Fundo: `#050505`
- Gradiente texto dourado: `linear-gradient(to right, #D4AF37, #F9E596, #D4AF37)`

### Animações
- Botão: `transform: translateY(-5px)` e aumento de `box-shadow` no hover, `0.3s ease`.
- Vignette overlay garante ausência de linhas duras no carregamento.

---

## Seção 2: O Problema (Já implementada, documentando padrão)

### Arquétipo e Constraints
- **Arquétipo:** Bento Box (Grid 1x2 modulado)
- **Constraints:** Hover Scale (nas caixas), Ícones Customizados de alto contraste, Mixed Weights no texto.
- **Justificativa:** O formato Bento separa visualmente as falhas do mercado das consequências, mantendo fácil digestão do conteúdo longo.

### Conteúdo
- **Título:** O tratamento da obesidade mudou completamente.
- **Subtítulo:** E a maioria dos médicos ainda está presa a protocolos ultrapassados. O mercado exige domínio sobre novas abordagens.
- **Caixa 1 (O que falta):** Análogos de GLP-1, Terapias injetáveis...
- **Caixa 2 (O preço):** Perder pacientes, Baixa resolutividade...

### Layout
- Grid com 2 colunas (`1fr 1fr`), espaçamento `30px`. Cards com padding forte de `50px`. 
- No mobile quebra para 1 coluna.

### Cores
- Caixa 1: Fundo `#111111`, Borda leve branca sutil.
- Caixa 2: Fundo sutil `#ff1e1e` com 2% opacidade, borda `#ff1e1e` 10%.
- Texto Alerta: `#ddd` com bullets vermelhos.

### Animações
- AOS configurado (`fade-up`, com `disableMutationObserver: true`). Hover nos bento-cards altera o translate Y em -5px.

---

## Seção 3: A Oportunidade

### Arquétipo e Constraints
- **Arquétipo:** Split Vertical (50/50 lado a lado)
- **Constraints:** Imagem Blur Background, Text Reveal.
- **Justificativa:** Proporciona um contraste suave em relação ao bloco de "problema", apresentando a solução de forma cinematográfica como uma nova janela de oportunidade.

### Conteúdo
- **Título:** Uma nova medicina está surgindo.
- **Texto:** E os médicos que dominarem essa abordagem estarão anos à frente no mercado clínico. O curso Emagrecimento Moderno & Terapias Injetáveis foi criado exatamente para isso. Capacitar médicos para atuar com segurança, ciência e resultados reais no tratamento moderno da obesidade.

### Layout
- Container Flex ou Grid 2 colunas (`1fr 1fr`) centralizado. 
- *Esquerda:* Titulo gigante centralizado verticalmente.
- *Direita:* Parágrafo explicativo ao lado, padding-left generoso (60px no desktop).
- No mobile: Stack vertical, imagem de fundo opcional sutil.

### Tipografia
- Título: DM Serif Display, `clamp(2.5rem, 4vw, 3.5rem)`, color `#F9E596`. Text shadow suave.
- Texto: DM Sans, `1.5rem`, color `#F2F2F2`, line-height 1.8.

### Cores
- Fundo: Transição gradiente de `#050505` para `#111111`.

### Elementos Visuais
- Um shape orgânico (Glow Orb dourado com blur de 120px) rotacionando suavemente ao fundo da coluna de texto, opacidade 10%.

### Animações
- Letras do Título animadas no scroll via AOS (`data-aos="fade-right"`).
- O texto aparece como `fade-left` com delay inicial de 200ms.

---

## Seção 4: Sobre o Curso

### Arquétipo e Constraints
- **Arquétipo:** Overlapping Grid (Elementos que vazam do grid tradicional)
- **Constraints:** Glassmorphism, Floating Cards.
- **Justificativa:** Cria uma sensação de camadas (depth) e tecnologia/ciência avançada, ideal para expor um curso teórico-prático complexo.

### Conteúdo
- **Título:** Sobre o Curso
- **Texto:** O curso Emagrecimento Moderno & Terapias Injetáveis foi desenvolvido para capacitar médicos no manejo clínico da obesidade...

### Layout
- Fundo com fotos de detalhe de seringa ou laboratório estético ultra-escuras (opacidade 15%).
- O conteúdo reside num Floating Card translúcido central (`max-width: 800px`), deslocado 50px acima da margem original para criar "overlap" com a seção anterior.
- Padding: `80px 60px`.

### Tipografia
- Título: DM Serif, 3rem, alinhado à esquerda.
- Texto: DM Sans, `1.2rem`, fontWeight 300.
- Drop-cap (Letra inicial do texto "O") gigante e dourada.

### Cores
- Fundo do container: rgba(20, 20, 20, 0.4) com `backdrop-filter: blur(20px)`.
- Borda: 1px solid rgba(212, 175, 55, 0.2).

### Interatividade
- Efeito Parallax sutil: o card "flutua" ligeiramente mais rápido que o fundo ao scrollar.

---

## Seção 5: O Que Você Vai Aprender

### Arquétipo e Constraints
- **Arquétipo:** Grid Assimétrico (Caixas com larguras/alturas variadas dependendo do tamanho do texto)
- **Constraints:** Hover Glow, Ícones Vetoriais SVG (linha final e limpa).
- **Justificativa:** Foge da repetição exata e monótona de check-list. Torna cada bloco de aprendizado um minicard escaneável e atraente.

### Conteúdo
- ✔ Atuar com segurança em terapias injetáveis
- ✔ Dominar protocolos modernos de emagrecimento
- ... (7 itens da copy)

### Layout
- Grid Flex Layout com `gap: 20px`. `justify-content: center`.
- Cada item é um mini-card de bordas arredondadas (8px).
- Os cards têm larguras variadas (`flex: 1 1 300px` mas com text-wrap ajustado).

### Tipografia
- Cards: DM Sans, `1.1rem`, color `#A0A0A0`, weight 400.

### Cores
- Cards Fundo: `#0a0a0a`.
- Hover: Fundo altera levemente para `#161410`, e o texto ilumina para `#F2F2F2`.

### Elementos Visuais
- Checkmarks em SVG desenhados (Draw SVG animation), dourados.

### Animações
- `Staggered fade-up`: Cada card surge com +100ms de delay no carregamento via scroll.
- Hover Glow: Box-shadow dourado de 20px com opacidade bem suave (0.05) no card ao passar o mouse.

---

## Seção 6: Para Quem É Este Curso

### Arquétipo e Constraints
- **Arquétipo:** Split Diagonal (A seção é cortada em ângulo no topo e na base)
- **Constraints:** High Contrast Typography, Scroll Target Reveals.
- **Justificativa:** O corte diagonal quebra o fluxo reto vertical, gerando energia. Divide claramente as especialidades base das metas de resultado.

### Conteúdo
- **Título:** Para Quem É Este Curso
- **Lista de Áreas:** Emagrecimento, Terapias injetáveis, Medicina estética, Longevidade e saúde metabólica, Tratamento integrado da obesidade.
- **Caixa de Foco (Subtítulo):** Ideal para médicos que desejam: se diferenciar no mercado, oferecer protocolos modernos...

### Layout
- Background da seção com cor `var(--bg-panel)` e clip-path diagonal: `polygon(0 5%, 100% 0, 100% 95%, 0 100%)`.
- Duas colunas internas. Coluna esquerda: Lista de áreas com bullets dourados minimalistas. Coluna direita: Bloco escuro com border dourada contendo "Ideal para médicos que desejam...".

### Tipografia
- Títulos: DM Serif `2.5rem`.
- Itens da Direita (Desejos): DM Sans, `1.15rem`, weight 500, maiúsculas em destaque sutil.

### Cores
- BG da Seção: `#111111`
- BG do Bloco Direito: `#050505` (Contrast box)
- Destaque: As marcas de seleção ( ✔ ) em `var(--gold-primary)`.

---

## Seção 7: Como Funciona o Treinamento

### Arquétipo e Constraints
- **Arquétipo:** Rule of Thirds (Divisão simétrica forte de 3 colunas base)
- **Constraints:** Number Counters (Números gigantes no fundo de cada etapa), Responsive Columns.
- **Justificativa:** A regra dos terços permite agrupar os 6 itens em 2 fileiras bem harmoniosas, dando sensação de processo e densidade curricular.

### Conteúdo
- **Título:** Como Funciona o Treinamento (Durante dois dias você terá acesso a:)
- 1. Conteúdo teórico atualizado
- 2. Hands-on supervisionado
- 3. Discussão de casos clínicos
- 4. Workshops especializados
- 5. Material didático completo
- 6. Certificação presencial

### Layout
- Container width 90%.
- CSS Grid: `grid-template-columns: repeat(3, 1fr)`. (Mobile: 1 coluna).
- Cada bloco tem um número gigante e translúcido caindo no fundo absoluto do bloco.

### Tipografia
- Número Gigante: DM Serif Display, `120px`, Absolute position, Color `rgba(212, 175, 55, 0.05)`, z-index 0.
- Título do bloco: DM Sans, `1.25rem`, Color `#fff`, z-index 1.

### Animacão
- O conteúdo de cada bloco faz `fade-up` enquanto o número ao fundo faz um sutil `scale-in` de 0.8 para 1.0.

---

## Seção 8: Programação do Evento

### Arquétipo e Constraints
- **Arquétipo:** Timeline Vertiacal
- **Constraints:** Sticky Element (A aba "DIA 1" fica fixa enquanto os conteúdos passam), Path Animation (Linha dourada crescendo).
- **Justificativa:** Cronogramas extensos ficam cansativos em listas simples. Uma timeline vertical reduz a carga cognitiva, guiando o olhar ponto a ponto.

### Conteúdo
- **DIA 1 – Conteúdo científico e clínico:** Evolução da obesidade...
- **DIA 2 – Workshops e prática:** Workshop de Lipedema...

### Layout
- Duas divisões macro (Dia 1 e Dia 2).
- Linha vertical dourada (width: 2px) rodando pelo lado esquerdo (`margin-left: 20px`).
- Para cada list item: Um ponto ("dot") na linha dourada, com o texto à direita (`padding-left: 40px`).
- Bloco do "DIA X" gruda (`position: sticky`) no topo da seção enquanto o usuário scrolla seus subtópicos.

### Tipografia
- Título dos Dias: DM Serif, `2.5rem`, color `var(--gold-light)`.
- Itens da Timeline: DM Sans, `1.1rem`, color `#DDD`.
- Padding entre itens: `20px`.

### Cores
- Ponto da timeline: BG `#050505`, border 2px solid `var(--gold-primary)`. Caixa de brilho no ponto ativo (via hover/scroll).

### Responsividade
- Em telas menores, a linha vertical fica bem próxima à borda esquerda para maximizar o reading space.

---

## Seção 9: Eventos Anteriores (Ouro Social/Networking)

### Arquétipo e Constraints
- **Arquétipo:** Masonry Gallery Clássica com Densidade
- **Constraints:** Imagem Granulada (Noise ao fundo), Hover Scale (Zoom in da imagem cortada), Cursor Playground (O cursor vira um "Ver mais" arredondado).
- **Justificativa:** Imagens são prova social brutal. Organização tipo masonry passa a ideia de muito volume, networking e movimento não-ensaiado (vida real).

### Conteúdo
- **Título:** Veja outros eventos realizados pelo Longevidade Brasil Movement
- **Texto e Bullets:** O Longevidade Brasil Movement já realizou diversos encontros... (Lista de itens).
- **Legenda Visual:** Mais de centenas de médicos já participaram.
- **Imagens:** Uma coleção das fotos nas pastas `EVENO GOIÂNIA`, `EVENTO SÃO PAULO`, `EVENTO SÃO LUÍS`.

### Layout
- Topo da seção: Título centralizado e texto descritivo.
- Galeria: CSS Column-count (3 no desktop, 2 tablet, 1 mobile) ou CSS Grid com ropw-spans. Gap de `16px`.
- Imagens: Cada container de imagem tem `overflow: hidden` e `border-radius: 4px`. As imagens carregam por CDN em `loading="lazy"`.

### Cores e Efeitos
- As imagens têm um filtro sutil de contraste (`contrast: 1.1`).
- No `:hover`, a imagem ampliada sutilmente (`transform: scale(1.05)`) no eixo Z, com duracão `0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94)`. Ocultando partes das outras.
- Filtro Granulado aplicado no pseudo-elemento do container principal da seção para mesclar o topo com as imagens.

---

## Seção 10: Local do Evento & Investimento

### Arquétipo e Constraints
- **Arquétipo:** Spotlight (Iluminação central) + Framed Content (Card de Preço Mestre).
- **Constraints:** Neon Colors Sutil (Glow dourado atrás do preço), Reveal on Scroll (Valores surgem escalando).
- **Justificativa:** Junta duas informações de decisão cruzadas: "Onde/Quando" e "Quanto". Manter ambas sob o mesmo holofote psicológico.

### Conteúdo
- **Local:** 📍 Alphaville – São Paulo | 📅 08 e 09 de Maio. Treinamento presencial com networking.
- **Preço:** Formação completa. R$ 8.000 ou 10x sem juros. Destaque: 💰 10% de desconto para pagamento via Pix.

### Layout
- Fundo totalmente preto `#000` (quebra do `bg-dark`), com um "holofote" desenhado em CSS Radial Gradient central no topo do card de preço.
- Elemento Esquerda: Infos de local, mais limpo e textual.
- Elemento Direita: Card de Investimento. Borda `1px solid var(--gold-primary)`, background `#111` com `box-shadow` pulsante bem leve (`0 0 30px rgba(212,175,55,0.1)`).

### Tipografia
- Preço: DM Serif, gigante `3.5rem`, color `var(--gold-light)`.
- Condição Pix: DM Sans, `1rem`, `background: rgba(46, 204, 113, 0.1)`, `color: #2ECC71`, pill-shaped radius.

### Animações
- Card de Preço faz um `zoom-in` (`scale(0.95) to scale(1)`) via AOS `fade-up`.

---

## Seção 11: Escassez e CTA Final

### Arquétipo e Constraints
- **Arquétipo:** Progressive Reveal + Split Assimétrico (Maioria do bloco alerta escassez, botão embaixo focado).
- **Constraints:** Color Overlay alert mode, Button Pulse Loop.
- **Justificativa:** Ultima chance. Precisa gerar senso de encerramento, urgência real e conversão imediata.

### Conteúdo
- **Destaque:** ⚠️ Vagas limitadas. 
- **Texto:** Por se tratar de um treinamento presencial com prática supervisionada, as vagas são restritas...
- **Título CTA:** Garanta sua vaga agora
- **CTA:** QUERO GARANTIR MINHA VAGA

### Layout
- Margens internas altas (Padding `100px 0`).
- Container max-width enxuto (`600px`), totalmente centralizado. Text-align center.
- Alerta encapsulado visualmente (Pill com ícone de warning e texto amarelo forte).
- Botão Extra Gigante no final.

### Tipografia
- Tõtulo Final: `3rem` DM Serif.
- Texto Escassez: `1.2rem` DM Sans, line-height `1.5`.

### Cores e Efeitos
- O fundo na área do CTA final volta a ter um gradiente dourado ultra-esfumaçado (como no Hero) no rodapé da página.
- Botão: `var(--gold-primary)` background, Color `#050505` text.

### Animação Interativa
- Botão faz `Pulse Loop` sutil a cada 2 segundos (`transform: scale(1.02); box-shadow: 0 0 20px var(--gold-primary)`).

---

## Seção 12: Rodapé / Contato

### Arquétipo e Constraints
- **Arquétipo:** Minimal
- **Constraints:** Monocromático, Sem padding superior excessivo.
- **Justificativa:** Evita distrações da conversão. Deixa contatos visíveis para dúvidas rápidas.

### Conteúdo
- Site: www.grupolongevidadebr.com.br
- Instagram: @longevidadebrasilmovement / @drfernandofranca
- Suporte: suporte@grupolongevidadebr.com.br

### Layout e Estilos
- Background: `#000000` (Preto absoluto).
- Tipografia: DM Sans, `0.9rem`, `color: #777`.
- Hover nos links: Mudam para `#FFF` de forma instantânea.
- Estrutura em única linha no desktop (`display: flex; justify-content: space-between`), quebra em stack vertical no mobile.

---

## Elementos Encantadores (Craft / Micro-Interações)
1. **Cursor Personalizado:** Um cursor point diminuto (dot) dourado em seções interativas. Inverte cores sobre imagens claras.
2. **Seleção de Texto:** `::selection { background: rgba(212, 175, 55, 0.4); color: #fff; }` para que a cópia lida mantenha a estética premium.
3. **Smooth Scroll Bar:** Barra de navegação do browser customizada no css, ultra fina (4px) e dourada escura `#AA771C`.
4. **Delay Fotográfico:** Na Seção de Eventos, um delay incremental puro do CSS em imagens no Grid Masonry faz elas subirem ritmadamente "como uma onda" na primeira visualização.
