# 04 · O acervo e as licenças

> **Aviso:** este é um levantamento técnico, não parecer jurídico. Os prazos seguem a Lei 9.610/1998 (art. 41:
> 70 anos contados de 1º de janeiro do ano seguinte à morte do autor). Antes de publicar, validar com
> assessoria jurídica, sobretudo os itens marcados **verificar**.

## 1. Resumo

| Categoria | Exemplos | Pode usar? |
|---|---|---|
| **Domínio público** | O texto francês de Kardec. As traduções de Guillon Ribeiro. A de Manuel Quintão (CEU), desde 2026. As citações bíblicas **tal como aparecem no texto traduzido**. | **Sim.** Atribuição recomendada. |
| **Livre, com condições** | A marcação do Sergio na geração 2 (CC BY-SA 4.0). O código LIBRUS (MIT). Verbetes da Wikipédia e do Wikcionário (CC BY-SA). OpenStreetMap (ODbL, com atribuição). | **Sim**, cumprindo a licença: atribuição e, no caso da CC BY-SA, a mesma licença nas derivações. |
| **Com restrição** | A marcação da geração 1 (CC BY-NC-SA 4.0: **não comercial**). | **Sim**, porque o projeto é filantrópico (dono, 2026-10-20). Mas o NC passa para as derivações (ver §6). |
| **Precisa de permissão ou deve sair** | A "Nota explicativa" da FEB. As notas da editora (N.E.). Os PDFs e o projeto gráfico da FEB. As citações da ARC (SBB). As traduções modernas (Herculano Pires, Evandro Noleto Bezerra, Salvador Gentile e outras). Os conteúdos do Luz Espírita e do Kardecpedia. | **Não**, sem permissão por escrito. Links podem. |
| **Pessoal ou de origem desconhecida** | As fotos do casal. As ilustrações sem fonte. As anotações dos leitores no Hypothes.is. | **Não reutilizar** sem consentimento ou sem conferir a origem. |

## 2. As obras básicas

| Obra | Original | Tradução usada pelo Sergio | Situação da tradução | Observação |
|---|---|---|---|---|
| *O Livro dos Espíritos* | 1857 (2ª ed. definitiva 1860), domínio público | Guillon Ribeiro (FEB) | **Domínio público no Brasil desde 01/01/2014** (o tradutor morreu em 26/10/1943) | — |
| *O Livro dos Médiuns* | 1861, domínio público | Guillon Ribeiro | Domínio público desde 2014 | — |
| *O Evangelho segundo o Espiritismo* | 1864, domínio público | Guillon Ribeiro | Domínio público desde 2014 | — |
| *O Céu e o Inferno* | 1865, domínio público | **Divergência.** Este fork credita **Manuel Quintão**. O `doutrina-content` (geração 2) diz Guillon Ribeiro, com o mesmo ISBN. | Segundo o aviso público do Sergio (shklr.org/legal), a tradução de Quintão é **domínio público desde 01/01/2026**. | **Verificar** contra o PDF de origem qual é a tradução, antes de usar o texto. |
| *A Gênese* | 1868, domínio público | Guillon Ribeiro | Domínio público desde 2014 | A folha de rosto deste fork tem o ISBN errado (o do ESE). |

**Edição de base:** a "Edição Histórica" da FEB, a partir dos PDFs que a FEB distribui de graça. Domínio público
cobre o **texto** de Kardec e o **texto da tradução**. Não cobre o que a FEB acrescentou depois (§3).

## 3. O que está dentro dos arquivos e **não** é domínio público

Encontrados ao ler os arquivos deste fork e da geração 2:

1. **"Nota explicativa"** (seção pós-textual, por exemplo `lde-6-01` e `ldm-3-01`). É um texto assinado
   "**A Editora (FEB)**", publicado por acordo com o Ministério Público Federal. Na geração 2, ele está em
   `books/md/shared/nota-explicativa.md` e entra em todas as obras. **É obra da FEB, com direitos.** Ou sai,
   ou fica com permissão.
2. **Notas da editora (N.E.).** São **cerca de 226** notas de rodapé "N.E." neste fork: LDE 21, LDM 11, ESE 16,
   CEU 27 e GEN 151. São comentários modernos da FEB, por exemplo "Atualmente, a Biologia classifica em cinco
   reinos…" e "a teoria do Grande Impacto, proposta em 1975…". **Não são de Kardec nem do tradutor.** Devem
   sair, ou ser substituídas por notas próprias da comunidade (CC BY-SA), claramente marcadas.
