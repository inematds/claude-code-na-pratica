# Atribuição & Licenças — Biblioteca

Esta biblioteca reúne **skills, agentes e prompts** prontos para usar com o Claude Code.
Os prompts foram escritos para este curso. As skills e agentes incluídos são **open-source**
(licenças MIT/Apache) e mantidos pelos respectivos autores — os créditos e licenças estão abaixo.

## Incluído neste repositório (open-source)

| Item | Pasta | Origem (upstream) | Licença |
|------|-------|-------------------|---------|
| Agentes de SEO (18) | `agentes/seo/` | github.com/agricidaniel/claude-seo | MIT |
| Skills de SEO (25) | `skills/claude-seo/` | github.com/agricidaniel/claude-seo | MIT |
| Superpowers (14 skills) | `skills/superpowers/` | github.com/obra/superpowers | MIT |
| Power Design (princípios) | `skills/power-design/` | github.com/ItsssssJack/power-design | MIT |
| UI/UX Pro Max | `skills/ui-ux-pro-max/` | github.com/nextlevelbuilder/ui-ux-pro-max-skill | MIT |
| Banco de Prompts (48) | `prompts/` | Escrito para este curso (INEMA.CLUB) | — |

As imagens de exemplo das skills foram omitidas para manter o repositório leve; consulte o
upstream para os assets completos.

## Apenas referência (não redistribuído aqui — acesse no upstream)

- **anthropics/skills** — github.com/anthropics/skills (Apache-2.0)
- **awesome-claude-skills** — github.com/ComposioHQ/awesome-claude-skills (catálogo, centenas de skills)
- **awesome-agent-skills** — github.com/VoltAgent/awesome-agent-skills (MIT)
- **open-design** — github.com/nexu-io/open-design (Apache-2.0)
- **Hermes (agente pessoal open-source)** — github.com/NousResearch/hermes-agent (MIT)

## Como usar

- **Prompts:** copie e cole no Claude Code, ajustando os campos `[entre colchetes]`.
- **Skills:** coloque a pasta da skill em `~/.claude/skills/` (ou no diretório de skills do seu
  ambiente) e o Claude passa a reconhecê-la. Veja o `SKILL.md` de cada uma.
- **Agentes:** os arquivos `.md` definem agentes especializados; use-os como referência para
  criar/instalar agentes no seu fluxo.

Cada item mantém o arquivo `LICENSE` da sua origem. Respeite os termos de cada licença ao reutilizar.
