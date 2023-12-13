# Projeto de simulação de um jogo de dados para o módulo Técnicas de Programação 1

1. Objetivo
  Simular o lançamento de dois dados, obtendo a soma de suas faces para cada lançamento e verificando por fim se o jogo de dados é justo ou não, por meio de um teste de hipótese. Para a simulação, foram realizados 1000 lançamentos (N = 1000). 
Para construção deste projeto, foram usadas as seguintes bibliotecas:

      1 - Numpy, para criação de um vetor simulando o lançamento dos dois dados e análise dos resultados; 
      
      2 - Seaborn para o plot de um histograma, a fim de verificar o comportamento do conjunto de resultados;
      
      3 - Math, para uso da função sqrt() (square root)

2. Metodologia
  Na primeira etapa do mini projeto, foi criado uma função chamada 'lanca_dados()' para simular o lançamento dos dois dados, que retornava para o programa principal a soma das duas faces. Então, a mesma foi executada 1000 vezes no programa principal e os resultados retornados por ela armazenados em um vetor. Usando os métodos mean (), max(), min()e std(), foram calculados a média, o lançamento com a maior e menor soma, e o desvio padrão para os resultados obtidos, respectivamente.
  A segunda etapa consistia na realização de um teste de hipótese para verificar se o jogo de dados simulado é justo ou não, supondo que todos os lançamentos tivessem a mesma chance de ocorrer. Para isto, primeiramente foi plotado o histograma, com seus valores convertidos para uma normal padrão, e chegou-se a conclusão de que o conjunto de dados seguia uma distribuição normal. Considerando que a população da simulação são os 1000 lançamentos, com uma distribuição normal (plotada no projeto) e desvio padrão conhecido (calculado na etapa 1), podemos realizar um teste bilateral com grau de confiança 95% para uma determinada amostra. Usando como parametro a média dos resultados obtidos para a soma das faces, podemos formular as hipóteses nula e alternativa como:

      H0 - média u = 7
      H_alternativa != 7

    Para a amostra, podemos usar a seguinte fórmula:

![image](https://github.com/camargo-vinicius/Projeto_Tecnicas_Prog_1/assets/89496385/6a32a1f6-6278-4f5e-a1d8-3867a2b0d919)

 onde, temos que:

    N: quantidade de lançamentos feitos
    
    z: definido a partir do grau de confiança desejado (para 95%, z = 1.96)
    
    p = proporção (podemos adotar p = 50% se eu não tenho nenhuma informação sobre o valor que eu espero encontrar)
    
    e = margem de erro (5% para grau de confiança 95%)

  Para estes parametros, o tamanho da amostra é 278. A partir dessa amostra, calcula-se a média amostral e o desvio padrão amostral para determinar o valor de estatística, com base na seguinte fórmula:

  ![image](https://github.com/camargo-vinicius/Projeto_Tecnicas_Prog_1/assets/89496385/7d75fa63-6eb4-4e22-802d-b609cf860070)

  Fonte: https://www2.ufjf.br/clecio_ferreira//files/2012/04/Cap5-Testes-de-hipoteses-Parte-13.pdf

onde:

  X = media amostral
  u_0= media população
   = desvio padrão amostral
  n = tamanho da amostra

Com o valor da estatística de teste, é verificado se este valor está compreendido entre 1.96 <= z <= 1.96 para rejeitar ou não a hipótese nula.

3. Resultados e conclusão

Todos os valores simulados da estátistica de teste ficaram dentro do intervalo de confiança de 95%. Logo, não podemos rejeitar a hipótese nula à um nível de significância de 5% e portanto a média da soma das faces fica próximo de 7.
Conclui-se que o jogo não é justo, pois os lançamentos dos dois dados não geram resultados igualmente prováveis. Para o jogador de dados, isto significa que quanto mais próximo a soma das faces estiver de 7, maior as probabilidades 
delas ocorrerem.







5. Resultados
