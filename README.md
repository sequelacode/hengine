# Hengine
Uma engine de Xadrez baseada em lances humanos.

## Introdução

A Hengine é uma engine de Xadrez baseadas em lances humanos. Basicamente, em função de um banco de dados de partidas acumuladas ao longo da historia do Xadrez, foi desenvolvido um algoritimo capaz de, em função do estado atual do tabuleiro de um jogo de Xadrez, sugerir o lance mais jogado naquela posição.

Os lances sugeridos pela Hengine são selecionados após uma análise que leva em conta:

1. Se o lance sugerido é de uma partida onde se obteve vitória
2. Qual o rating do jogador fez o lance
3. Média de partidas que fez o lance e obteve vitória

## Geração de Lances

Abaixo segue a arquitetura básica do processo de geração de lances:

### Arquitetura Básica
![Arquiterura de geração de lances](Hengine%20-%20Arquitetura.jpg)

