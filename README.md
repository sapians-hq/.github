# .github

[![Docs lint](https://github.com/sapians-hq/.github/actions/workflows/docs-lint.yml/badge.svg)](https://github.com/sapians-hq/.github/actions/workflows/docs-lint.yml)
[![Release](https://img.shields.io/badge/releases-GitHub-blue)](https://github.com/sapians-hq/.github/releases)

> **Tier:** `D` · **Classe:** `Config`

## O que é

Este repositório mantém o [overview público](profile/README.md), o [contrato documental](docs/padrao-de-repositorios.md) e os arquivos comunitários da `sapians-hq`. A implementação dos workflows compartilhados fica em [wbendinelli/.github](https://github.com/wbendinelli/.github), com versões próprias.

| Caminho | Papel |
| --- | --- |
| `profile/README.md` | Overview público da organização |
| `.github/ISSUE_TEMPLATE/` e `.github/PULL_REQUEST_TEMPLATE.md` | Templates comunitários, sujeitos às regras de herança do GitHub e aos arquivos locais de cada projeto |
| `SECURITY.md` e `CONTRIBUTING.md` | Canal de segurança e percurso geral de contribuição |
| `CODEOWNERS` | Propriedade deste repositório; não instala revisores automaticamente nos demais |
| `.sapians-repo.yml` | Classe, tier e descrição desta unidade |
| `docs/padrao-de-repositorios.md` | Estrutura e manutenção de README, About, topics e releases |

## Como consumir

Para entender a organização, comece pelo overview e pelo README do projeto. Para engenharia, adote o perfil derivado da classe em `.sapians-repo.yml`, confira os templates e use o validador central fixado:

```yaml
jobs:
  docs:
    uses: wbendinelli/.github/.github/workflows/docs-lint.yml@v0.8.1
    with:
      config-ref: v0.8.1
```

O pin de `uses` e `config-ref` precisa coincidir. Outros workflows conservam os contratos e pins próprios dos consumidores; atualizar documentação não autoriza modificar infraestrutura ou ambiente servido. A autoridade sobre método, marca, contratos e dados continua no repositório responsável.

## Versionamento

`version.txt`, manifesto e configuração de release identificam as versões deste conjunto de perfil, templates e documentação. A primeira versão organizada é `0.1.0`. Releases apontam para commits aceitos na main e descrevem o recorte entregue; não atestam publicação de produtos.

O fluxo de release prepara uma PR de versão/changelog; a publicação exige integração revisada e checks. Os releases do golden path `wbendinelli/.github` e dos produtos são independentes. O [padrão](docs/padrao-de-repositorios.md) detalha as regras; as fontes anteriores estão no [legado](docs/legado/2026-10-27-perfil-anterior/README.md).

## Links

- [Overview](profile/README.md) e [política documental](docs/padrao-de-repositorios.md).
- [Golden path v0.8.1](https://github.com/wbendinelli/.github/tree/v0.8.1).
- [Handbook](https://github.com/sapians-hq/sapians-handbook).
- [Segurança](SECURITY.md) e [releases](https://github.com/sapians-hq/.github/releases).

A herança dos arquivos comunitários segue a [lista e precedência oficiais do GitHub](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file). Licenças e CODEOWNERS conservam seu escopo local.
