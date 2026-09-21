# process_improve

## Propósito
Este repositório é um assistente completo de mapeamento e melhoria de processos para o Claude Code — do levantamento AS-IS em campo até o diagrama BPMN formal e a gestão do ciclo de vida BPM — implementado como uma família de 4 skills "especialista" em português, mais o `drawio-skill` como motor de diagramação, em `.claude/skills/`.

## As 4 skills + a skill de apoio
- **arquitetura-de-processos** — nível macro: cadeia de valor, hierarquia de processos, donos, interfaces, governança (framework APQC).
- **mapeamento-de-processos** — descoberta AS-IS de um processo específico: entrevistas, observação em campo (gemba), SIPOC, identificação de gaps/dores.
- **modelagem-de-processos** — formaliza um processo já descrito (AS-IS ou TO-BE) em um diagrama BPMN, delegando a geração visual ao `drawio-skill`.
- **gestao-de-processos-bpm** — ciclo de vida completo (descoberta → modelagem → análise → redesenho → automação → monitoramento).
- **drawio-skill** (skill de apoio, não parte da família de especialistas) — gera/edita diagramas `.drawio` nativos (BPMN e outras notações), com exportação para PNG/SVG/PDF. Requer Python 3 no ambiente; exportação nativa opcionalmente usa o binário do draw.io.

## Fluxo típico (pipeline)
`arquitetura-de-processos` (mapa macro) → `mapeamento-de-processos` (captura AS-IS de um processo específico) → `modelagem-de-processos` (formaliza em BPMN via `drawio-skill`) → `gestao-de-processos-bpm` (conduz o ciclo completo, incluindo redesenho/automação/monitoramento do mesmo processo).

## Como escolher a skill certa
| Pedido do usuário (exemplos) | Skill |
| --- | --- |
| "Como está estruturada nossa arquitetura de processos?", "quem é dono desse processo?", "monte a cadeia de valor" | `arquitetura-de-processos` |
| "entenda como o processo X funciona hoje", "mapeie o AS-IS da aprovação de despesas", "faça entrevistas sobre esse processo" | `mapeamento-de-processos` |
| "desenhe isso em BPMN", "transforme esse levantamento em um fluxograma", "faça o diagrama editável desse processo" | `modelagem-de-processos` (que aciona `drawio-skill`) |
| "redesenhe esse processo", "automatize esse fluxo", "monitore os KPIs desse processo", "gerencie o ciclo de vida BPM" | `gestao-de-processos-bpm` |
| Pedido direto por um diagrama `.drawio`/arquitetura técnica sem contexto de processo de negócio | `drawio-skill` diretamente |

## Observação
Este é um documento roteador/índice — consulte o `SKILL.md` e o `reference.md` de cada skill em `.claude/skills/<nome>/` para a metodologia completa.
