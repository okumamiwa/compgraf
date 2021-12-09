# Relatório:
### Alunos: 
Mariana Miwa Okuma Miyashiro e Miguel dos Reis

### Nome e descrição do projeto:
*3D Rocket*

Nessa cena 3D, foram gerados um foguete, asteroides diversos e um starfield, simulando uma nave flutuando pelo espaço. A cena pode ser vista através de uma câmera virtual.

Interação:
* usando teclas direcionais (ou w,a,s,d) para modificar a direção para qual a câmera virtual está apontada
* usando scroll do mouse para modificar na vertical a direção da câmera    
* com o clique do mouse o foguete se move para frente

### Detalhes do projeto:
Projeto baseado nos projetos *loadmodel*, *lookat*, *starfield* e nas diversas versões de *viewers* dados em aula no curso de Computação Gráfica [MCTA008-17]

Arquivos:
* main.cpp: define a função main do projeto
* openglwindow.hpp/.cpp: funções principais do programa, que carregam os modelos, gerenciam o counteúdo na tela e definem os meios de interação com usuário
* model.hpp/.cpp: responsável por gerenciar a renderização do starfield 
* asteroid.hpp/.cpp: gerencia os modelos geométricos dos asteroides 
* camera.hpp/cpp: define comportamento da câmera virtual
* rocket.hpp/cpp: carrega o modelo geométrico do foguete
* vertex.gpp: define estrutura de dado para os vértices

### Técnicas utilizadas:
As técnicas utilizadas no projeto foram as seguintes:
* Geral: biblioteca abcg
* Foguete: carregamento do modelo com loadmodel
* Asteroides: são gerados em posições randômicas dentro de um espaço limitado um pouco maior que o espaço visível, sendo que são usados dois modelos `.obj` diferentes. Além disso, a direção dos movimentos e das rotações de cada um deles também são randômicas.
* Starfield: gerados de forma similar ao projeto *starfield*, modificando as velocidade, tamanho e posições nas quais os objetos são gerados. Foi utilizado um dos modelos de asteroide para gerar cada estrela do starfield, criando 'estrelas cadentes' na cena.
* Iluminação e textura: utilizado mapeamento de normais com o modelo de Blinn-Phong afim de atingir o máximo de realismo possível

### Problemas encontrados:
* Ao realizar a compilação para WebAssembly, foi possível rodar a aplicação no servidor local, mas não através do github.io.
* A grande quantidade de elementos em tela tornou a aplicação excessivamente pesada, prejudicando o movimento do asteroides no *starfield*


### Video de Demonstração:
* Link do Video: [Google Drive](https://drive.google.com/file/d/1iMEJ74p8OBdjSPd3J4kLwzPWko8RW0OO/view?usp=sharing) 

![3DRocket](https://github.com/okumamiwa/compgraf/blob/main/3drocket2/3drocket2.gif)