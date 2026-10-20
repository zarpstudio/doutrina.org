# 05 · Próximos passos e decisões abertas

## Estado em 2026-10-20

- **Ainda não há código.** O site é um projeto que vem depois e só toca o backend da Zarp na parte da wiki
  (B22).
- Esta pasta `docs/` é a primeira entrega: a visão, os requisitos, o acervo e as decisões.
- Os arquivos do site antigo (Jekyll) continuam no repositório, sem alteração, como referência.
- **Não ativar o GitHub Pages neste repositório.** O arquivo `CNAME` aponta para `doutrina.org`, que hoje é
  publicado pelo Sergio a partir de `sergioSHKLR/doutrina`.

## Decisões para o dono

Cada decisão traz um padrão provisório, que vale até o dono decidir.

| # | Decisão | Opções | Padrão até decidir |
|---|---|---|---|
| DO-1 | **Título da wiki** | Um nome próprio novo; um nome em parceria com o Sergio ("doutrina" é a marca dele); um nome descritivo. Nenhum deles pode sugerir endosso de federação ou instituição. | Nome de trabalho neutro em staging ("Wiki Espírita") |
| DO-2 | **Domínio e redirecionamento** | **(a)** O Sergio cede `doutrina.org`, e o LIBRUS vai para outro endereço (por exemplo, librus.app). **(b)** Domínio novo, com link ou redirecionamento a partir de `doutrina.org`, combinado com ele. **(c)** Um subdomínio (`wiki.doutrina.org`) apontado para o nosso site, se ele mudar o DNS. **(d)** Os dois sites convivem, cada um no seu domínio. O DNS de `doutrina.org`, `centro.` e `lde.` é dele. | Não mexer em DNS. A conversa com o Sergio vem antes. |
| DO-3 | **Como creditar e envolver o Sergio e o JhonnyBn** | Uma página de créditos e um `NOTICE`. O Sergio como cofundador, conselheiro editorial ou primeiro Revisor. Convite para o modo pesquisa e para os grupos em inglês. O JhonnyBn creditado como dono do repositório de base. | Crédito visível desde o primeiro rascunho do site |
| DO-4 | **Acesso para o amigo** | Colaborador no GitHub deste repositório (leitura, triagem ou escrita). Habilitar Issues, que hoje estão **desligadas** aqui. Acesso ao staging. Um papel na wiki (Revisor ou Equipe). | Nada foi alterado. A decisão é do dono. |
| DO-5 | **Licença da marcação do Sergio** | Usar a geração 2 (`doutrina-content`, CC BY-SA 4.0, compatível). Ou pedir ao Sergio que relicencie a geração 1 (hoje CC BY-NC-SA, não comercial). Ou fazer uma transcrição nova. | Geração 2, com o acordo dele |
| DO-6 | **Migração do conteúdo** | Fonte (DO-5). Escopo: o LDE primeiro, como o Sergio fez, depois o ESE para os grupos semanais, e os outros em seguida. Formato das referências (COD-2). Trazer ou não os links de consulta que ele fez (Wikipédia, Wikcionário, Luz). Limpeza obrigatória ([04](04-conteudo-e-licencas.md), §11). | Nada migra antes da limpeza jurídica |
| DO-7 | **Template do site** | **(a)** Este repositório vira o site Next.js open source, começando pelo template de wiki da Zarp (B22 W12), quando ele existir, mais os módulos da Codificação. **(b)** Um repositório novo a partir do `frontend_pages_zarp-template` (B20). **(c)** O template de wiki compartilhado, sem código próprio. | (a), porque o dono quer este repositório open source |
| DO-8 | **Licença do código do site** | MIT (máxima reutilização, como o LIBRUS); Apache-2.0 (com cláusula de patentes); AGPL-3.0 (quem rodar uma versão modificada tem de abrir as mudanças) | A decidir antes do primeiro commit de código |
| DO-9 | **"Modo só local"** | O site open source funciona **sem** o backend da Zarp (Codificação, busca e anotações locais) e liga a comunidade só quando há backend configurado. Ou o site exige o backend. | Ler, buscar e anotar funcionam sem backend (é o que o offline primeiro pede). A comunidade exige backend. |
| DO-10 | **Quem opera e com que natureza** | A Zarp, uma associação sem fins lucrativos, o dono com o Sergio. Isso decide o controlador na LGPD, o encarregado (DPO), os termos de uso, as obrigações do Marco Civil e se a licença NC permite o uso. | Sem fins lucrativos e sem anúncios (o tom do projeto do Sergio) |
| DO-11 | **Idade mínima** | 13, 16 ou 18 anos, com revisão jurídica (ECA e ECA Digital) | 16 para a comunidade, 18 para o modo pesquisa |
| DO-12 | **Notas privadas** | Só no aparelho. Sincronização opcional com a conta. Sincronização cifrada de ponta a ponta. | Só no aparelho, com exportar e importar |
| DO-13 | **Papéis finais e primeiros Revisores** | A proposta de [02](02-visao.md), §6. Quem forma o primeiro corpo de Revisores. | A proposta de §6, e a Equipe concede os papéis |
| DO-14 | **Regras do site e lista de palavrões** | O texto das regras ([03](03-requisitos.md), MOD-4) e quem mantém a lista pt-BR | A Equipe redige, e os Revisores comentam |
| DO-15 | **Idiomas** | Só português do Brasil, ou português e inglês desde o início | Português do Brasil, com o site preparado para mais idiomas |
| DO-16 | **Relação com o LIBRUS** | Convivência com links cruzados; integração (o LIBRUS como leitor e a wiki como comunidade); ou substituição | Convivência, combinada com o Sergio |
| DO-17 | **O site antigo neste repositório** | Manter até o site novo existir. Depois, guardar numa tag (`legacy-jekyll-2025-03`) e remover. Ou mover para `legacy/`. | Manter, sem alteração |
| DO-18 | **Sincronizar com o upstream** | Este fork está 59 commits atrás de `JhonnyBn/doutrina.org`. Como a tecnologia será refeita, sincronizar não traz ganho. As novidades de conteúdo estão no `doutrina-content`. | Não sincronizar |
| DO-19 | **Cronograma** | Ver a seção seguinte | Ordem proposta abaixo, sem datas |

