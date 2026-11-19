# 04 · LLM: o que é e como funciona

Resumo explicando LLM para um colega de outra área, mais três limitações do modelo.

## O que é um LLM

Um LLM (como ChatGPT ou Claude) é uma IA treinada com bilhões de textos da internet, livros e códigos. No treino, ele aprende tentando adivinhar a próxima palavra de uma frase; a cada erro, ele ajusta seus parâmetros até dominar os padrões da nossa linguagem.

Quando você faz uma pergunta, ele não "pensa" como um humano: ele calcula e monta a resposta palavra por palavra, escolhendo sempre a continuação mais provável. É como o corretor automático do celular, só que incrivelmente avançado por ter lido quase tudo na internet. Depois, ele ainda passa por um ajuste fino com avaliações humanas para aprender a ser útil, seguro e seguir instruções.

## Limitações do modelo

1. **Alucinação:** como ele busca o texto mais provável e não necessariamente o verdadeiro, pode inventar dados, datas e regras com total convicção.
2. **Conhecimento congelado (data de corte):** ele só sabe o que estava nos dados até o fim do seu treino. Fatos recentes ou dados internos da empresa exigem integração externa (como RAG).
3. **Viés dos dados:** ele aprende com textos humanos, então pode reproduzir preconceitos, estereótipos ou visões parciais presentes na internet.
