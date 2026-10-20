# 01 · O legado do Sergio: o que existe hoje

Este documento descreve o trabalho que herdamos, com o crédito devido. Ele cobre as duas gerações do projeto:

- **geração 1**: o site Jekyll deste fork, de 2023 a 2025;
- **geração 2**: a plataforma LIBRUS, de 2026, que **não está neste fork** e é o que está no ar hoje em
  doutrina.org.

Tudo aqui foi lido em 2026-10-20, sem rodar scripts, Jekyll nem build.

## 1. Créditos

| Pessoa | Papel |
|---|---|
| **Sergio** ([@sergioSHKLR](https://github.com/sergioSHKLR)) | Idealizador, editor e programador. Fez a transcrição manual das cinco obras, o padrão de marcação, os links, o índice e o leitor. Assina 2.154 dos 2.155 commits deste fork, com duas identidades. Na bio pública do GitHub, ele se apresenta como líder de estudos espíritas em português e inglês, com grupos e palestras públicas. |
| **Mai** | Coautora. O site assina "Mai & Sergio", e as licenças da geração 2 dizem "Copyright (c) 2026 Mai and Sergio". |
| **@JLeoBRx** | Escreveu a maior parte do README da geração 1, segundo o próprio README. |
| **JhonnyBn** ([@JhonnyBn](https://github.com/JhonnyBn)) | Dono do repositório que serviu de base a este fork. Tem um commit (2023-11-17, "Persistent dark mode"). O Sergio continuou publicando nesse repositório até 2026-07. |
| **Grok (xAI)** | O próprio Sergio dá crédito a ele, nos `CREDITS.md` da geração 2, como assistente de programação e de documentação. |
| **Voluntários** | O README e a página "Voluntário" convidam pessoas para revisão de código, testes, links e textos. Não há outros autores no git. |

**Fundação SHKLR** ([shklr.org](https://shklr.org)) é a marca guarda-chuva do casal. O aviso legal público
diz: "An independent project, not for profit", sediado em Itajaí (SC).

## 2. História

Fonte: o histórico do git, o `PROJECT-MILESTONES.md` do `doutrina-content` e o HISTORY.md do arquivo
privado. Do arquivo privado, aqui vai só um resumo.

- **Quase dez anos antes (até 2023).** O Sergio estudou em livros impressos, PDFs, eBooks e Kindle, e depois
  no Kardecpedia. Também tentou PDFs interativos, planilhas, um site no Google Sites com mais de mil páginas
  (uma por questão) e ePubs. Nenhum deles servia ao estudo sério: faltava consulta cruzada, as anotações eram
  precárias e a tipografia, ruim.
- **2023-03-19.** Primeiro commit do `doutrina.org` (Jekyll). O repositório original hoje se chama
  `sergioSHKLR/doutrina-archive` e é privado.
- **2023-06 a 2024-01: o pico.** São 1.976 commits em 2023. Nessa fase ele fez a transcrição parágrafo por
  parágrafo dos PDFs da FEB, a hierarquia, as âncoras, os links, o índice geral do LDE e as anotações com
  Hypothes.is.
- **2024-02 a 2025-03: manutenção leve.** São 164 commits em 2024 e 15 em 2025. A versão "25.3.01 beta" saiu
  em março de 2025 (relatório Lighthouse de 01/03/2025).
- **2025-03-04.** Último commit que este fork contém. O fork foi criado em 2025-08-17.
- **2025-08 a 2026-07, no upstream `JhonnyBn/doutrina.org` (59 commits à frente).**
  - Novas páginas de perfil: Leitor, Instrutor, Voluntário e Detentor de Direitos, além de "Sobre" e
    "Manual avançado".
  - Avisos legais reescritos e analytics Umami.
  - LDM, ESE, CEU e GEN retirados do ar ("Em revisão"). Só o LDE ficou publicado.
  - Aviso de migração de Jekyll para Eleventy (`doutrina-11ty`, que não está público).
  - Em 2026-07-04, o arquivo `CNAME` foi apagado, e o domínio passou para a geração 2.
- **2026-05: a geração 2 começa.** O `doutrina-content` separa o conteúdo da apresentação. O LDE é refeito
  com rigor (âncoras estáveis, índice conferido letra a letra contra o PDF, marcadores de página do PDF).
- **2026-08 a 2026-09: LIBRUS.**
  - O `librus-shell` é uma SPA em Vite que publica três "sabores": **librus.app**, **doutrina.org** e
    **centro.doutrina.org**.
  - O `librus-linker` injeta os links.
  - O `lde-q` (2026-09) é um leitor por questão do LDE, publicado em lde.doutrina.org.
  - A interface foi congelada em 2026-09-10, na versão **0.9.14 beta**.

**O upstream tem trabalho mais recente que este fork.** E a geração 2, em outros repositórios, é bem mais
avançada que os dois. Este fork é um retrato de março de 2025.

### Mapa dos repositórios

| Repositório | Papel | Período | Licença declarada |
|---|---|---|---|
| `zarpstudio/doutrina.org` (este) | Geração 1, retrato de 2025-03-04 | 2023-03 → 2025-03 | Sem arquivo LICENSE. A página Avisos legais declara CC BY-NC-SA 4.0 para o formato. |
| `JhonnyBn/doutrina.org` | Geração 1, mais 59 commits | → 2026-07-04 | Igual à de cima |
| `sergioSHKLR/doutrina-archive` (privado) | O repositório original, renomeado. Tem HISTORY.md e esboços de uma "Wiki futura" de documentação. | 2023-03 → 2026-07 | — |
| `sergioSHKLR/doutrina-content` | Etapa 1 de 4: a fonte Markdown das cinco obras, os PDFs da FEB e as ferramentas de QA | 2026-05 → 2026-09 | **CC BY-SA 4.0** para a marcação. O texto é declarado domínio público. |
| `sergioSHKLR/librus-linker` | Etapa 2 de 4: carimba os links (Luz, Wikipédia, Wikcionário, mapa, Bíblia, Kardecpedia) | 2026-08 → | MIT |
| `sergioSHKLR/librus-shell` | Etapa 3 de 4: a SPA de leitura em quatro painéis | 2026-08 → 2026-09 | MIT |
| `sergioSHKLR/doutrina`, `librus`, `centro` | Etapa 4 de 4: hosts no GitHub Pages | 2026-08 → | MIT para o código |
| `sergioSHKLR/lde-q` | Leitor por questão do LDE | 2026-09 → | MIT |

## 3. Geração 1: o site deste fork

### 3.1 O que é

O site é Jekyll no GitHub Pages (gem `github-pages`, kramdown), com domínio próprio pelo arquivo `CNAME`. Ele
se define como "uma plataforma inédita de estudos integrados". A ideia central é **ler o texto original e
consultar fontes externas sem sair da página**. A tela tem quatro colunas, que aparecem conforme a largura:

1. **Menu**: o sumário do livro e os links das páginas.
2. **Principal**: o texto da obra, com links.
3. **Complementar**: um `iframe` onde os links da coluna Principal abrem (Wikipédia, Wikcionário, Luz
   Espírita, mapas, vídeos, Bible.com).
4. **Anotações**: a barra do **Hypothes.is**, para grifos e notas privados, de grupo ou públicos.

O desktop mostra as quatro colunas, o notebook três, o tablet duas e o celular uma. Há ajustes de
tipografia, todos guardados em `localStorage`: tamanho, entrelinha, fonte serifada, sem serifa ou mono, fundo
amarelo, verde ou rosa, e texto justificado. Também há modo escuro, tela cheia, compartilhamento (Web Share),
PWA (manifest e ícones) e um mapa Leaflet com os lugares das comunicações do ESE.

### 3.2 Arquivos

| Caminho | O que é |
|---|---|
| `index.md` + `_layouts/splash.html` | Tela de entrada com uma citação ("São Luiz e Santo Agostinho") e o botão "entrar". |
| `pages/` | Início, Manual, Roteiro, Avisos legais e Contato (um formulário do Google Forms). Também `ext.md` (a tela inicial da coluna Complementar), `hypo.md` (links para a busca e o grupo no Hypothes.is), `meet.md` (sala Whereby), `push.md` (notificações PushEngage) e `test.md`. |
| `books/` | As cinco obras, **um arquivo Markdown por livro** (de 0,8 a 1,35 MB cada). |
| `_layouts/` | Um layout por livro (`1-lde.html` … `5-gen.html`), com o sumário da coluna 1 **escrito à mão**, mais `0-default`, `splash`, `ext`, `blank` e `lighthouse`. |
| `_includes/` | As partes da tela de quatro colunas: cabeçalhos, menus, ferramentas de tipografia, o `iframe` complementar, a coluna do Hypothes.is e o alerta. `toc.html` é o [jekyll-toc](https://github.com/allejo/jekyll-toc) (MIT). |
| `assets/css` | `4-cols.css` e `styles.css`. |
| `assets/js/combined.js` | Todo o comportamento: menu, rótulos, modo escuro, tela cheia, tipografia, abertura de links na coluna 3 e a **reescrita de links por classe** (§4.3). Também carrega o chat Crisp. `_old/` guarda versões antigas dos scripts. |
| `assets/maps/map-ese.html` | Mapa Leaflet/OpenStreetMap com as cidades das comunicações do ESE (Bordeaux, Lyon, Havre…). |
| `assets/pwa`, `assets/images` | Ícones, imagens de Open Graph e ilustrações. A maior parte das ilustrações (retratos, cenas) não é usada em nenhuma página. |
| `hypothesis.html` | **Não é uma página do site.** É uma exportação salva do visualizador "facet" de Jon Udell para o Hypothes.is, com **203 anotações do próprio Sergio** (de 2022-06 a 2024-01, quase todas públicas) sobre doutrina.org e um rascunho do LDM. Serve de registro de como ele usava as anotações. |
| `lighthouse-report.html`, `assets/lighthouse/` | Relatório Lighthouse de 01/03/2025. |
| `test.html` | Um tutorial do Leaflet (camadas). É só um teste. |
| `.htaccess` | Regras de cache do Apache. O GitHub Pages não usa esse arquivo. |
| `z1.sh`, `z2.sh`, `z3.sh` | Atalhos de terminal no Linux, para poupar digitação. `z1.sh` roda `sudo bundle exec jekyll build --watch --incremental` (gera o HTML a partir do Markdown), `z2.sh` roda `sudo bundle exec jekyll serve --port 7003 --incremental` (serve o site local) e `z3.sh` roda `ps -ef \| grep jekyll` (procura o processo). Não fazem mais que isso. Não foram executados. |

### 3.3 Dependências de terceiros

Há nove. **Todas serão substituídas ou dispensadas no projeto novo** (ver [02-visao.md](02-visao.md)):

- Hypothes.is (anotações);
- Crisp (chat);
- PushEngage (notificações push);
- Whereby (vídeo);
- Google Forms (contato);
- Google Fonts e Material Symbols;
- Leaflet pelo unpkg;
- os sites abertos dentro de `iframe`;
- Umami (analytics, só no upstream).

## 4. A estrutura do conteúdo

### 4.1 As obras

As cinco obras básicas, a partir das edições da FEB:

| Obra | Sigla e emoji | Tradução | Edição de base |
|---|---|---|---|
| *O Livro dos Espíritos* (1857) | LDE 👻 (✨ na geração 2) | Guillon Ribeiro | FEB, ISBN 978-85-7328-728-8 |
| *O Livro dos Médiuns* (1861) | LDM ✒️ | Guillon Ribeiro | FEB, ISBN 978-85-7328-729-5 |
| *O Evangelho segundo o Espiritismo* (1864) | ESE 🕊️ | Guillon Ribeiro | FEB, ISBN 978-85-7328-730-1 |
| *O Céu e o Inferno* (1865) | CEU 🔥 | Manuel Quintão (neste fork). Ver a divergência em [04](04-conteudo-e-licencas.md). | FEB, ISBN 978-85-7328-731-8 |
| *A Gênese* (1868) | GEN 🌱 | Guillon Ribeiro | Neste fork, a folha de rosto repete por engano o ISBN e o PDF do ESE. A geração 2 corrige para 978-85-7328-732-5. |

O método foi copiar e colar cada parágrafo do PDF da FEB, sem OCR. O texto foi adaptado para leitura em tela:

- as comunicações mediúnicas foram destacadas;
- as citações bíblicas foram destacadas, com a ARC como versão de referência (em andamento);
- o itálico do original virou **negrito**;
- os numerais romanos viraram arábicos, exceto em títulos e séculos.

### 4.2 Hierarquia, âncoras e citação

- **Hierarquia:** livro → parte (🗃️) → capítulo (🗂️) → seção (📃/📑) → questão ou item (#️⃣). O que vem
  antes do texto principal é "Pré-textual" (parte 0) e o que vem depois é "Pós-textual" (número seguinte ao
  último capítulo).
- **Âncoras da geração 1:**
  - estruturais, `#lde-2-05` (livro-parte-capítulo);
  - no LDE, **uma âncora por questão**, `#q847` e `#q25a` (1.215 questões);
  - no índice geral do LDE, uma âncora por termo (315 termos, com 228 links para questões).
  - Nos outros livros, os 350 itens numerados do LDM ainda não têm âncora explícita. Por isso as 63 remissões
    `#LDM-pNN` do LDM não têm destino.
- **Vozes:** três estilos de bloco de citação:
  - **👻 mensagem de Espírito** (`spirit-multi`), com a assinatura (por exemplo, "Erasto");
  - **✝️ trecho bíblico** (`bible-multi`), com "Livro, cap. X, vers. Y, ARC";
  - **👴🏻 Kardec** (`grey-multi`).
- **Remissões internas:** "👉 segmento relacionado" e blocos `<details>` 🔗 com termos relacionados. Na maioria,
  esses blocos ainda dizem "*em construção*".
- **Conferência:** um ✅ no fim do parágrafo indica que ele foi conferido à mão. Há 294 no LDE.

### 4.3 Links de consulta

Há dois padrões:

- **Por classe (LDE).** É uma sintaxe própria, `[termo](slug){:.x}`. O `combined.js` reescreve o `href`
  conforme a classe: `.w` vira Wikipédia, `.d` Wikcionário, `.l` Luz Espírita, `.m` Google Maps, `.v` YouTube
  e `.b` Bible.com (ARC). Os links abrem na coluna 3.
- **Por referência (LDM, ESE, CEU, GEN).** São links de referência do Markdown, como `[Mediunidade][c8r]`,
  com 34 a 53 verbetes (quase todos da Wikipédia) definidos no topo de cada arquivo.

### 4.4 Volume

| Livro | Linhas | Palavras (com a marcação) | Âncoras explícitas | Links | Notas de rodapé |
|---|---|---|---|---|---|
| LDE | 14.967 | ~166 mil | 1.479 | 2.424 Wikipédia · 2.275 Wikcionário · 1.123 Luz | 27 |
| LDM | 8.523 | ~141 mil | 45 | 2.842 por referência | 25 |
| ESE | 8.041 | ~134 mil | 41 | 1.774 por referência · 87 Luz | 25 |
| CEU | 6.025 | ~123 mil | 27 | 2.719 por referência | 64 |
| GEN | 9.845 | ~156 mil | 28 | 2.459 por referência | 328 |

São cerca de 720 mil palavras e 5 MB de Markdown. O repositório inteiro tem cerca de 130 MB, quase tudo
histórico do git.

### 4.5 Busca

**A geração 1 não tem busca de texto.** Há o sumário da coluna 1, a busca do navegador e a busca de
anotações no Hypothes.is. Na geração 2, o painel **Ache** tem sumário e busca dentro do livro.

### 4.6 O que mudou na geração 2

- **Conteúdo separado da apresentação.** Há um arquivo parcial por parte (H2), e o arquivo completo é montado
  por script.
- **Um guia de estilo rígido** (`style-guide.md` v2.0): H1 é o livro, H2 a parte, H3 o capítulo, H4 a seção,
  H5 a unidade numerada e H6 só os termos do índice geral. Uma escada de emojis acompanha os níveis.
- **"Codex serial" de âncoras.** Toda heading recebe `{letra}{nnnn}`: `s` (LDE), `m`, `e`, `c` e `g`, por
  exemplo `#s0964`. As remissões entre livros usam o serial, como `/lde/#s0964`. O número da questão fica só
  no título.
  - O próprio Sergio registrou o custo disso: inserir uma heading **renumera tudo** depois dela.
  - Também registrou que os índices impressos do ESE, do CEU e do GEN citam por "capítulo romano + item" ou
    pelo nome do caso, e não por um número único.
- **Marcadores de página do PDF**, `[]{#page-N}`, para "ir à página N do livro impresso". No LDE estão
  completos (páginas 1–482).
- **Índice geral** conferido letra a letra contra o PDF. No LDE, as letras A–C estavam prontas em 2026-05.
- **Uma metodologia de links** (`librus-linker/METHODOLOGY.md`):
  - um termo recebe um link uma vez por seção;
  - a prioridade é Luz, depois mapa, Wikipédia e Wikcionário (com teto);
  - a Bíblia só aparece em citações;
  - o Kardecpedia só aparece para obras fora das cinco.
- **O leitor LIBRUS.** Tem quatro painéis, **Ache · Leia · Consulte · Anote**.
  - Há um "sabor" por público: doutrina.org, centro.doutrina.org (com vídeo Jitsi/JaaS) e librus.app (que
    serve outros acervos, como Sherlock Holmes).
  - Telas estreitas são bloqueadas até girar o aparelho.
- **O `lde-q`.** As marcações (favoritos, grifos, notas) ficam no aparelho ou num arquivo do Google Drive do
  leitor. O plano é usar um serviço de comentários (Remark42 ou Isso). O aviso legal cita o Hyvor Talk para
  comentários públicos.

## 5. Pontos fortes

1. **Missão clara e honesta.** O objetivo é o estudo sério da Codificação, "sem simplificar o texto".
   - O projeto não tem fins lucrativos.
   - Respeita os detentores de direitos e tem uma página dedicada a eles.
   - Reconhece que o estudo rende mais em grupo.
2. **Trabalho editorial enorme.** São as cinco obras transcritas à mão. O LDE tem 1.215 questões com âncora,
   o índice geral e quase seis mil links de consulta.
3. **Identidade das vozes.** O leitor distingue sempre quem fala: Espírito, Kardec ou texto bíblico, com a
   assinatura de cada um. Isso é a base de qualquer análise crítica no estilo de Kardec.
4. **Endereços estáveis por questão e item.** São eles que permitem citar a Codificação com precisão.
5. **Estudo ativo, não mídia passiva.** Ler, consultar e anotar ficam na mesma tela, e as anotações podem ser
   de grupo.
6. **Pensado para grupos de estudo.** Há o perfil "Instrutor", grupos privados no Hypothes.is e sala de vídeo.
7. **Disciplina crescente na geração 2.** O projeto ganhou guia de estilo, validadores, conferência contra o
   PDF e créditos explícitos.

## 6. Limites

1. **Um autor só.** Quase todo o histórico depende do Sergio. O conteúdo é editado por ele, não por uma
   comunidade.
2. **A conversa mora fora.** Anotações e discussões ficam no Hypothes.is, numa conta à parte de cada leitor.
   - A API pública mostra só cerca de 21 anotações públicas no domínio doutrina.org.
   - Não há moderação, perfis nem discussão ligada a um trecho dentro do próprio site.
3. **Muitas dependências de terceiros**, cada uma com a sua conta, privacidade e risco de sumir (§3.3).
4. **Conteúdo desigual entre os livros.** O LDE está rico em links, âncoras e índice. Os outros têm menos
   estrutura, e o upstream tirou quatro livros do ar para revisão.
5. **Âncoras frágeis.**
   - Na geração 1, o LDM não tem âncoras por item.
   - Na geração 2, o serial renumera quando a estrutura muda. Para citação de longo prazo, uma referência
     ligada à obra ("LDM, item 255"; "ESE, cap. X, item 19") é mais estável.
6. **Sem busca de texto** na geração 1.
7. **Mobile.** A geração 1 pede para usar o celular deitado. A geração 2 bloqueia telas estreitas.
8. **Questões de direitos ainda abertas** (detalhes em [04](04-conteudo-e-licencas.md)):
   - notas da editora (N.E.) e a "Nota explicativa" da FEB dentro do texto;
   - PDFs da FEB guardados nos repositórios;
   - citações da ARC, que tem dono.
9. **Pequenas falhas.**
   - O GEN cita o ISBN do ESE.
   - O CEU aparece com tradutor diferente em cada geração.
   - Em `pages/meet.md`, um link de anfitrião do Whereby com token está público. Vale avisar o Sergio para
     invalidar a sala, se ela ainda existir.

## 7. Licenças, em resumo

| Camada | Geração 1 (este fork) | Geração 2 (`doutrina-content`, LIBRUS) |
|---|---|---|
| Texto de Kardec e traduções | O site diz que não exerce direitos e cita a Lei 9.610/98, arts. 7º §3º e 46. | Declarados **domínio público** (Guillon Ribeiro desde 01/01/2014; Manuel Quintão desde 01/01/2026, segundo shklr.org/legal). |
| Marcação, estrutura, links e notas próprias | **CC BY-NC-SA 4.0** (declarado na página Avisos legais, sem arquivo LICENSE). O texto também inclui o "código mestre". | **CC BY-SA 4.0** (`LICENSE` e `NOTICE`, "Copyright (c) 2026 Mai and Sergio") |
| Código | Coberto pela mesma CC BY-NC-SA. `toc.html` é MIT. | **MIT** |

O que isso significa para nós, e o que pode ou não ser aproveitado, está em
[04-conteudo-e-licencas.md](04-conteudo-e-licencas.md).

## 8. O que levamos

Seguindo a orientação do dono (2026-10-20), **levamos a ideia, não a tecnologia**:

- **Levamos:**
  - a missão e o tom (estudo sério, fidelidade, sem fins lucrativos, fraternidade);
  - as lições de produto (ler, consultar e anotar juntos; vozes identificadas; citação precisa; o grupo de
    estudo como uso principal);
  - o desenho editorial (hierarquia, índice geral, tipos de unidade por livro);
  - possivelmente o acervo em Markdown, como **dados**, desde que limpo dos trechos com dono e com o acordo do
    Sergio.
- **Não levamos:** o Jekyll, o `combined.js`, os layouts com sumário escrito à mão, os scripts `z*.sh`, o
  painel em `iframe` e as nove dependências de terceiros.
