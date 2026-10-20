# 02 · A visão: uma wiki para continuar o trabalho de Kardec

## 1. A missão

**Continuar o trabalho científico de Allan Kardec**, seguindo o método de *O Livro dos Médiuns*, por meio de
uma **wiki colaborativa no estilo do Reddit**.

Kardec tratou o Espiritismo como ciência de observação. O próprio texto deixa a porta aberta para que o
trabalho continue:

> Caminhando de par com o progresso, o Espiritismo jamais será ultrapassado, porque, se novas descobertas
> lhe demonstrassem estar em erro acerca de um ponto qualquer, ele se modificaria nesse ponto. Se uma
> verdade nova se revelar, ele a aceitará.
>
> *A Gênese*, cap. I, item 55 (trad. Guillon Ribeiro)

O site do Sergio criou o melhor lugar para **estudar** a Codificação. O projeto novo quer um lugar onde a
comunidade **produza conhecimento** a partir dela: estudando junta, citando com precisão, discutindo com
método e registrando pesquisa, como Kardec fazia com a Sociedade Parisiense e a *Revista Espírita*.

## 2. Por que é uma evolução, não um recomeço

| | Sergio (doutrina.org / LIBRUS) | Projeto novo |
|---|---|---|
| Objetivo | Ler e estudar o texto original, sem simplificar | Isso, **e mais** continuar o trabalho: discutir, pesquisar e documentar |
| Quem produz | Um editor (Sergio) | Uma comunidade com papéis e revisão |
| Onde fica a conversa | Fora do site (Hypothes.is) | **Dentro do site**: discussões ligadas a qualquer conteúdo |
| Unidade central | O livro | **A wiki**: páginas de conhecimento com histórico, e a Codificação como base citável |
| Consulta | Sites de terceiros num `iframe` | Links e citações que o site resolve (Codificação, wiki, glossário), e links externos como referência |
| Grupos | Perfil "Instrutor" e grupos privados no Hypothes.is | Grupos de estudo e de pesquisa como comunidades do próprio site |
| Tecnologia | Jekyll, depois Vite e GitHub Pages | Next.js no Coolify (template da Zarp, B20) e o backend da Zarp para comunidade e wiki (B22) |

O dono resumiu assim (2026-10-20): **a tecnologia vem depois; o que importa é o propósito.** Muito do
repositório antigo será abandonado. As funções serão recriadas em Next.js, e **a wiki será o núcleo, por trás
de tudo**.

## 3. O método d'*O Livro dos Médiuns* como princípio de produto

O site não ensina o método: ele o **torna prática**. Cada princípio vira uma regra de produto.

| Princípio de Kardec | Onde está | O que vira no produto |
|---|---|---|
| **Estudo sério antes da prática.** O Espiritismo "não pode, como nenhuma outra ciência, ser aprendido a brincar". | LDM, 1ª parte, cap. III (Método), item 18 | Um caminho de estudo (FAQ, trilhas, grupos) antes do modo pesquisa. O modo pesquisa exige um nível de confiança e um compromisso com as regras. |
| **Os fatos e a razão antes da autoridade.** Nenhuma comunicação vale pelo nome que assina. | LDM, 2ª parte, cap. XXIV (Identidade dos Espíritos) e cap. XXVII (Contradições e mistificações) | Uma comunicação registrada é sempre **dado em análise**, nunca verdade publicada. O site mostra lado a lado o fato, a análise e a crítica. |
| **Controle universal do ensino dos Espíritos.** "Uma só garantia séria existe para o ensino dos Espíritos: a concordância que haja entre as revelações que eles façam espontaneamente, servindo-se de grande número de médiuns estranhos uns aos outros e em vários lugares." | ESE, Introdução, II | **Replicação independente** no modo pesquisa. Vários grupos respondem à mesma pergunta **sem ver as respostas dos outros**. Depois o site compara a concordância. |
| **Perguntas bem formuladas.** | LDM, 2ª parte, cap. XXVI (Perguntas que se podem fazer aos Espíritos) | Modelos de protocolo com a pergunta escrita antes da sessão, que não pode ser editada depois. |
| **Reuniões sérias e organizadas.** | LDM, 2ª parte, caps. XXIX e XXX (Reuniões e sociedades espíritas; Regulamento da Sociedade Parisiense) | Grupos com coordenador, regras próprias, ata da sessão e registro de presença. |
| **Fé raciocinada.** "Fé inabalável só o é a que pode encarar frente a frente a razão, em todas as épocas da Humanidade." | ESE, cap. XIX, item 7 (também na folha de rosto) | A moderação e a revisão julgam **argumento e fonte**, não opinião. Toda afirmação doutrinária na wiki pede citação da Codificação. |
| **A Codificação como base, sem fechar questão.** | GEN, cap. I, item 55 | O texto de Kardec é protegido: ninguém o edita. As páginas da wiki *sobre* ele são abertas e versionadas, e as divergências ficam documentadas em vez de apagadas. |

## 4. O que o site atual mantém

