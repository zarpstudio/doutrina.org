# 03 · Requisitos de produto

Este documento lista os requisitos do produto, não o design das telas. Para cada requisito, diz quem é
responsável e o que falta especificar.

## Legenda

| Marca | Significa |
|---|---|
| **[B22]** | Já está coberto no B22 do `main` (a seção vem ao lado). [Link do B22](https://github.com/zarpstudio/backend_api_zarp-admin/blob/main/docs/superpowers/specs/2026-10-19-zarpos/22-wiki-and-community.md) |
| **[backend]** | Outro módulo do backend da Zarp (CMS, users, notifications, search) |
| **[site]** | O site em Next.js, open source, neste repositório ou num derivado do template |
| **[lacuna B22]** | Precisa ser levado à correção do B22, que está em andamento (ver o resumo no §17) |
| **[decisão]** | Depende do dono (ver [05](05-proximos-passos.md)) |

## 0. Premissas

1. **Offline primeiro** (dono, 2026-10-20). Ler, buscar e anotar não dependem de rede. A comunidade sincroniza
   quando há conexão (§11).
2. **O repositório do site é open source.** Toda regra que importa mora no backend, e o cliente só antecipa
   avisos.
3. **O backend da Zarp só entra na parte de wiki e comunidade** (B22) e nos módulos que ela já usa (CMS para
   mídia e blog, users, notifications, search).
4. **A Codificação é conteúdo do site,** versionada no repositório e empacotada para uso offline. O backend
   guarda só uma referência leve de cada trecho (§1, COD-6).
5. **As regras de negócio seguem o mercado** (pedido do dono). Onde o B22 já adota um padrão conhecido
   (Reddit, Discourse, MediaWiki, Lobsters), ele é mantido. As lacunas estão marcadas.

## 1. Codificação (o acervo)

| ID | Requisito | Quem |
|---|---|---|
| COD-1 | As cinco obras ficam legíveis por parte, capítulo e questão ou item, fiéis à tradução escolhida ([04](04-conteudo-e-licencas.md)), e disponíveis offline. | [site] |
| COD-2 | **Cada unidade tem um endereço estável que nunca renumera,** baseado na numeração da própria obra: LDE pela questão (`lde/847`, `lde/790a`); LDM pelo item (`ldm/255`); ESE e GEN por capítulo e item (`ese/10/19`, `gen/15/19`); CEU por parte, capítulo e item, com os casos da 2ª parte por nome. O "codex serial" da geração 2 renumera quando a estrutura muda, por isso não serve como referência pública (pode servir como id interno). | [site] · formato: [decisão] |
| COD-3 | As vozes ficam marcadas semanticamente, com assinatura: Espírito, Kardec, texto bíblico, nota. | [site] |
| COD-4 | Índice geral de cada obra; depois, um índice combinado das cinco. | [site] |
| COD-5 | **O texto é protegido.** Correção de transcrição só entra por pedido (botão "reportar erro de transcrição") e passa pela Equipe e pelo Revisor. Como o repositório é aberto, a correção vira um PR, e o histórico de mudanças do texto é público. | [site] + repositório |
| COD-6 | **Registro leve de trechos no backend:** id canônico, rótulo ("LDE, q. 847"), URL e hash do texto. Serve para validar citações, contar discussões e ligar discussões a um trecho. | [lacuna B22] |
| COD-7 | Opcional: ir à página do livro impresso (os marcadores de página que o Sergio fez na geração 2). | [site] · [decisão] |
| COD-8 | Futuro: o original francês lado a lado. É domínio público. | [site] · [decisão] |

## 2. Citações da Codificação

| ID | Requisito | Quem |
|---|---|---|
| CIT-1 | Uma sintaxe curta de citação em posts, comentários e páginas da wiki, por exemplo `[[LDE 847]]`, `[[LDM 255]]` ou `[[ESE X, 19]]`. Ela vira link com pré-visualização do trecho, que funciona offline porque o texto está no site. | [site] para mostrar, [lacuna B22] para analisar e guardar |
| CIT-2 | Citação literal com trecho: o texto citado é conferido com o original (pelo hash do trecho), e o site avisa se a citação não confere. | [lacuna B22] |
| CIT-3 | **"Onde isto é citado":** cada questão ou item mostra as páginas da wiki e as discussões que o citam (backlinks). | [lacuna B22]. O `WikiLink` precisa de um tipo `citation`, e posts e comentários também precisam ser indexados. |
| CIT-4 | Referência inexistente gera aviso antes de publicar (`dryRun`) e aparece como link vermelho. | [B22 §6] (dryRun) + [lacuna B22] |
| CIT-5 | Na wiki, uma afirmação doutrinária sem fonte pode ser marcada "precisa de citação" por Revisores. | [site] + categorias [B22 §4.6] |
| CIT-6 | Outras fontes ficam como referência formatada: *Revista Espírita* (mês e ano, com link para o Kardecpedia), Bíblia (livro, capítulo e versículo, com link) e obras fora das cinco. | [site] |

## 3. Wiki

| ID | Requisito | Quem |
|---|---|---|
| WIKI-1 | Páginas com revisões imutáveis, autoria, diff, histórico e reversão. | [B22 §4.6, §6] |
| WIKI-2 | Páginas doutrinárias com edições pendentes: membros abaixo do nível sugerem, e o Revisor aprova ou rejeita com motivo. | [B22 §6] (`pendingChanges`, suggested edits) |
| WIKI-3 | Categorias e modelos de infobox, por exemplo: Espírito comunicante, Médium (histórico), Obra, Conceito, Caso (CEU), Lugar, Grupo ou Centro. | [B22 §4.6] (`WikiInfoboxTemplate`) |
| WIKI-4 | Cada página tem a sua discussão. | [B22 §4.3] (`Post.kind = talk`) |
| WIKI-5 | Links internos, backlinks, páginas desejadas e redirecionamentos depois de mover. | [B22 §4.6] |
| WIKI-6 | Glossário, a partir do "Vocabulário espírita" (LDM, 2ª parte, cap. XXXII). | [B22] (categorias) + [site] |
| WIKI-7 | **Divergências documentadas, nunca apagadas:** uma seção padrão "Visões divergentes", com citações. | [site] (modelo) + Revisores |
| WIKI-8 | Licença das páginas: CC BY-SA 4.0. | [B22 §15 W4] |
| WIKI-9 | Edição offline: a página vista fica guardada, a edição entra na fila com `baseRevisionId`, e o conflito é tratado ao sincronizar. | [B22 §6] (409 `edit_conflict`) + [site] |

## 4. Discussões ligadas a qualquer conteúdo

O dono pediu discussões presas a **qualquer conteúdo**: post do blog, vídeo, página e trecho da Codificação.

| ID | Requisito | Quem |
|---|---|---|
| THR-1 | Qualquer conteúdo pode ter uma discussão: página da wiki, artigo do blog (CMS), vídeo (mídia do CMS ou vídeo externo), **questão ou item da Codificação**, capítulo da Codificação, protocolo de pesquisa e encontro de grupo. | [lacuna B22] |
| THR-2 | Há **uma discussão principal por conteúdo**, criada quando chega o primeiro comentário. Posts livres que citam o conteúdo aparecem como "também discutido em". | [lacuna B22] |
| THR-3 | **Anotação presa a um trecho selecionado**, como no Hypothes.is, que ela substitui. A âncora é o id da unidade mais um seletor de citação de texto (modelo W3C Web Annotation: o trecho, o prefixo e o sufixo), para resistir a pequenas mudanças. A visibilidade pode ser privada, de grupo ou pública. **A privada fica só no aparelho** (§11), a menos que a pessoa ative a sincronização. | [site] + [lacuna B22] (de grupo e pública) |
| THR-4 | O leitor mostra quantas discussões e anotações existem por trecho. | [site] + [lacuna B22] (contagem por assunto) |
| THR-5 | Comentários em árvore, votos, ordenação (melhores, novos, controversos) e karma. | [B22 §4.3, §4.4, §5] |

**Hoje o B22 só liga discussão a página da wiki** (`talkPageId`). A proposta para a correção é um assunto
genérico no `Post`: `subjectType` (`wiki_page` \| `cms_article` \| `media` \| `external_video` \|
`codification_unit` \| `research_protocol` \| `group_event`) e `subjectRef`, com uma discussão principal
única por `(tenant, subjectType, subjectRef)`. As anotações viram comentários com âncora.

## 5. Posts com imagens

| ID | Requisito | Quem |
|---|---|---|
| IMG-1 | Os posts podem ser de texto, link, imagem ou galeria. | [B22 §4.3] (`PostMedia`) |
| IMG-2 | O upload passa pelo armazenamento do CMS: a imagem é recodificada, o EXIF é removido (pela privacidade e pela localização), o SVG é recusado, há limite de 10 MB e cota por nível de confiança (o TL0 não envia). | [B22 §7.1, §10] |
| IMG-3 | O texto alternativo é obrigatório, ou ao menos pedido com insistência. | [B22] (`altText`) + [lacuna B22] (obrigatoriedade) |
| IMG-4 | Imagens em comentários. | [decisão] · [lacuna B22] (hoje só em posts) |
| IMG-5 | Origem e licença da imagem declaradas no envio (própria, domínio público ou CC). É necessário para imagens usadas na wiki. | [lacuna B22] |
| IMG-6 | Imagem com pessoas identificáveis (médiuns, participantes de sessão) exige que o autor confirme o consentimento delas. | Regra do site + [lacuna B22] (campo de confirmação) |
| IMG-7 | Varredura de CSAM na borda (Cloudflare) e denúncia. A classificação de imagem por IA fica para depois. | [B22 §7.4, §7.8] |
| IMG-8 | Offline: a imagem é redimensionada no aparelho, entra na fila e só é enviada quando houver conexão. | [site] |

## 6. Moderação, incluindo palavrões

| ID | Requisito | Quem |
|---|---|---|
| MOD-1 | Fila, ações, registro público, notas de moderador, sanções, remoção com motivo e **recurso** (modmail). | [B22 §4.7, §7] |
| MOD-2 | Níveis de confiança, cotas, limite de velocidade por discussão, controle de multidão e anti-brigada. | [B22 §3.6, §7.1, §7.7] |
| MOD-3 | **Filtro de palavrões em pt-BR** (detalhes abaixo). | [B22 §7.5] (listas de frases) + [lacuna B22] |
| MOD-4 | **Regras do site próprias do projeto**, cada uma com motivo de remoção pronto (detalhes abaixo). | [B22] (`CommunityRule` de site) + texto [decisão] |
| MOD-5 | O que foi escrito offline só fica público depois das verificações do servidor. Se for recusado, o autor recebe o motivo no aplicativo e o rascunho continua salvo. | [B22] + [site] |
| MOD-6 | **Remoções e ordens legais também apagam os caches locais** na próxima sincronização, inclusive imagens. | [lacuna B22] (§11) |
| MOD-7 | Moderação por IA com rótulos e limiares por comunidade. Ela nunca bane nem aprova sozinha. | [B22 §7.4] |

**Regras do site (MOD-4):**

- **sem mediunidade remunerada nem venda de serviços espirituais.** "Dai gratuitamente o que gratuitamente
  recebestes" (ESE, cap. XXVI), e LDM, 2ª parte, cap. XXVIII (Charlatanismo e embuste);
- sem promessa de cura e sem conselho médico;
- sem atribuir comunicação a pessoa viva;
- sem expor pessoa falecida identificável sem consentimento da família;
- sem intolerância religiosa, que é crime no Brasil (Lei 7.716/1989);
- respeito às divergências entre correntes e instituições.

**Filtro de palavrões (MOD-3).** O B22 já tem listas de frases da AutoMod (`AutoModRule`, literal ou glob,
sem regex). O que falta para o português:

1. **Uma lista pt-BR mantida pela Equipe,** com níveis:
   - **leve:** o autor recebe um aviso antes de enviar e pode reescrever;
   - **médio:** o texto vai para a fila;
   - **grave**, ou insulto dirigido a uma pessoa: o texto é retido e vai para a fila (combina com o rótulo
     `harassment` da IA).

   A ação pode ser ajustada por comunidade. Uma comunidade de iniciantes pode ser mais estrita, por exemplo.
2. **Normalização antes de comparar.** Isso hoje não existe na AutoMod, que compara texto literal.
   - O texto passa para minúsculas e perde os acentos.
   - O leetspeak é desfeito (`0→o`, `1→i`, `3→e`, `4→a`, `@→a`, `$→s`).
   - Letras repetidas são reduzidas ("porrraaa").
   - Separadores são removidos ("p.o.r.r.a", "p o r r a").
   - Caracteres parecidos (confusables) são reduzidos à mesma forma. O B22 já faz isso nos handles.
3. **Palavra inteira e lista de exceções,** contra falso positivo (o "problema de Scunthorpe"): "cu" em
   "curso", "pica" em "picanha", verbos que também são palavrões. Os falsos positivos que os moderadores
   revertem alimentam a lista de exceções.
4. **Onde se aplica:** títulos, posts, comentários, edições da wiki, handles, bio, nomes de grupo e legendas.
5. **Nunca se aplica** ao texto da Codificação nem às suas citações literais conferidas (CIT-2). A lista não
   pode incluir termos que a própria obra usa, como "prostituição" ou "adultério".
6. **A lista pode ser pública.** O repositório é aberto, e o cliente usa a lista para avisar antes de enviar,
   mas quem decide é sempre o servidor.
7. **Rótulos da IA:** acrescentar `profanity` e `insult` aos rótulos da moderação por IA (§7.4 do B22).

## 7. Modo pesquisa

É o método de Kardec como fluxo de trabalho ([02](02-visao.md), §3). **Tudo aqui é [lacuna B22]:** a correção
do B22 em andamento está acrescentando o "modo pesquisa", e esta seção é a proposta de produto para ela.

| ID | Requisito |
|---|---|
| PES-1 | **Protocolo de pesquisa.** Tem título, perguntas (escritas **antes** das sessões e travadas depois de abertas), hipótese, citações da Codificação (obrigatórias), método (um modelo baseado em LDM, caps. XXIV–XXVII e XXIX), critérios de análise, coordenador e grupos participantes. As fases são: rascunho → aberto → em coleta → em análise → concluído (ou arquivado). |
| PES-2 | **Sessão.** Registra grupo, data, cidade (opcional), participantes e médiuns **por pseudônimo**, com consentimento registrado, além do tipo de comunicação e das condições. As perguntas feitas saem do protocolo, sem alteração. As respostas são transcritas na íntegra, com a assinatura atribuída, as observações e anexos (imagem de psicografia, com consentimento). Depois de **selada**, a sessão não pode mais ser editada. Correções entram como acréscimo, com motivo. |
| PES-3 | **Replicação cega** (controle universal do ensino dos Espíritos). Um grupo não vê as respostas dos outros grupos à mesma pergunta até selar a própria sessão, ou até o prazo do protocolo acabar. Só então abre a comparação. |
| PES-4 | **Análise de concordância.** Para cada pergunta, as respostas são classificadas em concorda, diverge ou parcial por **dois Revisores independentes**. Se os dois discordarem, um terceiro decide, como é prática na pesquisa científica. |
| PES-5 | **Crítica de identidade e de contradições.** Um roteiro de verificação a partir de LDM, caps. XXIV e XXVII: linguagem, coerência com o caráter atribuído, contradições, pedidos de elogio ou de dinheiro (sinais de mistificação). |
| PES-6 | **Conclusão como página da wiki,** no espaço "Pesquisa". Traz o resultado, as citações, os limites e o grau de concordância (alto, baixo ou inconclusivo). **Nunca "verdade revelada".** Uma conclusão pode ser revista por um novo protocolo. |
| PES-7 | **Ética e dados sensíveis.** Convicção religiosa é **dado pessoal sensível** na LGPD (art. 5º, II, e art. 11). Por isso: consentimento explícito, pseudônimo por padrão, coleta mínima e nenhum dado pessoal na exportação. Menores não participam de sessões. Nada de diagnóstico nem de cura. |
| PES-8 | **Quem pode participar:** membros a partir do TL2, num grupo de pesquisa aprovado. O Coordenador abre o protocolo e os Revisores analisam. |
| PES-9 | **Dados abertos:** os protocolos concluídos podem ser exportados (CSV ou JSON) sob CC BY-SA, sem dados pessoais. |
| PES-10 | **Offline.** A sessão pode ser registrada sem internet, durante a reunião, e selada no aparelho com a hora local. A hora oficial é a do servidor na sincronização. Para manter a regra de cegamento, o aparelho não guarda as respostas de outros grupos antes do fim da coleta. |

## 8. Grupos de estudo

| ID | Requisito | Quem |
|---|---|---|
| GRP-1 | O grupo é uma comunidade privada ou restrita, com o Coordenador como moderador. | [B22 §4.2] (`visibility`, `CommunityModerator`) |
| GRP-2 | **Plano de leitura**, por exemplo o ESE com um capítulo por semana, com os trechos linkados. O progresso individual fica no aparelho, e o progresso do grupo é opcional. | [site] + [lacuna B22] |
| GRP-3 | **Encontros:** data, link externo de reunião, pauta (trechos) e ata (uma página do grupo). A agenda é de outro módulo, ainda a definir. | [lacuna B22] / [backend] |
| GRP-4 | Anotações de grupo presas aos trechos, no lugar dos grupos do Hypothes.is. | THR-3 |
| GRP-5 | Convite e aprovação de participantes. | [B22 §4.2] (`approvedContributor`) |
| GRP-6 | Um grupo pode representar um **centro espírita**, com selo verificado pela Equipe. É a ideia do sabor "centro" do Sergio. | [decisão] |
| GRP-7 | Offline: o material do encontro (trechos e pauta) é baixado antes. | [site] |

## 9. Perfis e papéis

| ID | Requisito | Quem |
|---|---|---|
| PRF-1 | O perfil tem handle, avatar, bio, karma, flair e data de entrada. O `User` é um só, com uma extensão por tenant (D33). | [B22 §3.1, §4.1] |
| PRF-2 | O nome real, o e-mail, o telefone e a data de nascimento nunca ficam públicos. | [B22 §3.1] |
| PRF-3 | **Papéis:** Visitante, Membro, Coordenador, Revisor, Moderador e Equipe ([02](02-visao.md), §6), com selo no perfil. São concedidos pela Equipe. | [B22] (`siteRole`, moderadores, TL) + [lacuna B22] (papel Revisor e revisão de pesquisa) |
| PRF-4 | Contribuições do membro: edições, discussões e protocolos. | [B22] |
| PRF-5 | **A pessoa escolhe se os seus grupos aparecem no perfil.** Pertencer a um grupo espírita revela convicção religiosa, que é dado sensível. | [lacuna B22] |
| PRF-6 | Idade mínima. | [B22 §3.4] + [decisão]. A proposta é 16 anos para a comunidade e 18 para o modo pesquisa. |
| PRF-7 | Exportar e apagar a conta (LGPD, art. 18). O apagamento também limpa os dados locais na próxima sincronização. | [B22 §3.5] + [site] |

## 10. Notificações

| ID | Requisito | Quem |
|---|---|---|
| NOT-1 | Avisos de: respostas, menções, **citação do seu conteúdo**, decisão de moderação, convite de grupo, revisão da sua edição e mudança de fase de um protocolo. | [B22] + [backend] (`zarp-notifications`, ampliado para usuários finais) |
| NOT-2 | Offline: as notificações chegam na sincronização. O Web Push nativo, no lugar do PushEngage, é opcional. | [site] + [decisão] |
| NOT-3 | E-mail com resumo (digest) configurável. | [B22 §10] |

## 11. Offline primeiro, sessão e sincronização

| ID | Requisito | Quem |
|---|---|---|
| OFF-1 | **PWA com service worker.** A interface, a Codificação e o índice de busca ficam guardados (precache). Depois da primeira visita, tudo funciona sem rede. | [site] |
| OFF-2 | **Armazenamento local:** IndexedDB para os dados e `localStorage` só para preferências pequenas. O site pede armazenamento persistente (`navigator.storage.persist()`). **Aviso:** o Safari, no iOS, apaga os dados de sites não instalados depois de cerca de 7 dias sem uso. Por isso o site deve incentivar a instalação como aplicativo e oferecer backup. | [site] |
| OFF-3 | **Dados pessoais ficam no aparelho:** favoritos, grifos, notas privadas, progresso de leitura, preferências e rascunhos. Exportar e importar em JSON, como no `lde-q`. A **sincronização com a conta** (backup e vários aparelhos) é opcional, e cifrar as notas privadas de ponta a ponta também. | [site] + [decisão] |
| OFF-4 | **Cache do que foi visto:** páginas, discussões e grupos, com limite de tamanho. O que é menos usado sai primeiro. | [site] |
| OFF-5 | **Fila de escrita offline (outbox).** Cada operação leva uma chave de idempotência gerada no aparelho, e o servidor descarta as repetidas. A fila respeita a ordem e tenta de novo com espera crescente. O status "pendente" fica visível, e uma recusa mostra o motivo e mantém o rascunho. | [site] + [lacuna B22] (`Idempotency-Key` nas escritas de membro) |
| OFF-6 | **Sincronização incremental.** Uma chamada do tipo `GET …/sync?since=<cursor>` devolve o que mudou nos escopos da pessoa (comunidades, páginas acompanhadas, conteúdo próprio, grupos): criado, editado, apagado, removido pela moderação ou retirado por ordem legal. Para o que sumiu, ela devolve marcas de remoção (tombstones). O cursor só avança. | [lacuna B22] |
| OFF-7 | **Conflitos:** edição da wiki com base e merge, ou 409; comentário só acrescenta; voto fica com o último, pela hora; perfil com conferência de `version`. | [B22 §6] + [site] |
| OFF-8 | **Sessão de aparelho que não expira:** **sem prazo absoluto**, mas revogável. Ver o detalhe abaixo da tabela. | [lacuna B22] + [backend] (`zarp-users`) |
| OFF-9 | **Sanções offline.** Quem foi banido continua lendo o que está em cache e escrevendo rascunhos. Na sincronização, as escritas são recusadas. Se a pessoa saiu ou foi tirada de um grupo privado, o conteúdo desse grupo é apagado do aparelho. | [lacuna B22] + [site] |
| OFF-10 | **Ordens legais e remoções graves** (CSAM, ordem judicial, dado pessoal exposto) obrigam o aparelho a apagar o item na sincronização, inclusive as imagens. | [lacuna B22] + [site] |
| OFF-11 | **Hora.** A hora do servidor vale para a publicação. A hora local fica guardada como "escrito em". | [B22] + [site] |
| OFF-12 | **Sem segredo no cliente.** O site usa a API pública documentada. A chave de site do B22 (§2.3) é só um identificador, não um segredo. Valem os limites de requisição do B21a. | [B22] + [site] |

**Sessão de aparelho (OFF-8).**

- **O que fica do pedido do dono:** a sessão não tem prazo absoluto. Offline, a pessoa continua logada.
- **Padrões do mercado que entram:**
  - o token de renovação muda a cada uso, com detecção de reuso (sinal de roubo);
  - o servidor mantém uma lista de revogação;
  - o perfil mostra a lista de aparelhos, com a opção "encerrar";
  - ações sensíveis (trocar e-mail ou senha, apagar a conta) pedem login recente;
  - há um botão "sair e apagar os dados deste aparelho".
- **Offline:** a identidade local basta para ler e escrever rascunhos. Toda escrita é revalidada na
  sincronização. Se a sessão foi revogada, o aparelho para de enviar, mantém os rascunhos exportáveis e pede
  login.

## 12. Busca

| ID | Requisito | Quem |
|---|---|---|
| BUS-1 | **Busca na Codificação offline.** O índice é gerado no build e roda no aparelho. Ignora acentos e reconhece variações de palavra em português. A biblioteca será escolhida no levantamento open source (OSS first). | [site] |
| BUS-2 | Busca na wiki e na comunidade, no servidor. | [B22 §10] (`shared/search`) |
| BUS-3 | Busca no que está em cache, quando offline. | [site] |
| BUS-4 | Filtros por obra, por tipo de voz (Espírito, Kardec, Bíblia) e por assinatura. | [site] |

## 13. SEO e compartilhamento

| ID | Requisito | Quem |
|---|---|---|
| SEO-1 | URLs canônicas, dados estruturados, sitemaps, IndexNow e regras de `noindex`. | [B22 §8] |
| SEO-2 | **As páginas da Codificação são estáticas e indexáveis,** com URLs por unidade (COD-2). É o maior ativo de busca do site. | [site] |
| SEO-3 | Prévia de compartilhamento (Open Graph) de uma questão ou de um item, com o trecho. | [site] |

## 14. Legal e privacidade no Brasil

**O B22 foi escrito com foco nos EUA:** DMCA, COPPA, leis da Flórida, NCMEC. Esta wiki é brasileira. Tudo
abaixo é **[lacuna B22]** e precisa ser validado com assessoria jurídica:

1. **LGPD:** base legal, consentimento específico para dado sensível (convicção religiosa, art. 11),
   encarregado (DPO), direitos do titular (art. 18) e política de privacidade em português.
2. **Marco Civil da Internet** (Lei 12.965/2014):
   - guarda dos registros de acesso por 6 meses (art. 15). A obrigação vale para quem atua com fins
     econômicos. Como o projeto é filantrópico, falta confirmar se ela se aplica quando a Zarp, uma empresa,
     opera o site sem fins econômicos;
   - remoção após notificação, nos casos dos arts. 19 e 21;
   - a decisão do STF de 2025 sobre o art. 19 aumentou a responsabilidade das plataformas.
3. **Menores:** ECA e ECA Digital (Lei 15.211/2025), com idade mínima e verificação.
4. **Direito autoral:** notificação de violação com base na Lei 9.610/98, o equivalente nacional ao DMCA. É
   preciso um tipo de caso legal próprio no `LegalCase`.
5. **Intolerância religiosa** (Lei 7.716/1989): é motivo de denúncia e de remoção.
6. **Termos de uso, regras do site e política de conteúdo em português.**

## 15. Acessibilidade, idioma e desempenho

| ID | Requisito | Quem |
|---|---|---|
| NF-1 | WCAG 2.2 nível AA, com tipografia ajustável e modo escuro (legado do Sergio). | [site] |
| NF-2 | **Mobile em pé por padrão,** com tablet e desktop aproveitando as colunas (ler, consultar e conversar). | [site] |
| NF-3 | Português do Brasil primeiro, com a estrutura de idiomas preparada desde o início. O inglês vem depois: o Sergio conduz estudos em inglês. | [site] + [backend] |
| NF-4 | Core Web Vitals no verde. Métricas sem rastreadores de terceiros (B12 da Zarp, ou nada). | [site] + [decisão] |
| NF-5 | **Sem anúncios, sem venda e sem monetização.** O projeto é filantrópico (dono, 2026-10-20). Neste tenant, o B22 W5 fica "nenhuma". | Decidido |

## 16. Regras do mercado: o que o B22 já cobre e o que falta

**O B22 já cobre:**

- níveis de confiança (Discourse);
- cotas por nível e limites de requisição;
- links duplicados e limite de velocidade por discussão (Lobsters);
- remoção silenciosa (shadow removal) e shadowban;
- fila, registro público e notas de moderação;
- AutoMod (Reddit), regras de domínio e modmail com recurso;
- denúncias com motivo, sem revelar quem denunciou;
- controle de multidão, anti-brigada e teto de karma por votante;
- revisões imutáveis, proteção, edições pendentes e patrulha (MediaWiki);
- aliases depois de mover uma página;
- verificação de idade e consentimentos com versão;
- exportação e apagamento;
- retenção legal (legal hold) e fluxo de CSAM;
- travamento otimista (`version`) e auditoria.

**Falta, para esta wiki:**

- a sincronização offline;
- a sessão de aparelho;
- a idempotência nas escritas;
- as marcas de remoção (tombstones);
- a normalização de palavrões;
- as discussões ligadas a qualquer assunto e as anotações;
- as citações e os backlinks da Codificação;
- o modo pesquisa;
- o papel de Revisor;
- os dados sensíveis;
- a lei brasileira;
- as licenças das imagens.

## 17. Lacunas a levar à correção do B22

| # | Lacuna | Seções aqui |
|---|---|---|
| L1 | Assunto genérico do post (`subjectType` / `subjectRef`), com discussão principal única por assunto | §4 |
| L2 | Anotações presas a trechos, com seletor de citação de texto e visibilidade de grupo ou pública | §4 (THR-3), §8 |
| L3 | Registro leve de trechos da Codificação (id, rótulo, URL, hash) | §1 (COD-6) |
| L4 | Citações: análise, conferência de trecho, `WikiLink` do tipo `citation` e backlinks em posts e comentários | §2 |
| L5 | Modo pesquisa completo (protocolo, sessão selada, replicação cega, dupla análise, conclusão) | §7 |
| L6 | Papel de Revisor e fluxo de revisão de pesquisa | §9, §7 |
| L7 | Palavrões: normalização, níveis, exceções, ação por comunidade e rótulos `profanity` / `insult` | §6 |
| L8 | Sincronização incremental com cursor e marcas de remoção | §11 |
| L9 | Chave de idempotência nas escritas de membro | §11 |
| L10 | Sessão de aparelho sem prazo absoluto, revogável, com lista de aparelhos | §11 |
| L11 | Apagamento forçado de caches locais (ordem legal, saída de grupo, apagamento de conta) | §6, §11 |
| L12 | Imagens: texto alternativo obrigatório, licença e origem, consentimento de pessoas, imagens em comentários | §5 |
| L13 | Privacidade de grupos no perfil (dado sensível) | §9 |
| L14 | Lei brasileira: LGPD (art. 11), Marco Civil, ECA Digital, notificação pela Lei 9.610 e intolerância religiosa | §14 |
| L15 | Plano de leitura e encontros de grupo | §8 |
