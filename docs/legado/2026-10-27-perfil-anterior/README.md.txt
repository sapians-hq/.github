# .github

Community health files e defaults de organização para **sapians-hq**.

> **Tier:** `D` · **Classe:** `Config`

## O que é

Este repositório fornece, por herança, o que todo repositório da organização usa
sem precisar copiar: templates de issue e pull request, `CODEOWNERS` padrão,
política de segurança, e o perfil público da organização.

Um repositório que quiser divergir declara o seu próprio arquivo — o local
sempre vence o herdado.

## O que vive aqui

| Caminho | Efeito |
| :--- | :--- |
| `profile/README.md` | Página pública da organização em github.com/sapians-hq |
| `.github/ISSUE_TEMPLATE/` | Templates de issue em todos os repos da org |
| `.github/PULL_REQUEST_TEMPLATE.md` | Template de PR em todos os repos da org |
| `CODEOWNERS` | Revisor padrão quando o repo não define o seu |
| `SECURITY.md` | Política de divulgação de vulnerabilidade |

## Como consumir os reusable workflows

Os workflows de CI compartilhados **não vivem aqui** — vivem em
[`wbendinelli/.github`](https://github.com/wbendinelli/.github), que é público e
por isso pode ser chamado de qualquer organização.

```yaml
jobs:
  ci:
    uses: wbendinelli/.github/.github/workflows/ci-node.yml@v0.3.0
  brand:
    uses: wbendinelli/.github/.github/workflows/brand-lint.yml@v0.3.0
```

Disponíveis: `ci-node` · `ci-python` · `ci-python-uv` · `ci-terraform` ·
`security` · `brand-lint` · `release-please` · `lint`.

**Sempre pinar em tag**, nunca em `@main` — um bump no repo central não deve
quebrar CI de produção sem aviso.

## O padrão, e onde ele é decidido

Este repositório é a camada **executável**. O *porquê* — tiers, contratos de CI
por tier, política de gate — vive no handbook em
[`sapians-platform`](https://github.com/wbendinelli/sapians-platform/blob/main/handbook/golden-path.md).

Mudança de padrão é ADR + edição central, nunca cópia repo a repo.
