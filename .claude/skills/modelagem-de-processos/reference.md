# Especialista em Modelagem de Processos — Referência

## Conceitos-chave
- AS-IS vs. TO-BE — convenções visuais para não confundir os dois
- Granularidade/nível de detalhe (visão executiva → operacional)
- Pools e lanes — organização/sistema externo vs. papel/área interna

## Convenções de modelagem
- Um pool por organização ou sistema externo; lanes dentro de um pool por papel/área
- Fluxo de sequência dentro do mesmo pool; fluxo de mensagem (tracejado) entre pools
- Nomeação de tarefas no formato Verbo + Objeto (ex.: "Aprovar Pedido")
- Eventos de início/fim explícitos sempre presentes

## Ferramentas / Stack
- Notação: BPMN 2.0
- Geração e edição do diagrama: skill `drawio-skill` (artefato `.drawio` nativo, exportável para PNG/SVG/PDF)
- Repositórios de modelo: ARIS, Bizagi, Camunda Modeler

## Checklist detalhado
- [ ] Escopo do modelo definido (AS-IS ou TO-BE, não ambos no mesmo diagrama)
- [ ] Pools/lanes correspondem aos papéis/sistemas reais
- [ ] Notação BPMN aplicada corretamente (eventos, gateways, fluxos)
- [ ] Nível de detalhe adequado ao público
- [ ] Modelo validado com participantes do processo

## Armadilhas comuns
- Over-detailing — poluir o diagrama principal com exceções raras
- Uso incorreto de notação (gateway errado, fluxo de mensagem tratado como sequência)
- Modelar sem validação dos participantes
- Misturar convenções de AS-IS e TO-BE no mesmo artefato

## Leituras complementares
- Especificação BPMN 2.0 (OMG)
- Fundamentals of Business Process Management (Dumas et al.), capítulo de modelagem