3. **PDFs da FEB guardados em repositórios públicos.** O upstream (`books/pdf/WEB-*.pdf`) e o
   `doutrina-content` (`books/pdf/*.pdf`) guardam os PDFs da FEB. O PDF traz o projeto gráfico, a capa e as
   notas da FEB. **Não vamos guardar esses arquivos.** Vamos linkar para o site da FEB.
4. **Metadados contraditórios na geração 2.** O front matter do CEU diz "domínio público", mas também
   "Proibida a venda ou reprodução comercial sem autorização da FEB". Na migração, os metadados precisam ser
   refeitos, e cada informação precisa de fonte.

**O que não se protege:** a numeração das questões, a estrutura da obra, as ideias e a ortografia atualizada.
A Lei 9.610, art. 8º, I, exclui ideias e métodos. O art. 7º, §3º, diz que, no domínio das ciências, a proteção
cobre a forma literária e não o conteúdo.

## 4. Citações bíblicas

- **No texto de Kardec,** os trechos bíblicos são os que Kardec citou, em geral da tradução francesa de
  **Lemaistre de Sacy** (séc. XVII, domínio público), vertidos para o português pelo tradutor da obra.
  Usados como estão, **são domínio público**.
- **O Sergio planejava substituí-los pela ARC** (Almeida Revista e Corrigida). A ARC moderna é da
  **Sociedade Bíblica do Brasil (SBB)**, com direitos. Trocar o texto aumenta a exposição a direitos **e** se
  afasta da obra original.
- **Recomendação:**
  - manter o texto como a tradução da obra traz;
  - **linkar** a referência (livro, capítulo e versículo) para uma leitura externa, como o Bible.com, que
    hoje leva à ARC, ou outra versão;
  - se a comunidade quiser mostrar outra versão ao lado do texto, usar uma tradução em domínio público
    (**verificar**: Almeida antiga, de 1681/1753; Tradução Brasileira, de 1917) ou de licença livre;
  - ou obter permissão por escrito da SBB, conforme a política de citação dela.

## 5. Outras obras de Kardec (para a wiki e o modo pesquisa)

| Obra | Original | Traduções em português |
|---|---|---|
| *Revista Espírita* (1858–1869, 136 números) | Domínio público | As traduções correntes são recentes e têm direitos (**verificar** cada uma). Até lá, link para o Kardecpedia, como a geração 2 já faz. |
| *Obras Póstumas* (1890) | Domínio público | Existe tradução de Guillon Ribeiro pela FEB. Seria domínio público desde 2014 (**verificar** o tradutor da edição). |
| *O que é o Espiritismo* (1859), *O Principiante Espírita*, *Viagem Espírita em 1862* e outros opúsculos | Domínio público | **Verificar** o tradutor e a data de cada edição. |

**Oportunidade:** como os originais franceses são livres, uma **tradução comunitária, aberta e revisada**
(CC BY-SA) das obras sem tradução livre (por exemplo, a *Revista Espírita*) é um projeto natural para a wiki e
continua o trabalho de Kardec.

## 6. O trabalho do Sergio: marcação, links e índice

| Geração | Licença declarada | O que isso significa para nós |
|---|---|---|
| **1 (este fork)** | CC BY-NC-SA 4.0. Está na página "Avisos legais", **sem** arquivo LICENSE no repositório. A licença diz cobrir só o formato (diagramação, emojis, tipografia, hierarquia, "código mestre"), **não** o conteúdo. | **NC = não comercial.** O projeto é filantrópico (dono, 2026-10-20), sem venda, anúncios nem monetização, então o uso é compatível. **Mas há duas ressalvas.** Primeiro, por causa do SA, o NC passa para as derivações: as páginas da wiki que incorporassem essa marcação ficariam BY-NC-SA, e não CC BY-SA como as outras. Segundo, pelos termos do NC, terceiros não poderiam reutilizá-las comercialmente. Por isso a geração 2 continua sendo a melhor fonte. |
| **2 (`doutrina-content`)** | **CC BY-SA 4.0** (`LICENSE`, `NOTICE`: "Copyright (c) 2026 Mai and Sergio"). O texto de Kardec e as traduções ficam de fora e são declarados domínio público. | **Compatível** com a licença da wiki (CC BY-SA 4.0, W4), com atribuição e mesma licença nas derivações. É a melhor fonte para migrar, depois da limpeza do §3. |
| **Código LIBRUS** (`librus-shell`, `librus-linker`, `lde-q`, hosts) | **MIT** | Pode ser lido e reaproveitado com aviso de copyright. O dono decidiu reconstruir em Next.js, então o mais provável é aproveitar ideias, não código. |

