# 📋 Roteiro de Entrevista — Fechamento de Ordem de Produção (AS-IS)

**Projeto:** Mapeamento AS-IS do processo de fechamento de OP  
**Data:** 22/09/2026  
**Entrevistador:** André Carrasco  
**Entrevistado:** Letícia Ramos | **Cargo/Papel:** Programadora PCP

---

## 🎯 Instruções Gerais
- Entrevista é **observacional**: procure entender o que realmente acontece, não o que deveria acontecer.
- Peça **exemplos concretos** — "me mostra uma OP que você fechou semana passada".
- Capture **tempos, frequências e exceções** — "quanto tempo leva?", "isso sempre acontece assim?".
- Anote **dores/gaps** que o entrevistado menciona espontaneamente.
- **Deixe falar**: se a resposta saí do script, anote — pode ser importante.

---

# ROTEIRO 1: PROGRAMADOR DE PRODUÇÃO

## A. Planejamento & Emissão da Planilha

**A1.** Quando você recebe a demanda comercial (co-packer, marca própria)? Por qual canal?  
_Resposta:_  co-packer é recebida por email e marca propria, retirada da previsão de vendas do modulo MRP do sistema SAP
_Notas:_

**A2.** Qual é o processo exato que você faz para montar a programação semanal de OPs? (Descreva passo a passo)  
_Resposta:_  vamos supor que vamos realizar a programação hoje. 
recebo a demanda sempre 15 a 20 dias antes do próximo mês, ja com a capacidade de produção do mês, seguindo do dia 20 a 20, onde o departamento comercial destrincha o volume envasado, ja com a janela de produção estabelecidas. com a demanda em mãos, é realizada com base na velocidade nominal da maquina, com base na horas disponiveis do período. com isso temos a quantidade geral de caixas que conseguimos entregar nessa janela de produção. com essa informação em mãos, o departamento comercial entra em contato com cliente, informando a disponbilidade e capacidade de produção naquela janela. cliente retorna com o que ele tem necessidade que seja produzido, em cima do volume que conseguimos entregar naquela janela. cliente informando o comercial e o comercial informando a devolutiva do cliente ao PCP, é realizado a alocação dessas ordens na programação. após realizar a alocação das ordens, é realizada outra devolutiva para o comercial, entrar em contato com o cliente e validar a programação proposta. validado com cliente, segue o plano. nao validado, ajusta o plano de produção, conforme necessidade do cliente.
_Notas:_

**A3.** Quais informações você coloca na planilha de OPs? (Listar cada campo/coluna)  
_Resposta:_  lote, produto, ordem de produção, quantidades de tanques que serão formulados, data e horario. hoje essas planilhas são preenchidas em dois locais. uma planilha de programação para linha de latas. e outra planilha com a programação da linhas tetrapak. as duas são diferente em layout, mas conteudo igual.
_Notas:_

**A4.** Quanto tempo leva para montar essa planilha? (De quando chega a demanda até estar pronta)  
_Resposta:_  1,5 h. é realizada a montagem, revisada e enviada para o departamento comercial para validar com cliente.
_Notas:_

**A5.** Para quem você encaminha essa planilha? (Nominalmente, qual departamento, como — email, sistema, impressa?)  
_Resposta:_  comercial - email ou foto no whatsapp quando solicitam. grupo da liderança do bloco - foto no whatsapp. 
_Notas:_

## B. Acompanhamento Durante a Produção

**B1.** Depois que a planilha é emitida, você acompanha a produção de alguma forma? (Telefone, sistema, visita na linha?)  
_Resposta:_  realiza ligações para saber o andamento da produção. sistema mes da empresa. walk in gemba
_Notas:_

**B2.** Se uma OP não sai conforme planejado (atraso, problema), como você fica sabendo?  
_Resposta:_  sistema mes, grupo de whatsapp das ocorrências e ligação para o bloco
_Notas:_

**B3.** Quando uma OP é alterada (quantidade, data), você atualiza a planilha? Como?  
_Resposta:_  quando gera atraso da produção, a data da ordem é postergada. atualizo na planilha e encaminho novamente para os meios de comunicação
_Notas:_

## C. Recebimento de Dados da Linha

**C1.** Como você recebe as informações de que a OP foi produzida? (Quem envia, por qual canal, que informações trazem?)  
_Resposta:_  informações chegam via email. com foto das maquinas. envasadora, inspetor eletronico e quantidade que saiu paletizada
_Notas:_

**C2.** Você valida esses dados antes de repassar para o PCP? Se sim, como? Qual é o critério?  
_Resposta:_  não repasso, pois a pessoa que faz o planejamento, é a mesma que faz o apontamento das informações
_Notas:_

**C3.** Qual é a frequência: você recebe os dados ao vivo ou no final do turno/dia?  
_Resposta:_  quando encerra a produção. independente do horário que cair
_Notas:_

