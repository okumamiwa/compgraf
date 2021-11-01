# Relatório:
### Alunos: 
Mariana Miwa Okuma Miyashiro e Miguel dos Reis

### Nome e descrição do projeto:
*Rocket Trip*

Neste jogo o usuário deve tentar se desviar dos obstáculos de cor azul/verde, tentando chegar o mais longe possível. O acúmulo de pontos se dá através do tempo do jogo e ao colidir com as bolinhas amarelas, que também adicionam pontos. 

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
* Biblioteca abcg

### Projeto em WebAssembly:
[Rocket Trip](https://okumamiwa.github.io/compgraf/rocket/)

![image](https://github.com/okumamiwa/compgraf/blob/main/rocket/rocketTrip.png)