## Ordem proposta (sem código até a fase E)

| Fase | O quê | Onde |
|---|---|---|
| **A, agora** | Esta documentação. As decisões DO-1 a DO-19. A conversa com o Sergio (pauta abaixo). | Este repositório |
| **B** | Levar as lacunas L1–L15 ([03](03-requisitos.md), §17) à **correção do B22**. A fase 0 do B22 (FAQ e comunidade) é a primeira peça do backend. A estimativa atual do B22, **antes da correção**, é de 172–238 horas de agente. | `backend_api_zarp-admin` |
| **C** | **Limpeza jurídica do acervo** ([04](04-conteudo-e-licencas.md), §11). **Levantamento open source** (`ZARP-OSS-FIRST.md`): sincronização offline primeiro, busca no aparelho, âncoras de anotação (W3C Web Annotation), listas de palavrões em pt-BR e leitores de livro em Next.js. Só pesquisa, sem código. | Este repositório (docs) |
| **D** | **Especificação das telas** (regra 3 do `ZARP-API-DESIGN.md`): as do site neste repositório e as do painel da Equipe no repositório do dashboard. | Este repositório + dashboard |
| **E** | **Primeira entrega do site:** a Codificação offline (leitor, busca, índice e anotações locais). Funciona **sem backend**. | Este repositório (Next.js) |
| **F** | A comunidade (B22 P1) e as discussões ligadas a qualquer conteúdo. Depois, a wiki (P2), os grupos de estudo e o **modo pesquisa**. Por fim, a segurança e o SEO (P3) e a auditoria final. | Backend + site |

## Pauta da conversa com o Sergio

1. Apresentar a visão ([02](02-visao.md)) como **continuação** do trabalho dele. Saber se ele quer participar,
   e em que papel.
2. **Licença:** o acordo para usar a marcação da geração 2 (CC BY-SA) ou relicenciar a geração 1 (NC).
3. **Domínio** `doutrina.org` e os subdomínios (DO-2), e o futuro do LIBRUS (DO-16).
4. **Crédito:** como ele e a Mai querem aparecer. Se podemos citar o HISTORY.md do arquivo privado dele.
5. **Conteúdo:**
   - o tradutor do CEU (Quintão ou Guillon);
   - a origem do `vine.png`;
   - a situação do índice geral (letras D–Z do LDE);
   - a remoção da Nota explicativa, das notas N.E. e dos PDFs da FEB.
6. **Segurança:** em `pages/meet.md` há um link público de anfitrião do Whereby, com token. Sugerir que ele
   invalide a sala, se ainda existir.
7. **Anotações:** autorização para importar as anotações dele no Hypothes.is como notas iniciais.

## O que não fazemos agora

- Escrever código, configurar build ou rodar os scripts antigos.
- Alterar as configurações do repositório (Pages, colaboradores, Issues), o DNS ou os domínios.
- Mexer nos arquivos existentes do site (README, `_config.yml`, `books/`, `pages/`…).
- Importar texto, PDFs, imagens ou anotações.
