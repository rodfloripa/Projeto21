# Projeto21
Precificação Dinamica com Multi-Armed Bandits

Implementando o artigo "Improving multi-armed bandits for pricing":
https://trovo.faculty.polimi.it/01papers/trovo2018improving_b.pdf

Para ver o desempenho de clássicos algoritmos Bandits em ambiente
estacionário e não estacionário veja o link:
https://github.com/dquail/NonStationaryBandit

<div align="justify">
Cada braço representa o lucro obtido com um determinado preço de produto.
Dado um braço ai, as realizações de todos os resultados Xj com j < i fornecem informações que podem ser exploradas para o cálculo do UCB no
valor esperado µi.
De fato, como µi ≤ µj, podemos usar as realizações obtidas até o momento de Xj como amostras otimistas para estimar µi.
Consideramos Xi,t a média empírica,na rodada t, dos resultados obtidos puxando o braço ai por Ti(t − 1) rodadas e
xi,t sua realização
</div>

![Formula](https://github.com/rodfloripa/Projeto21/blob/main/formula.jpg?raw=true)


Recompensas Médias dos Braços Modelados com a Distribuiçao Beta:

Braço1: 0.3

Braço2: 0.4

Braço3: 0.5

Braço4: 0.6

Braço5: 0.7


![Recompensa no tempo](https://github.com/rodfloripa/Projeto21/blob/main/reward.png?raw=true)
