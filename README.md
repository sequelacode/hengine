# Hengine

Engine de xadrez baseada em lances humanos.

## Introdução

A **Hengine** é uma engine de xadrez fundamentada em lances historicamente jogados por humanos.  
Seu funcionamento baseia-se na análise de um grande banco de dados de partidas de xadrez acumuladas ao longo da história do jogo.

A partir do **estado atual do tabuleiro**, a Hengine utiliza um algoritmo próprio para **sugerir o lance mais recorrente e eficiente** naquela posição, considerando apenas partidas reais já disputadas.

Diferentemente de engines tradicionais focadas exclusivamente em cálculo profundo e avaliação heurística, a Hengine prioriza padrões humanos de jogo, buscando reproduzir decisões tomadas por jogadores experientes em contextos semelhantes.

## Critérios de Seleção de Lances

Os lances sugeridos pela Hengine passam por uma análise estatística baseada nos seguintes critérios:

1. **Resultado da partida**  
   O lance deve ter sido realizado em partidas que resultaram em vitória.

2. **Rating do jogador**  
   É considerado o rating (ELO) do jogador que executou o lance, atribuindo maior peso a jogadores mais bem ranqueados.

3. **Taxa de sucesso do lance**  
   Avalia-se a média de partidas em que o lance foi utilizado e resultou em vitória.

Esses fatores combinados permitem que a engine priorize lances não apenas populares, mas também **estatisticamente eficazes**.

## Geração de Lances

A geração de lances na Hengine segue um fluxo bem definido, desde a leitura do estado atual do tabuleiro até a recomendação final.

### Arquitetura Básica

A imagem abaixo ilustra a arquitetura geral do processo de geração de lances:

![Arquitetura de geração de lances](Hengine%20-%20Arquitetura.jpg)