**C4.** Já aconteceu de a linha te enviar dados que não fizessem sentido? (Exemplo: quantidade maior que planejado, foto confusa). Como você agiu?  
_Resposta:_  sim. questionei e liguei para a pessoa realizar a conferência novamente, antes de finalizar o apontamento.
_Notas:_

## D. Dores & Gaps

**D1.** Qual é a maior dificuldade que você enfrenta no fechamento das OPs?  
_Resposta:_  falta de informações coerentes com a realidade. a ordem ser finalizada em um turno, e for informada/ fechada em outro turno. um líder passando para o outro realizar o trabalho que o primeiro deveria ter realizado. estoque estar batendo, sistema contra físico. pois quando estoque sistemico esta com quantidade abaixo do que necessito utilizar na ordem, fico com saldo errado, nao conseguindo finalizar a ordem. não conferencia no final da produção dos insumos que foram contabilizados, gerando uma incerteza do que realmente tem.
_Notas:_

**D2.** O que falta hoje que facilitaria seu trabalho?  
_Resposta:_  padronização e cumprimento das obrigações de todos
_Notas:_

---

# ROTEIRO 2: LÍDER DE LINHA DE PRODUÇÃO

## A. Coleta de Dados — Antes da Produção

**A1.** Quando você recebe a planilha de OPs do programador, o que você faz com ela?  
_Resposta:_  informação da programação é repassada ao operador da sala de envase quando finaliza a produção atual
_Notas:_

**A2.** Você tira foto do equipamento **antes** de iniciar o envase? Por quê? Quando exatamente (setup concluído? linha rodando?)?  
_Resposta:_  foto é tirada somente na finalização da produção
_Notas:_

**A3.** Quem tira essa foto? (Você, operador, inspetor?)  
_Resposta:_  sim, eu
_Notas:_

## B. Coleta de Dados — Durante/Após Produção

**B1.** Descreva o processo exato de **contagem de quantidade produzida**. (De cabeça? Planilha? Sistema? Balança?)  
_Resposta:_  verifico a ultima folha de paletização, vejo o que tenho de sobra do inicio que é o primeiro palete, e o que sobrou do último palete
_Notas:_

**B2.** Quem faz essa contagem? (Operador, inspetor, você?)  
_Resposta:_  eu
_Notas:_

**B3.** Como você calcula: "O que foi produzido"? (Exemplo: foto inicial − foto final = produzido? Ou outro método?)  
_Resposta:_  vejo o que foi palete completo na produção, mais quantidade que foi no primeiro palete e o que tem no palete final
_Notas:_

**B4.** E o que é **paletizado** — como você registra isso? (Planilha? Sistema? Manual?)  
_Resposta:_  registro de verificação em papel
_Notas:_

**B5.** **Pergunta crítica:** Do insumo que era planejado, quanto realmente sobra após a produção? Você tem registro disso?  
_Resposta:_  quem tem esses valores é o departamento de PCI, programação e controle de insumos. hoje não tem a verificação do que chega de material no bloco. tanto físico como sistema.
_Notas:_

## C. Envio de Dados

**C1.** Quando você envia os dados para o PCP (foto + quantidades)? (Turno inteiro? No final? Próximo dia?)  
_Resposta:_  no final da produção
_Notas:_

**C2.** Por qual canal você envia? (Email com anexo? WhatsApp com foto? Sistema? Papel?)  
_Resposta:_  dois canais. primeiro, o grupo de conferência da expedição, confere o que saiu do bloco de produção contra o que entrou na expedição. em email ao pcp, ![alt text](<Captura de tela 2026-09-22 174351.png>)
encaminho essa planilha com a quantidade contada em cada equipamento, calculo automatico. fluxo não é igual para todos os encarregados. cada um faz da sua maneira.
_Notas:_

**C3.** Que informações exatamente você envia? (Foto + um número? Foto + planilha? Descrição?)  
_Resposta:_  perda por equipamento da linha de envase
_Notas:_

**C4.** Já houve situação em que o PCP te pediu para revisar/corrigir esses dados? Quantas vezes? Por quê?  
_Resposta:_  comigo, não
pode ser que com outros encarregados, sim
_Notas:_

## D. Desvios & Exceções

**D1.** Existe alguma OP que **não segue** esse processo padrão? (Diferente quantidade, sem foto, etc)  
_Resposta:_  não
_Notas:_

**D2.** O que faz você ter que revisar/corrigir dados já enviados?  
_Resposta:_  no meu caso, quando vou fazer o fechamento, os valores dos contadores dos inspetores, estão muito divergentes. exemplo: despaletizadora contou 700.000 latas e envase que é a maquina posterior, contou 900.000 latas.
_Notas:_

**D3.** Qual é a maior dificuldade que você enfrenta ao fornecer esses dados?  
_Resposta:_  no meu caso, quando tem essas divergências. realizo a contagem do que entrou de latas no despaletizador e o que saiu de latas no paletizador
_Notas:_

