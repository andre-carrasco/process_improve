# 📊 Análise AS-IS: Fechamento de Ordem de Produção

**Data:** 22/09/2026  
**Entrevistado:** Letícia Ramos (Programadora PCP + Operacional Fechamento)  
**Duração:** 60 min  
**Elaborado por:** André Carrasco

---

## 1️⃣ SIPOC — Escopo do Processo

| Elemento | Descrição |
|----------|-----------|
| **Fornecedores** | 1. Departamento Comercial (demanda co-packer); 2. Sistema SAP MRP (demanda marca própria); 3. Líderes de Linha (dados de produção) |
| **Entradas** | Demanda comercial (15-20 dias antes); Previsão de vendas (MRP); Fotos + planilha de produção (email/WhatsApp); Capacidade máquina |
| **Processo** | Planejamento semanal → Programação → Produção → Coleta de dados → Validação → Fechamento no SAP |
| **Saídas** | Planilha de programação; OP fechada no SAP; Relatório de perda (marca própria); Faturamento (terceirizados) |
| **Clientes** | Comercial; Finanças; Expedição; Estoque; Clientes (terceirizados) |

---

## 2️⃣ Atores Identificados

### A. Letícia Ramos — Programadora PCP
- **Responsabilidades**: Montar programação semanal; acompanhar produção; receber dados; validar; fechar no SAP
- **Tempo gasto**: 1,5h planejamento + ~20min/OP fechamento (se dados corretos)
- **Ponto de dor**: "Falta de informações coerentes com a realidade"

### B. Líderes de Linha (não entrevistados diretamente)
- **Responsabilidades**: Coletar dados de produção; contabilizar quantidade produzida; contabilizar paletização; enviar dados
- **Canal**: Email com planilha + foto
- **Frequência**: No final da produção, turno imprevisível
- **Inconsistência**: "Cada um faz da sua maneira" — falta padronização

### C. Departamento de PCI (Programação e Controle de Insumos)
- **Responsabilidades**: Controlar insumos que chegam no bloco; controlar o que sobra
- **Problema**: "Não tem verificação do que chega de material no bloco" (físico vs sistema)

---

## 3️⃣ Fluxo Detalhado (Passo a Passo)

### **FASE 1: PLANEJAMENTO (Responsável: Letícia)**

**Entrada:** Demanda comercial (co-packer email + marca própria SAP MRP)  
**Tempo:** 15-20 dias antes do mês  

1. Comercial destrincha volume envasado com janela de produção
2. Letícia calcula capacidade máquina (velocidade nominal × horas disponíveis)
3. Letícia aloca ordens na programação semanal
4. Letícia envia para comercial validar com cliente
5. Se cliente não aprova → ajusta plano
6. Se cliente aprova → segue o plano

**Saída:** Planilha de programação (lotes, produtos, OP, quantidade tanques, data/hora)  
**Encaminhamento:** 
- Comercial (email ou foto WhatsApp)
- Grupo de lideranças do bloco (foto WhatsApp)

**Tempo total fase:** 1,5 horas

---

### **FASE 2: ACOMPANHAMENTO DURANTE PRODUÇÃO (Responsável: Letícia)**

**Entrada:** Programação aprovada  

1. Letícia acompanha via Sistema MES, WhatsApp (ocorrências), ligação
2. Se OP atrasa → Letícia avisa comercial
3. Se OP alterada → Letícia atualiza planilha e reenvia

**Saída:** Programação atualizada (se houver alteração)

---

### **FASE 3: COLETA DE DADOS DA LINHA (Responsável: Líderes de Linha)**

**Entrada:** Programação da semana  
**Trigger:** Quando encerra a produção (independente do horário)

1. Líder da linha tira foto do equipamento **no final da produção** (não antes)
2. Líder contabiliza quantidade produzida:
   - Verifica última folha de paletização
   - Conta primeiro palete (sobra inicial)
   - Conta último palete (sobra final)
   - Calcula: paletes completos + sobra início + sobra fim
3. Líder registra contagem em **papel** (registro de verificação)
4. Líder envia dados via **dois canais**:
   - Grupo de conferência expedição (conferem o que saiu do bloco vs o que entrou na expedição)
   - Email ao PCP com planilha (quantidade por equipamento, cálculo automático)

**Problema Crítico:** "Cada encarregado faz da sua maneira" — não há padronização

**Dados Enviados:**
- Foto do equipamento (final da produção)
- Planilha com perda por equipamento
- Quantidade paletizada

**LACUNA IDENTIFICADA:**
- ❌ Não há foto **ANTES** da produção (só no final)
- ❌ Consumo real de insumo não é verificado
- ❌ Departamento PCI não tem verificação do que chegou no bloco (físico vs sistema)
- ❌ Divergências entre contadores de equipamento não são detectadas (ex: despaletizadora 700k vs envase 900k)

---

### **FASE 4: RECEBIMENTO E VALIDAÇÃO (Responsável: Letícia)**

**Entrada:** Email com foto + planilha de produção  
**Frequência:** No final da produção, hora imprevisível

1. Letícia recebe dados via email
2. Letícia valida comparando com planejado e verificando discrepâncias
3. Se dados OK → segue para SAP (15-20 min)
4. Se dados divergem → Letícia liga para líder revisar/conferir

