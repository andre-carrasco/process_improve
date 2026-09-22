# 📊 Projeto: PCP — Fechamento de Ordem de Produção

**Status:** 🟡 Em Coleta de Dados  
**Última atualização:** 22/09/2026  
**Responsável:** André Carrasco  
**Objetivo:** Mapear, analisar e otimizar o processo de fechamento de OP (Ordem de Produção) do departamento de PCP

---

## 📋 Escopo

**Processo:** Fechamento de Ordem de Produção no SAP  
**Atores Principais:**
- Letícia Ramos (Programadora PCP + Operacional Fechamento)
- Líderes/Encarregados de Linha (Coleta de dados)
- Departamento PCI (Controle de Insumos)

**Problema Central:** Taxa de erro de 33% nas OPs (5 de 15 por semana precisam revisão) — falta confiabilidade nos dados fornecidos pela linha

---

## 📁 Estrutura do Projeto

```
pcp_fechamento_op/
├── 01_coleta_dados/          # Fase de descoberta AS-IS
│   ├── roteiros/             # Roteiros de entrevista
│   │   ├── roteiro_entrevista_fechamento_op.md        (✅ Respondido - Letícia)
│   │   └── roteiro_entrevista_encarregado.md          (⏳ Pendente - após gemba)
│   ├── gemba_walk/           # Observação in loco
│   │   ├── checklist_gemba_walk_fechamento_op.md      (⏳ Pendente)
│   │   └── [fotos e observações da gemba]
│   └── analises/             # Consolidação de dados
│       ├── analise_asis_fechamento_op.md              (✅ Consolidado)
│       └── [futuros detalhamentos]
│
├── 02_modelagem/             # Formalização em BPMN
│   ├── diagrama_asis.drawio
│   ├── diagrama_asis.png
│   └── [versões iterativas]
│
├── 03_redesenho/             # Otimização & TO-BE
│   ├── proposta_melhorias.md
│   ├── diagrama_tobe.drawio
│   └── plano_implementacao.md
│
└── README.md                 # Este arquivo
```

---

## 🔄 Fase Atual: 01 — Coleta de Dados (AS-IS)

### ✅ Concluído
- [x] **Entrevista com Letícia Ramos** (Programadora + Fechamento)
  - Arquivo: `01_coleta_dados/roteiros/roteiro_entrevista_fechamento_op.md`
  - Duração: 60 min
  - Data: 22/09/2026

- [x] **Análise AS-IS Consolidada**
  - Arquivo: `01_coleta_dados/analises/analise_asis_fechamento_op.md`
  - Inclui: SIPOC, fluxo detalhado, volumetria, gaps críticos

### ⏳ Pendente
- [ ] **Gemba Walk** (Observação in loco)
  - Checklist: `01_coleta_dados/gemba_walk/checklist_gemba_walk_fechamento_op.md`
  - Responsável: André Carrasco
  - Duração estimada: 4-6 horas (um turno)
  - Próximo encarregado: ___________________

- [ ] **Entrevista com Encarregado de Linha**
  - Arquivo: `01_coleta_dados/roteiros/roteiro_entrevista_encarregado.md`
  - Data prevista: Após gemba walk
  - Duração: 30 min

- [ ] **Entrevista com Departamento PCI**
  - Roteiro: (será criado)
  - Objetivo: Entender fluxo de entrada/consumo/sobra de insumos

---

## 🎯 Achados Principais (até agora)

### Dores Identificadas
1. **Taxa de erro 33%** — 5 de 15 OPs por semana precisam revisão
2. **Consumo de insumo não verificado** — apenas estimado na ficha técnica
3. **Foto só no final** — impossibilita rastreabilidade desde o início
4. **Falta padronização** — "cada encarregado faz à sua maneira"
5. **Responsabilidade difusa** — OP finalizada em turno A, informada em turno B

### Gaps Críticos
- ❌ Não há foto ANTES da produção
- ❌ Não há contagem do que sobra de insumo
- ❌ Departamento PCI não verifica entrada/saída física
- ❌ Divergências entre contadores de equipamento não são detectadas

---

## 📚 Arquivos de Referência

### Documentos do Projeto
- **Análise AS-IS**: `01_coleta_dados/analises/analise_asis_fechamento_op.md`
- **Roteiro Letícia**: `01_coleta_dados/roteiros/roteiro_entrevista_fechamento_op.md`
- **Checklist Gemba**: `01_coleta_dados/gemba_walk/checklist_gemba_walk_fechamento_op.md`
- **Roteiro Encarregado**: `01_coleta_dados/roteiros/roteiro_entrevista_encarregado.md`

### Referência Global
- **Instruções do Repositório**: `../../CLAUDE.md`
- **Skills Disponíveis**: `.claude/skills/`

---

## 🚀 Próximos Passos

### Imediato (Esta Semana)
1. Realizar Gemba Walk (4-6h)
2. Preencher checklist durante observação
3. Entrevistar encarregado após gemba (30 min)

### Curto Prazo (Próximas 2 Semanas)
1. Entrevistar departamento PCI
2. Consolidar dados em SIPOC expandido
3. Documentar fluxo completo com pontos de decisão

### Médio Prazo (Final de Setembro)
1. Formalizar em diagrama BPMN (AS-IS)
2. Validar diagrama com Letícia e encarregados
3. Iniciar análise de melhorias (TO-BE)

### Longo Prazo (Outubro)
1. Propor redesenho
2. Planejar implementação
3. Definir métricas de sucesso

---

## 📞 Contatos & Stakeholders

| Papel | Nome | Departamento | Contato |
|-------|------|-------------|---------|
| Programadora PCP | Letícia Ramos | PCP | - |
| Encarregado Linha | (a confirmar) | Produção | - |
| Gerente PCI | (a confirmar) | PCI | - |

---

## 📝 Notas

**Observação importante (por Letícia):**
> "Falta padronização e cumprimento das obrigações de todos"

Esta é a síntese do problema — não é apenas processo, é também disciplina operacional.

---

**Criado em:** 22/09/2026  
**Última alteração:** 22/09/2026