**D4.** O que falta hoje que facilitaria sua parte do processo?  
_Resposta:_  confiabilidade nos numeros fornecidos pelos equipamentos
_Notas:_

---

# ROTEIRO 3: OPERACIONAL DO PCP (Quem Fecha a OP no SAP)

## A. Recebimento de Dados

**A1.** Como e quando você recebe os dados de produção da linha? (Qual canal, qual frequência?)  
_Resposta:_ ja respondido anteriormente 
_Notas:_

**A2.** De quem você recebe? (Sempre a mesma pessoa ou pode ser qualquer um da linha?)  
_Resposta:_  dependo do turno que finalizou a produção.
_Notas:_

**A3.** Que informações chegam para você? (Descreva exatamente o conteúdo de um email/foto/mensagem típica)  
_Resposta:_  ja respondido anteriormente
_Notas:_

## B. Validação & Análise

**B1.** Quando você recebe os dados, o que você faz **primeiro**? (Lê, valida, já coloca no SAP?)  
_Resposta:_  sigo esse fluxo
_Notas:_

**B2.** Qual é o seu critério para dizer "esses dados estão OK"? (Compara com o planejado? Verifica lógica?)  
_Resposta:_  comparo com planejado e verifico discrepância dos dados
_Notas:_

**B3.** Com que frequência você encontra uma divergência/erro nos dados? (Sempre? Às vezes? Raramente?)  
_Resposta:_  das 15 fechadas na semana, em média, 5
_Notas:_

**B4.** Quando encontra divergência, qual é seu processo? (Você corrige? Pede revisão? Quem?)  
_Resposta:_  peço revisão para o responsavel
_Notas:_

**B5.** Qual é o **tempo total** que você leva para validar e registrar uma OP no SAP, do recebimento dos dados até o status "fechado"?  
_Resposta:_  se os dados estiverem corretos, não necessitando de verificação novamente, 15/20 minutos para realizar o fechamento
_Notas:_

## C. Registro no SAP

**C1.** Descreva o processo exato de fechar uma OP no SAP. (Qual tela, quais campos, em qual ordem?)  
_Resposta:_  ordem de serviço (produtos terceirizados) -> insiro a o.s. correspondente ao produto, vou no numero do pedido e coloco a quantidade produzida, gerando os insumos da ficha tecnica. realizo o apontamento das matérias primas utilizadas. o apontamento para clientes (positive e nude), é realizado somente o que utiliza na ficha tecnica, nao gerando perda. as perdas paras esses clientes, é realizada uma transferencia de estoque no sistema, para o estoque de perda. demais cliente terceirizados, todo o insumo utilizado é inserido direto na ordem de serviço.
e para produtos de marca própria. é realizado o mesmo fluxo para os demais clientes que não sao (positive e nude), porem, nao é na mesma tela, é em ordem de produção.
_Notas:_

**C2.** Quais informações **obrigatoriamente** você precisa preencher? (Quantidade produzida? Consumo de insumo? Defeito? Outra?)  
_Resposta:_  quantidade produzida, consumo de insumos e horas utilizadas para produzir aquele lote.
_Notas:_

**C3.** Que informação você não consegue preencher hoje por falta de dado? (Consumo de insumo? Devolução? Outra?)  
_Resposta:_  consigo preencher o consumo de insumos, mas a confiabilidade desses numeros fornecidos, é baixa.
_Notas:_

**C4.** Depois de fechar a OP no SAP, qual é o próximo passo? (Relatório? Passagem para finanças? Nada? Aviso para alguém?)  
_Resposta:_  produtos marca propria, apos finalizar o fechamento é emitido um relatório de perda.
para produtos terceirizados, a quantidade produzida que foi apontada anteriormente, vira armazenagem, onde é gerada o faturamento dos produtos.
_Notas:_

## D. Problemas & Gargalos

**D1.** Qual é a **maior dificuldade** que você enfrenta no fechamento de OPs?  
_Resposta:_  ja respondido anteriormente
_Notas:_

**D2.** Quantas OPs por dia você precisa revisar/corrigir por causa de dados errados?  
_Resposta:_  ja respondido anteriormente
_Notas:_

**D3.** Qual informação hoje está **faltando** ou é difícil de obter? (Consumo real de insumo? Refugo? Devolução?)  
_Resposta:_ ja respondido anteriormente
_Notas:_

**D4.** Se você pudesse mudar **uma coisa** neste processo, qual seria?  
_Resposta:_  ja respondido anteriormente
_Notas:_

---

## 📝 Observações Gerais (Ao Final)

**Temas que saíram do roteiro mas parecem importantes:**  
_Respostas:_  
_Notas:_

**Próximos passos sugeridos pelo entrevistado:**  
_Respostas:_  
_Notas:_

---

**Assinado:** André Carrasco | **Data:** 22/09/2026 | **Duração entrevista:** 60 min
