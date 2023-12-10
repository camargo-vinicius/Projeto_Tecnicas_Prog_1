# Projeto de simulação de um jogo de dados para o módulo Técnicas de Programação 1
O jogo consiste em lançar dois dados e verificar a soma de suas faces, repetindo o processo 1000 vezes e verificando por fim se o jogo de dados é justo ou não, por meio de um teste de hipótese.
Para construção deste projeto, foram usadas as bibliotecas numpy, seaborn, e math.
Para verificação se o jogo é justo ou não, foi plotado o gráfico da distribuição do conjunto de dados resultante dos 1000 lançamentos e observou-se que os eventos podem ser representados por uma curva gaussiana. Então, um teste t-student foi realizado, com grau de confiança de 95% (z = 1,96).
Para este valor de z, a amostra deveria conter 278 resultados e por meio do valor t para esta amostra, chegou-se a conclusão de que em 95% dos casos, a simulação feita representa um jogo de dados justo.
