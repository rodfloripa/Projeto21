# Projeto21
Precificação Dinamica com Multi-Armed Bandits

Implementando o artigo "Improving multi-armed bandits for pricing":
https://trovo.faculty.polimi.it/01papers/trovo2018improving_b.pdf

Para ver o desempenho de clássicos algoritmos Bandits em ambiente
estacionário e não estacionário veja o link:
https://github.com/dquail/NonStationaryBandit

Considerando um ambiente não estacionário,temos o resultado para 3 modificações
da curva de demanda no tempo e calibração no exato momento.
É possível aumentar o número de modificações. O algoritmo poderia detectar a queda na recompensa e
fazer a calibração automática dos braços, mas para simplificar isto não foi feito.


![Recompensa no tempo](https://github.com/rodfloripa/Projeto21/blob/main/reward.png?raw=true)