1. **A missão e o tom:** estudo sério, fidelidade ao texto, fraternidade e respeito aos detentores de
   direitos. **O projeto é filantrópico** (dono, 2026-10-20): a Zarp não tem interesse comercial nele. Não
   há venda, anúncios nem monetização, como no projeto do Sergio.
2. **A Codificação no centro:** as cinco obras, legíveis, com **endereço estável para cada questão e cada
   item**. Sem isso não há citação.
3. **As vozes identificadas:** Espírito (com assinatura), Kardec e texto bíblico.
4. **Ler, consultar e anotar no mesmo lugar.** É a ideia das quatro colunas do Sergio, recriada no site
   novo: ao lado do texto ficam a consulta (glossário, wiki, referências) e a conversa (discussões e
   anotações).
5. **O índice geral** de cada obra, e no futuro um índice combinado das cinco. O Sergio já o descrevia como
   "um compêndio de extremo valor para pesquisadores, palestrantes e líderes de estudo em grupo".
6. **O grupo de estudo como uso principal.** O próprio Sergio dizia que o melhor uso era "um estudo em grupo,
   liderado por pessoa versada na doutrina".
7. **O cuidado de leitura:** tipografia ajustável, modo escuro e uma tela sem distrações.
8. **O crédito** ao Sergio, à Mai e aos voluntários, de forma visível no site novo.

## 5. O que muda

1. **A tecnologia.** Next.js no Coolify, a partir do template de sites da Zarp (B20). O backend da Zarp cuida
   da comunidade e da wiki (B22). Jekyll, LIBRUS, `combined.js` e os scripts ficam como referência.
2. **Sem dependências de terceiros no núcleo:**

   | Antes | Depois |
   |---|---|
   | Hypothes.is | Anotações e discussões do próprio site, ligadas a um trecho |
   | Crisp | Contato pelo site e pelos canais da Zarp, sem chat de terceiros (decisão aberta) |
   | PushEngage | Notificações do backend (inbox e e-mail) |
   | Whereby / JaaS | Link de reunião no grupo de estudo (a ferramenta de vídeo não é núcleo) |
   | Google Forms | Formulário do site (backend) |
   | Painel em `iframe` | Cartões de consulta próprios (verbete da wiki, glossário, citação) e links externos que abrem em nova aba |

3. **A wiki é o núcleo.**
   - Páginas de conhecimento com histórico imutável e autoria: temas, conceitos, biografias, glossário, casos
     e pesquisas.
   - Cada página tem a sua discussão.
   - A Codificação fica como texto protegido, mas **citável e comentável** trecho a trecho.
4. **Comunidade no estilo do Reddit.** Comunidades por tema e por grupo, posts com texto, link ou imagem,
   comentários em árvore, votos, karma e moderação. A conversa deixa de morar fora.
5. **Discussões ligadas a qualquer conteúdo:** um post do blog, um vídeo, uma página da wiki, **uma questão do
   LDE ou um item do LDM**.
6. **O modo pesquisa:** o método de Kardec como fluxo de trabalho (§3 e [03](03-requisitos.md)).
7. **Poucos papéis, cada um com função especial.** A proposta abaixo é para o dono decidir.
8. **Offline primeiro e código aberto** (dono, 2026-10-20). Ver §5.1.
9. **Mobile de verdade.** O site deve funcionar bem no celular em pé. As gerações anteriores pediam para
   deitar o celular ou bloqueavam a tela.
10. **Regras de negócio do mercado.** O dono pediu que o backend cubra o máximo das regras já usadas na
    indústria: níveis de confiança, cotas, fila e registro de moderação, recurso, denúncias, fluxos legais e
    proteção de menores. O B22 já traz boa parte disso. O que falta está em [03](03-requisitos.md).

### 5.1 Offline primeiro, pouca dependência do backend, código aberto

O que o dono pediu (2026-10-20):

- **Offline primeiro.** Tudo o que o usuário tem fica guardado no aparelho. Se a internet cair, o site
  continua funcionando.
- **O login não expira.** Sem internet, a pessoa continua logada. Quando a conexão volta, o backend envia o
  que mudou e o site fica atualizado.
- **Reduzir ao máximo a dependência do backend.** O repositório do doutrina.org será **open source**.

O que isso significa:

1. **Ler e estudar não dependem de servidor.**
   - A Codificação, o índice e a interface vêm no próprio site e ficam guardados para uso offline (PWA).
   - As marcações pessoais ficam no aparelho: favoritos, grifos, notas, progresso de leitura e rascunhos.
   - O `lde-q` do Sergio já seguia essa linha: marcações locais, com sincronização opcional.
2. **A comunidade usa o backend, mas não para quando ele some.**
   - Discussões, páginas da wiki e grupos já vistos ficam guardados e podem ser lidos offline.
   - O que a pessoa escreve offline (comentário, post, edição, anotação) entra numa **fila local** e é
     enviado quando a conexão volta.
   - Ao sincronizar, o backend aplica as regras (moderação, cotas, conflito de edição) e devolve o resultado.
3. **O backend é a fonte da verdade do que é público e compartilhado.** O aparelho é a fonte da verdade do
   que é pessoal. Quando a pessoa reconecta, o aparelho pede "o que mudou desde a última vez": conteúdo novo,
   editado, removido ou retirado por ordem legal. Tudo isso é aplicado no cache local.
