# 05 · Tokens, janela de contexto e temperatura

Definição de token, janela de contexto e temperatura em uma frase cada, mais um exemplo do que acontece quando a conversa ultrapassa a janela.

## Definições

| Conceito | Definição |
|----------|-----------|
| **Token** | É o pedacinho de texto que o modelo realmente lê e gera, que pode ser uma palavra inteira, parte de uma palavra ou até um sinal de pontuação, e é por ele que se mede o tamanho (e o custo) de cada pergunta e resposta. |
| **Janela de contexto** | É o limite de tokens que o modelo consegue considerar de uma vez numa chamada, somando instruções, histórico da conversa, documentos e a própria resposta, funcionando como a "memória de trabalho" dele, já que entre uma chamada e outra ele não guarda nada. |
| **Temperatura** | É o ajuste que controla o quanto o modelo arrisca na hora de escolher o próximo token: baixa deixa as respostas mais previsíveis e consistentes, alta deixa mais variadas e criativas (e com mais chance de erro). |

## Quando a conversa passa da janela

Imagine um chatbot de atendimento em que o cliente informa o número do pedido logo no começo e depois passa um bom tempo conversando sobre outros assuntos. Como o modelo não tem memória, o sistema reenvia toda a conversa a cada mensagem. Quando o histórico passa do tamanho da janela, as mensagens mais antigas precisam ser cortadas, ou a chamada simplesmente dá erro. Aí o cliente pergunta "e o meu pedido, como está?" e o bot não sabe mais de que pedido se trata, porque essa informação saiu da janela.

Por isso, em produção, é preciso guardar os dados importantes fora do modelo (por exemplo, num banco) e reenviá-los sempre que forem necessários.
