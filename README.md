# process_improve

Assistente de mapeamento e melhoria de processos para o [Claude Code](https://claude.com/claude-code) — do levantamento AS-IS em campo até o diagrama BPMN formal e a gestão do ciclo de vida BPM.

## O que este repositório faz

Ao abrir este projeto no Claude Code, você tem uma suíte de 4 skills especialistas em processos de negócio, mais uma skill de apoio para diagramação, todas em `.claude/skills/`:

| Skill | Papel |
| --- | --- |
| [`arquitetura-de-processos`](.claude/skills/especialista-em-arquitetura-de-processos) | Nível macro: cadeia de valor, hierarquia de processos, donos, interfaces, governança (framework APQC) |
| [`mapeamento-de-processos`](.claude/skills/mapeamento-de-processos) | Descoberta AS-IS de um processo específico: entrevistas, observação em campo (gemba), SIPOC, gaps e dores |
| [`modelagem-de-processos`](.claude/skills/modelagem-de-processos) | Formaliza um processo descrito (AS-IS ou TO-BE) em um diagrama BPMN |
| [`gestao-de-processos-bpm`](.claude/skills/especialista-em-gestao-de-processos-bpm) | Ciclo de vida completo: descoberta → modelagem → análise → redesenho → automação → monitoramento |
| [`drawio-skill`](.claude/skills/drawio-skill) | Skill de apoio: gera/edita diagramas `.drawio` nativos e editáveis (BPMN e outras notações), usada por `modelagem-de-processos` |

## Como usar

1. Abra este repositório no Claude Code.
2. Descreva o que você precisa em português (ou inglês) — a skill certa é acionada automaticamente pelo pedido. Exemplos:
   - *"mapeie como funciona hoje a aprovação de despesas"* → `mapeamento-de-processos`
   - *"transforme esse levantamento em um fluxograma BPMN"* → `modelagem-de-processos` (que aciona `drawio-skill`)
   - *"como está estruturada nossa arquitetura de processos?"* → `arquitetura-de-processos`
   - *"redesenhe e automatize esse processo"* → `gestao-de-processos-bpm`
3. Veja [`CLAUDE.md`](CLAUDE.md) para o guia completo de qual skill usar em cada situação, e o `SKILL.md`/`reference.md` de cada pasta para a metodologia detalhada.

## Pipeline típico

```
arquitetura-de-processos  →  mapeamento-de-processos  →  modelagem-de-processos  →  gestao-de-processos-bpm
   (mapa macro)                (captura AS-IS)             (formaliza em BPMN,         (ciclo completo:
                                                              via drawio-skill)          redesenho/automação/
                                                                                          monitoramento)
```

## 📁 Estrutura de Projetos

Este repositório está organizado por **projetos de mapeamento**. Cada projeto tem seu próprio espaço com coleta de dados, modelagem e redesenho.

### Projetos Ativos

| Projeto | Status | Pasta | Descrição |
|---------|--------|-------|-----------|
| **PCP — Fechamento de OP** | 🟡 Coleta de Dados | [`projetos/pcp_fechamento_op/`](projetos/pcp_fechamento_op/) | Mapeamento do processo de fechamento de Ordem de Produção no departamento de PCP — taxa de erro 33%, falta confiabilidade de dados |

### Estrutura de um Projeto

Cada projeto em `projetos/<nome>/` segue esta estrutura:

```
projetos/<nome>/
├── 01_coleta_dados/          # Fase 1: Descoberta AS-IS
│   ├── roteiros/             # Roteiros de entrevista
│   ├── gemba_walk/           # Checklists e observações in loco
│   ├── analises/             # Consolidação de dados
│   └── README.md             # Status e achados
│
├── 02_modelagem/             # Fase 2: Formalização em BPMN
│   ├── diagrama_asis.drawio  # Diagrama AS-IS editável
│   ├── diagrama_asis.png     # Exportação PNG
│   └── [documentação]
│
├── 03_redesenho/             # Fase 3: Otimização & Proposta TO-BE
│   ├── proposta_melhorias.md # Recomendações
│   ├── diagrama_tobe.drawio  # Diagrama TO-BE
│   └── plano_implementacao.md
│
└── README.md                 # Índice e status do projeto
```

### Como Consultar um Projeto

Abra o `README.md` da pasta do projeto para ver:
- Status atual
- Achados principais
- Próximos passos
- Arquivos de cada fase

**Exemplo:** [`projetos/pcp_fechamento_op/README.md`](projetos/pcp_fechamento_op/README.md)

## Pré-requisitos

- [Claude Code](https://claude.com/claude-code)
- Python 3 no ambiente (usado pelos scripts do `drawio-skill` para gerar/validar os diagramas `.drawio`)

## Créditos

A skill `drawio-skill` é vendorizada a partir do repositório [Agents365-ai/drawio-skill](https://github.com/Agents365-ai/drawio-skill) (MIT License — ver [LICENSE](.claude/skills/drawio-skill/LICENSE) na própria pasta da skill). As demais skills foram desenvolvidas para este repositório.