**Frequência de Problemas:** Das 15 OPs fechadas por semana, em média **5 precisam de revisão** (33% de taxa de erro!)

**Critérios de Validação:**
- Compara com planejado
- Verifica discrepância lógica

**Problemas Encontrados:**
- Ordem finalizada em um turno, informada em outro
- Líder passando trabalho para outro (responsabilidade difusa)
- Estoque bate sistema × físico
- Quando estoque de insumo está abaixo do que precisa usar, saldo fica errado
- Falta conferência no final da produção do que foi consumido

---

### **FASE 5: REGISTRO NO SAP (Responsável: Letícia)**

**Entrada:** Dados validados  
**Tempo:** 15-20 minutos (se dados corretos, sem revisões)

#### **Para Produtos Terceirizados (Ordem de Serviço)**
1. Insere número da OS correspondente ao produto
2. Va para número do pedido
3. Coloca quantidade produzida
4. Sistema gera insumos da ficha técnica
5. Realiza apontamento das matérias primas utilizadas
6. **Clientes Positive e Nude**: só insere o que usa na ficha (sem perda)
7. Perdas para Positive/Nude: transferência de estoque → estoque de perda
8. **Demais terceirizados**: insere todo insumo utilizado direto na OS

#### **Para Produtos Marca Própria (Ordem de Produção)**
1. Mesmo fluxo que demais terceirizados (diferente tela)
2. Após fechamento: emite relatório de perda

**Campos Obrigatórios:**
- Quantidade produzida
- Consumo de insumos
- Horas utilizadas para produzir

**Problema:** "Consigo preencher consumo de insumos, mas a confiabilidade desses números fornecidos é baixa"

---

### **FASE 6: PÓS-FECHAMENTO (Responsável: Sistema SAP)**

**Saídas:**
- Marca própria → Emite relatório de perda
- Terceirizados → Quantidade produzida vira armazenagem → gera faturamento

---

## 4️⃣ Volumetria & Tempos

| Métrica | Valor |
|---------|-------|
| **OPs por dia** | 10-15 |
| **OPs por semana** | 50-75 |
| **OPs que precisam revisão por semana** | ~5 em cada 15 (33%) |
| **Tempo planejamento (uma vez/semana)** | 1,5h |
| **Tempo fechamento por OP (dados OK)** | 15-20 min |
| **Tempo fechamento por OP (com revisão)** | +ligação + conferência |
| **Tempo de ciclo produção até fechamento** | ~12h |
| **Tempo total até status "fechado" no SAP** | 12h + 20min validação |

---

## 5️⃣ Principais Gaps & Dores 🚨

### **Críticos:**

1. **Falta de Confiabilidade de Dados (33% de taxa de erro)**
   - Divergências lógicas não detectadas antes do envio (ex: despaletizadora 700k, envase 900k)
   - Consumo de insumo é estimado, não verificado
   - Estoque físico × sistema desbalanceado

2. **Consumo de Insumo Não É Verificado**
   - Departamento de PCI não tem registro do que chega no bloco
   - Não há contagem do que sobra de insumo após produção
   - Dificulta rastreabilidade e balanço

3. **Foto Só no Final (Não Antes)**
   - Impossibilita verificar quantidade inicial com precisão
   - Impede rastrear discrepâncias durante o processo

4. **Falta de Padronização**
   - "Cada encarregado faz da sua maneira"
   - Coleta em papel (não estruturada)
   - Dois canais de envio (email + WhatsApp)
   - Sem padrão de formato/campos

5. **Responsabilidade Difusa**
   - Ordem finalizada em um turno, informada em outro
   - Líder passando trabalho para outro
   - Falta clareza de quem é responsável

6. **Ciclo de Revisão Longo**
   - 33% das OPs precisam de revisão (5 em 15)
   - Letícia precisa ligar para líder revisar
   - Bloqueia fechamento rápido

---

## 6️⃣ Necessidades Mapeadas

**Letícia relata falta de:**
- ✅ Padronização (campos, formato, processo)
- ✅ Cumprimento de obrigações (responsabilidade clara)
- ✅ Confiabilidade nos números (equipamentos, consumo)
- ✅ Verificação do estoque de insumo (entrada × saída × sobra)

---

## 7️⃣ Próximos Passos

### Para o Mapeamento:
1. ✅ **Entrevista com Letícia** (Programadora + Fechamento) — FEITO
2. ⏳ **Gemba Walk** — Observar produção real, coletar dados, tirar fotos antes/depois
3. ⏳ **Entrevista com Líder de Linha** — Validar fluxo de coleta, entender "cada um faz à sua maneira"
4. ⏳ **Entrevista com PCI** — Entender registro de insumo entrada/saída

### Para Modelagem:
- Após gemba + 3 entrevistas → documentar fluxo completo em SIPOC expandido
- Identificar pontos de decisão, desvios, ciclos de revisão
- Preparar para formalizar em BPMN (modelagem-de-processos)

---

**Status:** AS-IS 50% consolidado (1 de 3 atores entrevistados)  
**Próxima reunião:** Gemba Walk + Entrevista com Líder de Linha
