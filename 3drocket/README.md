# Relatório:
### Alunos: 
Mariana Miwa Okuma Miyashiro e Miguel dos Reis

### Nome e descrição do projeto:
*3D Rocket*

Nessa cena 3D, foram gerados um foguete, asteroides diversos e um starfield. A cena pode ser vista através de uma câmera virtual.

Interação:
* usando teclas direcionais (ou w,a,s,d) para modificar a direção para qual a câmera virtual está apontada
* usando scroll do mouse para modificar na vertical a direção da câmera    

### Detalhes do projeto:
Projeto baseado nos projetos *loadmodel*, *lookat* e *starfield* dados em aula no curso de Computação Gráfica [MCTA008-17]

Arquivos:
* main.cpp: define a função main do projeto
* openglwindow.hpp/.cpp: funções que carregam modelos, gerenciam o counteúdo na tela e definem os meios de interação com usuário
* model.hpp/.cpp: responsável po gerenciar modelo geométrico do starfield 
* asteroid.hpp/.cpp: gerencia os modelos geométricos dos três asteroides 
* camera.hpp/cpp: define comportamento da câmera virtual
* rocket.hpp/cpp: carrega o modelo geométrico do foguete
* vertex.gpp: define estrutura para vértices

### Técnicas utilizadas:
As técnicas utilizadas no projeto foram as seguintes:
* Geral: biblioteca abcg
* Foguete: carregamento do modelo com loadmodel
* Asteroides: são gerados em posições randômicas, sendo que para cada asteroide na lista de asteroides é escolhido um dos três modelos `.obj` e depois de gerados eles se mantém na mesma posição, girando em torno do próprio eixo
* Starfield: gerados de forma similar ao projeto *starfield*, modificando as velocidade, tamanho e posições nas quais os objetos são gerados. Foi utilizado um dos modelos de asteroide para gerar cada estrela do starfield, criando um 'estrelas cadentes' na cena.


### Video de Demonstração:
<video src='https://drive.google.com/file/d/1JNHZlrRcFAWX6cf9AG_rIUPENIzPi0Lo/view?usp=sharing' width=180/>