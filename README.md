# wine-quality
Modelagem de regressão com o objetivo de prever a qualidade do vinho baseando-se em características fisíco-quimicas e sensoriais.

# Discussão da Resolução
Como descrito em https://github.com/jessica-santos/wine-quality/blob/master/wine-quality.ipynb, por serem valores discretos, e não contínuos, uma possível abordagem seria criar um modelo multiclasse. Porém, por não ter exemplos de todas as classes (0 a 10), esse modelo seria falho. Neste caso a melhor alternativa é fazer uma regressão.

Foram testados dois modelos muito utilizados para regressão, uma regressão linear clássica e uma Random Forest Regressor (RFR), que por ser um ensemble costuma apresentar ótimos resultados, além de não necessitar de muitos testes de parâmetros.

Foram utilizadas 6 métricas para avaliar o erro dos modelos, três comumente utilizadas na análise de modelos de regressão: Mean squared error, Mean absolute error e variance score e três mais básicas que auxiliam a avaliar o erro de acordo com o problema: erro máximo, erro mediano e porcentagem de erros menores que 1. Utilizando todas essas métricas é possível garantir uma avaliação abrangente do modelo.

Em todas as 6 métricas o modelo RFR se sobressai sobre o modelo de Regressão Linear. No modelo RFR obtemos um erro mediano de 0.29, ou seja, em metade das predições o erro não passa de 0.29. Além disso, em aprox. 91% das predições o erro é menor do que 1. É difícil dizer com certeza se o modelo desta forma seria suficiente sem entender a aplicação, porém o erro está balanceando - em apenas 4,6% dos dados há um alto erro (maior do que 1) para cima e em 4,4% um alto erro para baixo - e obtém uma precisão suficiente para maioria dos casos.