4. **Código aberto.**
   - O repositório do site é público. Não pode haver segredo no cliente: nenhuma chave de API privada,
     nenhuma regra que só valha porque o código é fechado.
   - Toda regra de negócio que importa (moderação, permissão, cotas) **mora no backend**. O cliente só pode
     antecipar avisos, por exemplo um aviso de palavrão antes de enviar.
   - O backend da Zarp continua privado e é usado pela API pública documentada. Se o site também deve
     funcionar sem o backend da Zarp, em "modo só local", é decisão aberta em
     [05](05-proximos-passos.md).
5. **O login que não expira tem custo de segurança.** Num aparelho roubado ou compartilhado, a sessão
   continua aberta. A proposta segue o padrão do mercado:
   - uma **sessão de aparelho sem prazo fixo**, renovada a cada uso;
   - **revogável** pelo servidor (sair, trocar a senha, banimento, "sair de todos os aparelhos");
   - um botão "sair e apagar os dados deste aparelho".
   - Offline, o aparelho não tem como saber da revogação. Ele descobre na próxima sincronização e então
     limpa o que for preciso.

   Os detalhes estão em [03](03-requisitos.md), §11.

## 6. Papéis (proposta)

Poucos tipos de usuário, cada um com uma função. No backend, todos são o mesmo `User`, com uma extensão por
tenant (D33). A tabela mostra como cada papel se encaixa no B22.

| Papel | Função especial | No B22 (no `main`) |
|---|---|---|
| **Visitante** | Lê tudo o que é público: Codificação, wiki e discussões abertas. | Anônimo, `@PublicContent()` |
| **Membro** | Comenta, posta, vota, anota, sugere edições na wiki e participa de grupos. Ganha confiança com o tempo. | `WikiMemberProfile` + níveis de confiança TL0–TL3 |
| **Coordenador de grupo** | Cria e conduz um grupo de estudo ou de pesquisa (privado ou restrito), aprova participantes, marca sessões e abre protocolos de pesquisa. | Moderador de uma comunidade (`CommunityModerator`) |
| **Revisor** | Guarda a qualidade doutrinária e científica: aprova edições pendentes na wiki, valida citações, revisa protocolos e conclusões, e marca divergências. | TL3 ou moderador com permissão `wiki`. A revisão de pesquisa é **[lacuna B22]**. |
| **Moderador** | Aplica as regras de convivência: fila, remoções, sanções e recursos. | Moderador de comunidade ou `site_moderator` |
| **Equipe** | Administra o site: corpus da Codificação, regras, casos legais e configurações. | Staff do tenant (`AdminJwtGuard` → `wiki.*`) |

Um mesmo membro pode acumular papéis, por exemplo Revisor e Coordenador. Os papéis especiais são concedidos
pela Equipe, nunca por autoatribuição.

## 7. Como o site se organiza (esboço, não é especificação de tela)

- **Codificação:** as cinco obras, com navegação por parte, capítulo e questão ou item. Cada trecho mostra o
  número de discussões e citações e o botão "discutir este trecho".
- **Wiki:** páginas temáticas, glossário, biografias (Kardec, médiuns, Espíritos que assinam), casos do CEU e
  conceitos. Cada página tem histórico, citações e discussão.
- **Comunidade:** o feed e as comunidades por tema (Mediunidade, Moral, Ciência e Espiritismo, Dúvidas
  (FAQ)…).
- **Pesquisa:** protocolos abertos, em coleta, em análise e concluídos, e a comparação de concordância.
- **Grupos:** grupos de estudo e de pesquisa, com cronograma de leitura e sessões.
- **Blog e vídeos:** conteúdo da equipe (CMS da Zarp), cada item com a sua discussão.
- **Perfil:** handle, bio, grupos, contribuições, karma e selos de papel.

## 8. Princípios que não negociamos

1. **O texto de Kardec é intocável no site.** Correções de transcrição passam pela Equipe, com histórico.
   Interpretações ficam na wiki, nunca no texto.
2. **Comunicação mediúnica é dado, não autoridade.** Ela sempre aparece com o contexto (grupo, médium sob
   pseudônimo, data, pergunta) e com a análise.
3. **Ninguém é exposto.** Médiuns e participantes usam pseudônimo se quiserem. Os dados pessoais seguem a
   LGPD. Nada de evocar ou expor pessoas falecidas identificáveis sem o consentimento da família.
4. **Sem promessa de cura e sem conselho médico** em nome do Espiritismo. As regras do site proíbem isso, e a
   moderação aplica.
5. **Fraternidade na moderação.** As regras são claras, a remoção sempre tem motivo e todo membro pode
   recorrer.
6. **Crédito a quem veio antes:** Sergio, Mai, JhonnyBn, os voluntários, a FEB como editora de referência
   das traduções e as fontes consultadas.
7. **O estudo nunca depende de conexão.** Ler, buscar e anotar funcionam offline. O que é pessoal fica com a
   pessoa, no aparelho dela.
8. **Aberto por padrão.** O site é open source, e nenhuma regra importante depende de o código estar escondido.
