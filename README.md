# Agentes de Análise de Edital de Concessão de RSU

## Uso rápido no claude.ai/code

Cada agente tem 2 fases (exceto o 04 que é tarefa única). Execute um por vez para evitar timeout.

| Comando | O que faz | Output |
|---------|-----------|--------|
| `siga agentes/01_concessao.md fase 1` | Extrai dispositivos sobre concessão | `01a_concessao_extracao.md` |
| `siga agentes/01_concessao.md fase 2` | Analisa + jurisprudência | `01b_concessao_analise.md` |
| `siga agentes/02_licitacao.md fase 1` | Extrai dispositivos sobre habilitação | `02a_licitacao_extracao.md` |
| `siga agentes/02_licitacao.md fase 2` | Analisa + jurisprudência | `02b_licitacao_analise.md` |
| `siga agentes/03_gestao_riscos.md fase 1` | Extrai gestão comercial + matriz de riscos | `03a_gestao_riscos_extracao.md` |
| `siga agentes/03_gestao_riscos.md fase 2` | Analisa + jurisprudência | `03b_gestao_riscos_analise.md` |
| `siga agentes/04_erros_inconsistencias.md` | Varredura integral de erros (tarefa única) | `04_erros_inconsistencias.md` |
| `siga agentes/05_caderno_encargos.md` | Análise técnica operacional (tarefa única) | `05_caderno_encargos.md` |

## Sequência recomendada

1. Rode as fases 1 dos agentes 01, 02 e 03 (podem ser em paralelo se não der timeout)
2. Rode o agente 04 (erros — não depende dos outros)
3. Rode as fases 2 dos agentes 01, 02 e 03 (usam os outputs das fases 1)
4. Rode o agente 05 se necessário (escopo técnico)
5. Leve TODOS os `.md` para o claude.ai e peça a consolidação

## Para novo edital

1. Crie repositório privado no GitHub
2. Copie o `CLAUDE.md` e a pasta `agentes/` para o repo
3. Faça upload dos PDFs
4. Acesse claude.ai/code, conecte o repo, execute os agentes
