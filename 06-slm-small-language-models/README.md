# 06 · SLM (Small Language Models)

Resumo definindo SLM, quadro comparativo SLM x LLM e dois exemplos de tarefas da plataforma: uma em que um SLM bastaria e outra que exigiria um LLM.

## O que é um SLM

Um SLM (Small Language Model) é um modelo de linguagem construído com a mesma base dos LLMs, mas bem menor: em geral, entre 1 e 13 bilhões de parâmetros, contra centenas de bilhões dos modelos grandes. Ele não sabe fazer tudo o que um LLM faz, e essa é justamente a ideia. Treinado ou ajustado para um domínio específico, como atendimento, triagem de chamados ou análise de documentos, ele faz aquele conjunto de tarefas com boa precisão, menor custo e resposta mais rápida.

Por ser leve, pode rodar localmente, em dispositivos de borda ou em nuvem privada, sem mandar dados para servidores de terceiros. Por isso as empresas usam SLMs em tarefas de alto volume e baixa latência, deixando os LLMs para o que exige raciocínio complexo, contexto longo ou criatividade.

## SLM x LLM

| Critério | SLM | LLM |
|----------|-----|-----|
| **Parâmetros** | Geralmente de 1 a 13 bilhões | De centenas de bilhões a trilhões |
| **Latência** | Baixa, podendo chegar a milissegundos quando roda localmente | Maior, já que normalmente depende de chamadas a servidores na nuvem |
| **Custo de inferência** | Baixo, cerca de uma ordem de grandeza menor em alto volume | Alto, e cresce rápido com o volume de requisições |
| **Amplitude de tarefas** | Restrita: muito bom em tarefas delimitadas de um domínio | Ampla: generalista, lida com assuntos e tarefas variados |
| **Privacidade** | Pode rodar on-premise, na borda ou em nuvem privada, sem dados saírem da empresa | Normalmente consumido via API de terceiros, o que exige cuidado com dados sensíveis |
| **Fine-tuning** | Mais barato e rápido de ajustar para um domínio específico | Caro e complexo; na prática, costuma ser usado como vem |

## Na nossa plataforma

**Onde um SLM bastaria:** classificar a intenção da mensagem do cliente no início do atendimento (por exemplo, segunda via, status de pedido ou reclamação) para direcionar ao fluxo certo. É uma tarefa fechada, repetitiva, de altíssimo volume e que precisa ser rápida.

**Onde seria necessário um LLM:** responder dúvidas abertas do cliente consultando documentos variados (RAG), ou avaliar a qualidade de uma conversa inteira, entendendo contexto, tom e se o problema foi realmente resolvido. Essas tarefas exigem raciocínio, contexto longo e flexibilidade para lidar com entradas imprevisíveis.
