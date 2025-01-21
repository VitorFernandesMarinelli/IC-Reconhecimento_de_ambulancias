# IC-Reconhecimento_de_ambulancias

Esse repositorio, cotem os códigos do projeto de iniciação cientifica feita em 2024, com o objetivo de indentificar o melhor metodo de reconhecer ambulatorios moveis do SAMU, podendo ser aplicado em sistemas como semafaros inteligentes por exemplo.

# Tecnologias usadas

Usamos a plataforma do matlab em conjunto com os modelos YOLO v4 e Fast R-CNN.

# Desenvolvimento (Resumido)

Queriamos comparar dois modelos o YOLO v4 e o Fast R-CNN, alem de indentifica qual elemento é mais facil de ser reconhecido. Criamos 3 classes para cada modelo, uma para o simbulo da cruz vermelha, umas para o número 192 e uma para texto ambulancia.

Selecionamos alguns videos do youtube com ambulatorios moveis do SAMU em ação e por meio de um código em python, fizemos a quebra dos videos em frames. Separamos as melhores e dividimos 10%(validação):30%(treino):60%(testes).  

# Treinamento

Separamos 100 imagens para cada classe e treinamos em ambos os modelos. Usando 50 epocas para YOLO e 10 epocas para o Fast. 

Com um PC com uma GPU nvidia GTX 1500Ti com 6GB de memória, um processador intel core i5-6500 com 4 núcleos e 16 GB de memoria ram, levou 7 horas para treinar cada classe do modelo YOLO e 11 horas para cada classe do modelo Fast R-CNN.

# Resultados

## Precisão:
            YOLO                Fast R-CNN
Número:     Inconclusivo        Inconclusivo
Simbulo:    65%                 91%
Texto:      50%                 91%

## Velocidade para indentificar elementos:

YOLO: 3,16 segundos
Fast R-CNN: 24,58 segundos


# Conteudos

Na pasta detectores, tem os modelos usados para cada classe já treinados. Na pasta scripts tem os códigos do dois modelos, usados para o treino e o teste dos detectores. E na ultima há um conjunto de fotos selecionadas, e tabelas com as imagens selecionadas que foram usadas para o treino.