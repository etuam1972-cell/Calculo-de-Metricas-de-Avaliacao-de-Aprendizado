README — Cálculo de Métricas de Avaliação de Aprendizado
Projeto de implementação das principais métricas de avaliação de modelos de classificação de dados, a partir de uma matriz de confusão.

Sobre o projeto
Este exercício tem como objetivo implementar, na prática, as métricas fundamentais de avaliação de classificadores. Mais do que decorar fórmulas, a proposta é entender o que cada métrica está medindo e quando cada uma é a mais adequada — porque acurácia sozinha engana, especialmente em bases desbalanceadas.

Objetivo
Calcular, a partir de valores de VP, VN, FP e FN:

Acurácia — proporção global de acertos
Sensibilidade (recall) — capacidade de identificar os positivos reais
Especificidade — capacidade de identificar os negativos reais
Precisão — confiabilidade das predições positivas
F-score — equilíbrio entre precisão e sensibilidade
Matriz de confusão
A matriz é escolhida livremente, já que o foco é compreender o mecanismo das métricas. A adotada neste projeto:

Predito Positivo	Predito Negativo
Real Positivo	VP = 50	FN = 10
Real Negativo	FP = 5	VN = 100
Total de elementos N = 165 (60 positivos reais, 105 negativos reais).

Fórmulas
Métrica	Fórmula
Acurácia	(VP + VN) / N
Sensibilidade	VP / (VP + FN)
Especificidade	VN / (VN + FP)
Precisão	VP / (VP + FP)
F-score	2 × (P × S) / (P + S)
Estrutura do código
Uma única função metricas(vp, vn, fp, fn) recebe os quatro valores da matriz e devolve um dicionário com as cinco métricas arredondadas em quatro casas decimais.

Como adaptar
Basta alterar os valores de VP, VN, FP e FN na chamada da função. Todos os cálculos derivam da mesma matriz, e as fórmulas permanecem válidas para qualquer combinação.

Aprendizados
Acurácia é uma métrica de contexto, não de decisão — ela não distingue tipos de erro.
Sensibilidade e precisão medem coisas diferentes e frequentemente entram em conflito.
O F-score só faz sentido lido junto com as métricas que o compõem; um F1 alto pode esconder recall baixo compensado por precisão alta.
A matriz de confusão é a fonte de verdade: todas as métricas são apenas recortes diferentes dela.
Se quiser, posso também ajustar o README para um formato entregável de curso (com nome do aluno, disciplina e data) ou converter o conteúdo para um arquivo .md pronto para commit — mas isso depende de onde você vai publicar.




