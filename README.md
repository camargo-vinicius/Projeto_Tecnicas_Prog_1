# Projeto de simulação de um jogo de dados para o módulo Técnicas de Programação 1

1. Objetivo
  Simular o lançamento de dois dados, obtendo a soma de suas faces para cada lançamento e verificando por fim se o jogo de dados é justo ou não, por meio de um teste de hipótese. Para a simulação, foram realizados 1000 lançamentos (N = 1000). 
Para construção deste projeto, foram usadas as seguintes bibliotecas:

1 - Numpy, para criação de um vetor simulando o lançamento dos dois dados e análise dos resultados; 
2 - Seaborn para o plot de um histograma, a fim de verificar o comportamento do conjunto de resultados;
3 - Math, para uso da função sqrt() (square root)

2. Metodologia
  Na primeira etapa do mini projeto, foi criado uma função chamada 'lanca_dados()' para simular o lançamento dos dois dados, que retornava para o programa principal a soma das duas faces. Então, a mesma foi executada 1000 vezes no programa principal e os resultados retornados por ela armazenados em um vetor. Usando os métodos mean (), max(), min()e std(), foram calculados a média, o lançamento com a maior e menor soma, e o desvio padrão para os resultados obtidos, respectivamente.
  A segunda etapa consistia na realização de um teste de hipótese para verificar se o jogo de dados simulado é justo ou não, supondo que todos os lançamentos tivessem a mesma chance de ocorrer. Para isto, primeiramente foi plotado o histograma, com seus valores convertidos para uma normal padrão, e chegou-se a conclusão de que o conjunto de dados seguia uma distribuição normal. Considerando que a população da simulação são os 1000 lançamentos, que a média dos lançamentos é conhecida e sempre fica próxima de 7, (obtida na etapa 1 e considerada o parâmetro de interesse do problema) e que a população é normal, podemos realizar um teste bilateral com grau de confiança 95% (ou seja, z = 1,96) para uma determinada amostra. Logo, se o valor obtido para o z simulado não pertence ao intervalo -1,96 <= z <= 1,96, rejeitamos a hipótese nula. Caso contrário, não rejeitamos a hipótese nula e portanto podemos dizer que o jogo é justo ao nível de significancia de 5%. Para o tamanho da amostra, foi usada a seguinte fórmula

![image](https://github.com/camargo-vinicius/Projeto_Tecnicas_Prog_1/assets/89496385/6897ed2a-1cfa-46f8-a17b-a523e0176d6a)


4. Resultados