**Postura:** mesmo onde a licença permite, a proposta é **pedir o acordo do Sergio** e dar o crédito de forma
visível ([05](05-proximos-passos.md)). A originalidade de uma marcação sobre texto em domínio público é
discutível. A relação com quem fez o trabalho não é.

## 7. Conteúdo de terceiros só linkado (não copiado)

| Fonte | Licença | Uso no projeto novo |
|---|---|---|
| Wikipédia e Wikcionário | CC BY-SA 4.0 | Link livre. Se copiarmos um trecho para um cartão de consulta, é preciso atribuição e a mesma licença. |
| Portal Luz Espírita | Direitos reservados | Só link. |
| Kardecpedia | Direitos reservados | Só link. |
| Bible.com (YouVersion) | Direitos de cada versão | Só link. |
| Vídeos (A Igreja de Jesus Cristo dos Santos dos Últimos Dias, *Os Escolhidos*, BibleProject) | Direitos dos donos | Só link ou embed oficial. A **adequação doutrinária** desses vídeos fica para os Revisores. |
| OpenStreetMap | ODbL | Com a atribuição "© OpenStreetMap contributors". |
| Google Fonts, Noto Emoji, Material Symbols | OFL / Apache-2.0 | Livres. No site novo, servir as fontes do próprio domínio (offline primeiro). |
| `jekyll-toc` (allejo) | MIT | Fica para trás com o Jekyll. |

## 8. Imagens e outros arquivos deste fork

- **`vine.png`** é a "interpretação artística do desenho original (mediúnico)" da cepa do Prefácio do LDE. O
  desenho original de 1857 é domínio público. A **interpretação** tem autoria não documentada (**verificar**
  com o Sergio).
- **Retratos e cenas** (`french-elder.jpg`, `russian-prince.jpg`…): **não são usados em nenhuma página**. Pelo
  menos um vem de uma obra de Rembrandt (domínio público, segundo os metadados), mas a origem das outras não
  está documentada. **Não migrar** sem conferir.
- **Fotos pessoais** (`us-round.*`, `me-dec-2023.jpg`): são do casal. **Não reutilizar.**
- **Logos de terceiros** (Hypothes.is, Crisp): são marcas. Ficam para trás junto com as ferramentas.

## 9. Anotações dos leitores

- O `hypothesis.html` guarda 203 anotações do próprio Sergio, e a API pública mostra cerca de 21 anotações
  públicas no domínio. As anotações **são dos seus autores**. Os termos do Hypothes.is tratam das anotações
  públicas de forma própria (**verificar** se há dedicação ao domínio público).
- **Não importar** anotações de terceiros sem o consentimento de cada autor. As do Sergio podem ser importadas
  com o acordo dele, como notas de abertura das discussões.

## 10. Licença do que a comunidade produzir

| O quê | Proposta |
|---|---|
| Páginas da wiki | **CC BY-SA 4.0** (B22 W4), com atribuição pelo histórico de revisões |
| Posts e comentários | Licença ao operador nos termos de uso. O autor mantém a autoria. |
| Protocolos e dados de pesquisa | CC BY-SA 4.0 para os dados **sem** dados pessoais. Os consentimentos de médiuns e participantes ficam registrados à parte. |
| Imagens enviadas | O autor declara a origem e a licença no envio ([03](03-requisitos.md), IMG-5) |
| Código do site (repositório open source) | **[decisão]** MIT ou Apache-2.0 (permissivas) ou AGPL (obriga quem roda a abrir as mudanças). Ver [05](05-proximos-passos.md). |
| Texto da Codificação no repositório | Domínio público, com um `NOTICE` explicando o que é e o que não é. |

## 11. Antes de migrar qualquer texto

1. Escolher a fonte. A recomendação é o `doutrina-content` (CC BY-SA), com o acordo do Sergio. A alternativa
   é este fork (CC BY-NC-SA) ou uma transcrição nova a partir dos PDFs.
2. Confirmar o tradutor do CEU contra o PDF.
3. Retirar a Nota explicativa, as notas N.E. e qualquer outro texto da FEB.
4. Não trazer PDFs nem imagens da FEB.
5. Manter as citações bíblicas como estão no texto e linkar a referência.
6. Gravar a origem de cada obra num `NOTICE` (edição, tradutor, data de domínio público e o que foi alterado:
   numerais, itálico para negrito, marcação).
7. Creditar o Sergio e a Mai na página de créditos e no `NOTICE`, conforme a licença.
8. Obter a validação jurídica dos itens marcados **verificar**.
