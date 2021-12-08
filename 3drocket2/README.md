# Relatório:
### Alunos: 
Mariana Miwa Okuma Miyashiro e Miguel dos Reis

### Nome e descrição do projeto:
*3D Rocket*

Nessa cena 3D, foram gerados um foguete, asteroides diversos e um starfield. E foram aplicadas iluminação e textura em cada objeto. A cena pode ser vista através de uma câmera virtual.

Interação:
* usando teclas direcionais (ou w,a,s,d) para modificar a direção para qual a câmera virtual está apontada
* usando scroll do mouse para modificar na vertical a direção da câmera    

### Detalhes do projeto:
Iluminação e texturização do Projeto baseadas nos projetos *viewer2* a *viewer5* dados em aula no curso de Computação Gráfica [MCTA008-17]

Em relação à atividade 2 foram adicionados:
* arquivos `.mtl` (asteroid1, asteroid2 e rocket): carregam as propriedades dos materiais de cada objeto
* arquivos `.png`/`.tga`: imagens para o mapeamento de textura dos materiais de cada objeto

### Técnicas utilizadas:
As técnicas utilizadas no projeto foram as seguintes:
* Geral: biblioteca abcg
* Shaders: normalmapping.vert e normalmapping.frag (utilizados no *viewer5*), que aplica o modelo de reflexão de Blinn–Phong e o mapeamento de normais
* Leitura do arquivo .mtl: na função loadObj de model, asteroid e rocket, é feita a procura do path para o arquivo mtl indicado no arquivo obj, assim é possível adquirir as propriedades específicas do material do objeto (Ka, Kd, Ks, shininess e nomes dos arquivos de textura difusa e normal)
* Carregamento de texturas: funções `loadDiffuseTexture` e `loadNormalTexture`, definidas para model, asteroid e rocket, sendo que ambas as funções utilizam a `abcg::opengl::loadTexture`
* vertex.hpp: a estrutura Vertex tem os atributos adicionais normal(carregado a partir do objeto ou da função `computeNormals`), texCoord(carrega a partir do arquivo obj) e tangent (computado através de `computeTangents` quando há coordenadas de texturas)
* openglwindow.cpp: a função paintGL é modificada para passar as informações necessárias para os shaders (variáveis uniformes para matrizes de visualização, diffuseTexLoc, mappingModeLoc, normalTexLoc, coeficientes para iluminação). Também foram implementadas funções para carregar as propriedades dos materiais dos objetos carregados, passar para as variáveis dos shaders (KaLoc, KdLoc, KsLoc e shininessLoc) e renderizar cada objeto da cena.
* asteroid3: como o obj não tinha mtl associado a ele foram utilizados coeficientes default e texturas dos outros asteroides
* rocket: o `pattern_normal.png` foi utilizado como textura normal

### Problemas encontrados:
Ao realizar a compilação para WebAssembly, foi possível rodar a aplicação no servidor local, mas não através do github.io


### Video de Demonstração:
* Link do Video: [Google Drive](https://drive.google.com/file/d/1JNHZlrRcFAWX6cf9AG_rIUPENIzPi0Lo/view?usp=sharing) 

![3DRocket](https://github.com/okumamiwa/compgraf/blob/main/3drocket/3drocket.gif)