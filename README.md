# Power Method and Random Walks
Neste repositório, responderemos algumas perguntas relacionadas à um clássico jogo de tabuleiros Snake and Ladders

### ![Problema](https://imgur.com/u1JyqTp)
A imagem acima representa o tabuleiro do jogo Snake and Ladders. As regras do jogo são bem simples:

1: Os jogadores começam na casa 1.
2: Na sua vez, o jogador deve arremessar uma moeda. Se o resultado for cara, ele anda uma casa. Caso for coroa, ele anda duas.
3: Caso o jogador, logo após realizar seu movimento parar no começo de uma escada, ele automaticamente sobe para o final dela. E caso o jogador parar na boca de uma cobra, ele desce até sua cauda.
4: Ganha o jogador que chegar primeiro à casa 36.

### ![Diagrama](https://imgur.com/HJBNl0L)

A imagem representa o grafo do tabuleiro. À partir dele podemos extrair a matriz P de adjascências.

### ![Distribuição P](https://imgur.com/x6oI8HY)

Após montarmos a matriz P no script, rodamos o Power Method para extrair a distribuição estacionária. Obtivemos assim, as probabilidades que o jogador tem de cair em cada uma das casas em 100 rodadas. (Imagem acima).
O Estado 36 (Final do jogo) tem probabilidade de 93% de ser acessado após 100 iterações, e logo atrás dele, temos o estado 31, com pouco mais de 1% de chance.

Montamos também a matriz P_, que é a matriz de adjascências que admite saltos aleatórios com alpha = 0.1.
Segue abaixo os resultados da distribuição estacionária da matriz P_.

### ![Distribuição P_](https://imgur.com/ci0sxT8)

Claramente, os resultados são diferentes. Sem saltos aleatórios, o jogador tem 93% de chance de sair vitorioso após 100 iterações, diferentemente da iteração com saltos, que só possui 18%

O Script inteiro do exemplo está contido no arquivo T1.py
