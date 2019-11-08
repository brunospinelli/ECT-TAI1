# Reconhecimento de caracteres escritos a mão utilizando Multi-layer Perceptron (MLP)

## Introdução
Este trabalho foi realizado por Bruno Guedes Spinelli, aluno do curso de Engenharia Biomédica da UFRN.

O objetivo deste trabalho é desenvolver um algoritmo de  rede neural artificial convolucional do tipo Multi-layer Perceptron (MLP) capas de reconhecer e identificar caracteres escritos a mão. Para o treinamento da rede foi utilizada um banco de imagens contendo diversas imagens de cada letra do alfabeto (de A a Z, totalizando 26 letras) e para o teste foram utilizadas imagens contando caracteres feitos a mão em um programa de edição de imagem.

##Metodologia

O Perceptron foi o primeiro modelo de rede neural artificial criado com a capacidade de aprendizado. Sendo baseado no funcionamento dos neurônios e sinapses biológicas, o Perceptron é capaz de classificar as entradas, de forma binária, em dois grupos distintos e sua arquitetura é baseada em 3 elementos principais:

1) Uma camada de entrada (X).
2) Uma camada de saída (Y).
3) Um conjunto de pesos (W) ligando a entrada à saída.

![perceptron]

**Figura 1 - Representação de um Perceptron**

Neste tipo de rede a aprendizagem da rede é realizada pela modificação dos pesos (W) durante o seu treinamento. Entretanto, o Perceptron apenas é capaz de solucionar problemas linearmente separáveis, o que é um grande problema afinal problemas reais normalmente não podem ser solucionados apenas com uma reta para separar seus elementos. Por este motivo foi escolhido uma rede neural Multi-Layer Perceptron (MLP) para a realização dessa atividade.

O MLP é uma rede neural artificial muito parecida com o Perceptron, porém possui mais de uma camada de neurônios e pode ser utilizada para situações que exijam mais de uma reta para a separação correta dos elementos de entrada. Sua arquitetura consiste nos seguintes elementos:

1) Uma camada de entrada (X).
2) Uma ou mais camadas escondidas (Hidden layers).
3) uma camada de saída (Y).

![mlp]

**Figura 2 - Representação de um MLP**

O principio de funcionamento da MLP é dado pela propagação do sinal de entrada por todas as camadas da rede até que chegue a saída, ou seja, os neurônios das camadas subsequentes utilizam como entrasa o sinal de saída dos neurônios das camadas anteriores, seguida do calculo do erro, utilizando as saídas produzidas pelos neurônios da última camada, e da correção dos pesos de todos os neurônios, a partir da última camada, minimizando seus erros. Desta forma a cada treinamento realizado a rede neural tende a aumentar sua chance de acerto.

Uma rede neural convolucional (CNN do inglês Convolutional Neural network ou ConvNet) é uma classe de rede neural artificial que vem sendo aplicada com sucesso no processamento e análise de imagens digitais. Em uma CNN os dados, geralmente imagens, são pré-processados de modo que se evidencie as caracteristicas desejadas e então as caracteristicas do dado enviadas para a rede em um vetor de caracteristica, auxiliando a rede neural a ter uma melhor aprendizagem.




