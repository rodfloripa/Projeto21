# Projeto21
Precificação Dinamica com Multi-Armed Bandits

Implementando o artigo ["Improving multi-armed bandits for pricing"](
https://trovo.faculty.polimi.it/01papers/trovo2018improving_b.pdf)

[Desempenho de clássicos algoritmos Bandits em ambiente
estacionário e não estacionário](
https://github.com/dquail/NonStationaryBandit)

<div align="justify">
Este artigo apresenta uma evoluçao do UCB classico, com UCB1-M e UCB-LM explorando a monotonicidade dos braços.
Cada braço representa o lucro obtido com um determinado preço de produto.
Dado um braço ai, as realizações de todos os resultados Xj com j < i fornecem informações que podem ser exploradas para o cálculo do UCB no
valor esperado µi.
De fato, como µi ≤ µj, podemos usar as realizações obtidas até o momento de Xj como amostras otimistas para estimar µi.
Consideramos Xi,t a média empírica,na rodada t, dos resultados obtidos puxando o braço ai por Ti(t − 1) rodadas e
xi,t sua realização.

                                                              
</div>

  ![Formula](https://github.com/rodfloripa/Projeto21/blob/main/formula.jpg?raw=true)

Fig1. UCB1-M
<br>
<br>
<br>
 ![Formula](https://github.com/rodfloripa/Projeto21/blob/main/formula2.jpg?raw=true)

Fig2. UCB-LM
<br>
<br>
O Conhecimento "Monotônico"
<div align="justify">
Neste problema específico, sabemos com certeza que as recompensas estão ordenadas da seguinte forma:
μ1 ≥ μ2 ≥ ... ≥ μK

Por causa disso, qualquer informação que tenhamos sobre o Braço 1 ou o Braço 2 nos diz algo sobre o valor máximo possível do Braço 3. Se nossos dados sugerem que o Braço 1 tem uma recompensa máxima plausível de 0,8, então o Braço 3 não pode ter uma recompensa maior que 0,8, mesmo que seus próprios dados limitados sugiram que possa ser 0,9.

Imagine o Braço 1 (o melhor) e o Braço 10 (o pior):

Sem o min (UCB padrão): Você não utilizou muito o Braço 10. Sua incerteza é enorme. Seu teto(upper bound) é 1,0(alto). Você desperdiça muitas rodadas utilizando o Braço 10 para "ver se ele é bom".
Com o min (UCB1-M): O algoritmo vê que o teto do Braço 1 é 0,6. Mesmo que o Braço 10 não tenha dados, o min diz: "Como o Braço 10 é monotonicamente pior que o Braço 1, seu teto(upper bound) deve ser ≤0,6". Resultado: O "teto alto" do Braço 10 é reduzido instantaneamente. O algoritmo percebe que o Braço 10 é um perdedor muito mais rápido do que perceberia de outra forma. 
Podemos calcular o arrependimento como a diferença de recompensa com o melhor braço em todo o período e a recompensa obtida pelo algoritmo.
</div>




Recompensas Médias dos Braços Modelados com a Distribuiçao Beta:

Braço1: 0.3

Braço2: 0.4

Braço3: 0.5

Braço4: 0.6

Braço5: 0.7


![Recompensa no tempo](https://github.com/rodfloripa/Projeto21/blob/main/lamento.png?raw=true)

Fig3. UCB-LM é o melhor modelo,com o menor arrependimento
