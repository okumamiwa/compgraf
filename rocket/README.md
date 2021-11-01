# Relatório:
### Alunos: 
Mariana Miwa Okuma Miyashiro e Miguel dos Reis

### Nome e descrição do projeto:
*Rocket Trip*

Neste jogo o usuário deve tentar se desviar dos obstáculos de cor azul/verde, tentando chegar o mais longe possível. O acúmulo de pontos se dá através do tempo do jogo e ao colidir com as bolinhas amarelas(scorestars), que também adicionam pontos. 

Movimentos:
* direita e esquerda
* aceleração (usado barra de espaço)

### Detalhes do projeto:
Projeto baseado no *asteroids* dado em aula na semana 5 do curso de Computação Gráfica [MCTA008-17]

Arquivos:
* main.cpp: define a função main do projeto e possui vsync ativado para ajustar o frame rate do jogo ao rodar localmente ou em WebAssembly
* gamedata.hpp:define a estrutura do jogo, descreve estado atual e os dispositivos de entrada
* rocket.hpp/.cpp: declara e implementa o foguete que faz o trajeto do jogo
* obstacles.hpp/.cpp: declara e implementa os objetos dos quais o foguete deve desviar
* scorestars.hpp/cpp: declara e implementa objetos com os quais o usuário pode ganhar pontos ao colidir o foguete com eles

### Técnicas utilizadas:
As técnicas utilizadas no projeto foram as seguintes:
* Geral: biblioteca abcg
* Obstáculos e scorestars: foi utilizado como base o exercício de geração de polígonos dado em aula, modificando-o para gerar um conjunto de objetos a cada intervalo (definido de forma inversamente proporciconal à velocidade do jogo, que aumenta com o tempo) e movendo os objetos para baixo na tela na velocidade do foguete para criar o movimento do jogo na vertical
* Foguete: não se movimenta na vertical na tela em si, se movimenta apenas para direita e esquerda dado os limites da tela do jogo. Aplica aceleração ao aumentar a "velocidade do foguete", ou seja, a velocidade em que os objetos se movem para baixo, até um limite default de aceleração.
* Coloração dos objetos: também baseada nos exercícios de geração de triângulos/polígonos. As scorestars tem apenas uma cor sólida amarela e os obstáculos tem cores azuis/verdes geradas aleatoriamente utilizando *std::default_random_engine*.


### Projeto em WebAssembly:
[Rocket Trip](https://okumamiwa.github.io/compgraf/rocket/)

![image](https://github.com/okumamiwa/compgraf/blob/main/rocket/rocketTrip.png)