# ⚡ Claude Code na Prática

Curso prático e gratuito sobre **Claude Code** — do zero ao produto. Sem jargão, sem
pré-requisito de programação. Você aprende fazendo e sai com projetos reais no ar.

🔗 **Acesse:** https://inematds.github.io/claude-code-na-pratica/ · Parte do [INEMA.CLUB](https://inema.club)

## O que é

Um site de curso autocontido (HTML + Tailwind via CDN + JS, sem build), no padrão
INEMA.CLUB v2, com **camada de aprendizagem**: progresso por tópico, "marcar como lido",
dúvidas, anotações, medidores por módulo/trilha/curso e painel "Minha jornada" — tudo salvo
no próprio navegador (localStorage). Tema claro/escuro incluso.

## Trilhas

| Trilha | Foco | Módulos |
|--------|------|---------|
| 🧱 **1 · Fundamentos** | Instalar, operar, memória e power features | 4 |
| 🚀 **2 · Construir** | Website, apps, "qualquer coisa" e design systems | 4 |
| 📈 **3 · Operar & Lucrar** | Agente pessoal, compliance, monetização e seu painel/OS | 4 |
| 📚 **Biblioteca** | 48 prompts + 60+ skills + 18 agentes, prontos pra usar | — |

Cada módulo traz: conceito com analogias, passo a passo, exemplo guiado, exercícios com
critério, **prompts prontos** (PT-BR), erros comuns e checklist.

## Estrutura

```
index.html                 # landing
assets/learn.css|js        # camada de aprendizagem (temas, progresso, jornada)
curso/trilha1..4/          # índices de trilha + páginas de módulo
biblioteca/                # prompts, skills e agentes (open-source) + ATTRIBUTION.md
```

## Biblioteca & licenças

Os prompts foram escritos para este curso. As skills e agentes incluídos são **open-source**
(MIT/Apache) dos respectivos autores — créditos e licenças em [`biblioteca/ATTRIBUTION.md`](biblioteca/ATTRIBUTION.md).

## Rodar localmente

```bash
python3 -m http.server 8000
# abra http://localhost:8000
```

---

Curso de pesquisa e educação · INEMA.CLUB · 2026
