# Padrão dos repositórios SAPIANS

A estrutura comum deve ajudar uma pessoa a localizar a fonte editável, preparar uma contribuição e interpretar a versão recebida. O padrão executável é o [golden path v0.8.0](https://github.com/wbendinelli/.github/tree/v0.8.0), identificado pelo commit `9a1212d9df466988781b0b3c4285d5dc61f58ea6`. Os perfis vêm de `doclint/config.json`; este guia não cria um schema paralelo.

## README por classe

| Classe | Perfil | Leitura obrigatória |
| --- | --- | --- |
| App, Service, Library | product | O que é, Quickstart, Scripts em tabela, Arquitetura, Status, Links |
| Docs, Content | content | O que é, Estrutura, Status, Links |
| IaC, Config | config | O que é, Como consumir, Versionamento, Links |
| Research | research | Overview, Quickstart, Reproducing, Citation, License |
| ClientDelivery | client | Ficha do projeto, O que é, Status datado, Links |

Classe descreve o tipo; tier descreve o contrato de governança declarado. Uma versão, tier ou badge isolado não comprova disponibilidade, suporte, segurança ou validação científica. Um projeto conserva suas diferenças reais de runtime, licença, idioma e contribuição.

O README identifica comandos existentes, dependências explícitas, fonte por artefato e estado observado. Guias especializados ficam em suas fontes e recebem links, em vez de cópias evolutivas concorrentes. O frontmatter do conteúdo da plataforma Docs não é imposto a READMEs ou runbooks.

## About e topics

A descrição do GitHub deve corresponder à finalidade do manifesto e do README, com prosa SAPIANS/VITA. O website aponta para um destino existente e pertinente; quando não há site publicado comprovado, usar a documentação do próprio projeto. Topics descrevem domínio, tipo e tecnologias presentes na fonte. Não usar termos de validação, disponibilidade ou conformidade como selo sem evidência.

## Tags e releases

Uma tag fixa uma revisão. Um release descreve essa revisão e, quando distribui arquivos, identifica versões, origem, licença, hashes e verificações. Não mover tags antigas nem reescrever resultados. O README separa a última versão publicada do que avançou na main.

Nos projetos com manifesto de release, a automação central prepara uma PR de versão/changelog. Aplicações, conteúdo, configuração e bibliotecas conservam suas unidades de versão; um repositório com vários pacotes documenta as versões de cada artefato. Pré-releases são identificadas como tal. Publicação de um release GitHub não implica implantação, publicação em registry ou alteração de dados.

Releases existentes preservam seu contexto. Quando ainda não há release, a primeira publicação precisa indicar o commit aceito e o escopo real, sem apresentar uma candidata ou kit documental como serviço estável. Materiais e ativos mantêm suas licenças; visibilidade do GitHub não redefine direitos.

## Conferência e manutenção

- README e `.sapians-repo.yml` coerentes com código e documentação.
- About, website e topics coerentes com essas fontes.
- Caller `docs-lint.yml` com ferramenta e regras na mesma tag `v0.8.0`.
- Links locais válidos; badges apontando para workflows, licenças e releases reais.
- Release/tag e manifesto coerentes com a unidade versionada; main posterior identificada.
- Legado com origem, SHA-256, sucessor e arquivos brutos fora dos parsers ativos.
- Revisão independente e checks do head antes da main; nenhum deploy/apply ou alteração jurídica por efeito desta organização.

O contrato é mantido junto das fontes dos projetos. Credenciais de automação, permissões e controles remotos possuem configuração própria; este guia não declara que estejam habilitados universalmente.
