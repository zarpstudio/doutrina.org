# Documentação do projeto: a wiki do Espiritismo

Esta pasta guarda a visão, os requisitos e as decisões do novo projeto que nasce do doutrina.org.
**Aqui só há documentação. Não há código por enquanto.** O site é um projeto que vem depois, e ele só
toca o backend da Zarp na parte da wiki.

## A missão em uma frase

**Continuar o trabalho científico de Allan Kardec**, seguindo o método de *O Livro dos Médiuns*, por meio
de uma wiki colaborativa no estilo do Reddit, em que a comunidade estuda, cita, discute e pesquisa a partir
da Codificação.

## O ponto de partida

O doutrina.org é obra de **Sergio** ([@sergioSHKLR](https://github.com/sergioSHKLR)), com a esposa **Mai**,
e de alguns voluntários. Desde 2023 ele transcreveu à mão as cinco obras básicas e criou um leitor de estudo
com colunas, links de consulta e anotações. Este repositório é um fork desse trabalho, que estava em
[`JhonnyBn/doutrina.org`](https://github.com/JhonnyBn/doutrina.org) e foi transferido de `itskelme` para
`zarpstudio`.

O projeto do dono **é uma evolução do projeto do Sergio**. Daqui levamos sobretudo **o propósito e a
missão**. A tecnologia de hoje (Jekyll, scripts, painéis e dependências de terceiros) será reconstruída em
Next.js, com a wiki como núcleo. Fica como referência, não como base de código.

## O que o dono decidiu (2026-10-20)

1. **O propósito vem primeiro, a tecnologia depois.** Muito deste repositório será abandonado, inclusive as
   dependências de terceiros. As funções serão recriadas em Next.js.
2. **A wiki é o núcleo**, por trás de tudo. É nela que o trabalho de Kardec continua.
3. **Poucos tipos de usuário, com funções especiais** (proposta em [02](02-visao.md), §6).
4. **O backend cobre o máximo de regras de negócio já usadas na indústria** (ver [03](03-requisitos.md), §16).
5. **Offline primeiro.** Os dados ficam no aparelho, e o login não expira: sem internet, a pessoa continua
   logada. Quando a conexão volta, o backend atualiza o que mudou. A ideia é reduzir ao máximo a dependência
   do backend.
6. **Este repositório será open source.**
7. **A Zarp não tem interesse comercial no doutrina.org.** O projeto é filantrópico: sem venda, sem anúncios
   e sem monetização.

## Documentos

| Arquivo | O que tem |
|---|---|
| [01-legado-sergio.md](01-legado-sergio.md) | O que existe hoje: créditos, história, estrutura do site e do conteúdo, pontos fortes, limites e licenças. Inclui a geração mais nova do Sergio (LIBRUS), que não está neste fork. |
| [02-visao.md](02-visao.md) | A visão do dono como evolução: a wiki no estilo do Reddit para continuar o trabalho de Kardec, o método d'*O Livro dos Médiuns* como princípio de produto, o que fica do site atual e o que muda. |
| [03-requisitos.md](03-requisitos.md) | Requisitos de produto: moderação (com palavrões), discussões ligadas a qualquer conteúdo, posts com imagens, modo pesquisa, grupos de estudo, citações da Codificação, perfis e papéis. Cada item diz se é do backend (B22) ou do site. |
| [04-conteudo-e-licencas.md](04-conteudo-e-licencas.md) | O acervo: o que é domínio público, que traduções podem ser usadas e o que precisa de permissão ou deve sair. |
| [05-proximos-passos.md](05-proximos-passos.md) | Decisões abertas para o dono e próximos passos, ainda sem código. |

## Relação com o backend da Zarp

A parte de comunidade e wiki é especificada no backend, no repositório
[`zarpstudio/backend_api_zarp-admin`](https://github.com/zarpstudio/backend_api_zarp-admin):

- **B22, tenant `WIKI` e comunidades no estilo do Reddit:**
  [`docs/superpowers/specs/2026-10-19-zarpos/22-wiki-and-community.md`](https://github.com/zarpstudio/backend_api_zarp-admin/blob/main/docs/superpowers/specs/2026-10-19-zarpos/22-wiki-and-community.md).
  > **Atenção:** o B22 que está no `main` (lido em 2026-10-20) ainda cita o wiki do Spigot como segunda
  > instância. Ele está sendo corrigido agora: a segunda instância é **a wiki do Espiritismo**, com um
  > **modo pesquisa** baseado no método de Kardec, e o plano de FAQ e comunidade de 2026-09-19 entra como
  > **fase 0**. Nomes podem mudar na correção (por exemplo, um módulo base `zarp-community` e um
  > `CommunityProfile` no lugar de `WikiMemberProfile`). Onde estes documentos citam seções do B22, valem as
  > seções do `main`. As lacunas que achamos estão marcadas com **[lacuna B22]** em
  > [03-requisitos.md](03-requisitos.md).
- **D33, "Core entities and extensions"** (`AGENTS.md`): o membro é um `User` global com uma extensão por
  tenant, nunca uma conta paralela.
- **`ZARP-API-DESIGN.md`**: rotas desenhadas a partir da tela, resposta que se adapta ao ator, e nenhuma
  rota sem a especificação da tela.
- **B20, `zarp-websites`** (`20-zarp-websites.md`): os sites da Zarp rodam no Coolify, cada um no seu
  repositório, criados a partir de um template.

## Fontes consultadas (2026-10-20)

- Este fork (`main`, último commit de 2025-03-04, 2.155 commits), lido sem executar nada.
- O upstream [`JhonnyBn/doutrina.org`](https://github.com/JhonnyBn/doutrina.org), que está 59 commits à frente
  (até 2026-07-04).
- Os repositórios públicos do Sergio da geração LIBRUS: `doutrina-content`, `librus-linker`, `librus-shell`,
  `doutrina`, `librus`, `centro`, `lde-q`. Também o aviso legal público em
  [shklr.org/legal](https://shklr.org/legal).
- O repositório original do Sergio, hoje `sergioSHKLR/doutrina-archive` (**privado**). Foi lido só para
  entender a história. Nada dele é copiado aqui.
- A API pública do Hypothes.is, para contar as anotações públicas no domínio.

## Como manter

- Escrever em português do Brasil, a língua do dono. Os nomes de arquivo podem ficar em inglês.
- Quando uma decisão de [05-proximos-passos.md](05-proximos-passos.md) for tomada, registrar a data e quem
  decidiu, e atualizar os outros documentos que dependem dela.
- Nada nesta pasta altera os arquivos do site antigo (README, `_config.yml`, `books/` etc.).
