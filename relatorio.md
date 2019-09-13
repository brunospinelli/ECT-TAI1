# Previsão da situação final (aprovação ou não) de alunos utilizando Multi-layer Perceptron (MLP)

## Introdução

Este trabalho foi realizado por Bruno Guedes Spinelli.

O objetivo deste trabalho é realizar uma previsão da situação final, possivel aprovação ou reprovação, de alunos a partir de dados coletados sobre as atividades realizadas, ou não, pelo aluno. Para conseguir realizar a previsão foi utilizado Multi-layer Perceptron (MLP), um tipo de rede neural artificial. A base de dados utilizada pode ser encontrada clicando aqui, nela podemos obervar as sequintes atributos de dados:

qsemana: quantidade de dias diferentes que houve submissão de questões

submeteu: quantidade de questões submetidas pelo aluno por semana

subListaLab: quantidade de submissões na lista de laboratório a cada 2 semanas

subListaExer: quantidade de submissões na lista de exercícios a cada 2 semanas

subDistintasLab: quantidade de dias em que submeteu, a cada 2 semanas, nas listas de lab

subDistintasExer: quantidade de dias em que submeteu, a cada 2 semanas, nas listas de exer

diferentesLabSemanas: quantidade de questões diferentes submetidas nas listas de laboratório a cada 2 semanas

diferentesExerSemanas: quantidade de questões diferentes submetidas nas listas de exercícios a cada 2 semanas

situacao: indica se o aluno foi aprovado (1) ou reprovado (0)

qsub: quantidade de submissões das listas correspondente (seja lab ou exercicio)

qsubp: uantidade de questões submetidas para a prova 1 (L1,L2,L3) ou da prova 2 (L4,L5)

totalsub: total de submissões feitas pelo aluno

igualACem: quantidade de submissões em que o aluno acertou 100%, seja nas L123 ou L45


* Apresentar os membros da equipe. 
* Descrever o problema.  
* Descrever a base de dados.  

## Metodologia 

O Perceptron foi o primeiro modelo de rede neural artificial criado com a capacidade de aprendizado. Sendo baseado no funcionamento dos neurônios e sinapses biológicas, o Perceptron é capaz de classificar as entradas, de forma binária, em dois grupos distintos e sua arquitetura é baseada em 3 elementos principais:

1) Uma camada de entrada (X).
2) Uma camada de saída (Y).
3) Um conjunto de pesos (W) ligando a entrada à saída.

Neste tipo de rede a aprendizagem da rede é realizada pela modificação dos pesos (W) durante o seu treinamento. Entretanto, o Perceptron apenas é capaz de solucionar problemas linearmente separáveis, o que é um grande problema afinal problemas reais normalmente não podem ser solucionados apenas com uma reta para separar seus elementos. Por este motivo foi escolhido uma rede neural Multi-Layer Perceptron (MLP) para a realização dessa atividade.

O MLP é uma rede neural artificial muito parecida com o Perceptron, porém possui mais de uma camada de neurônios e pode ser utilizada para situações que exijam mais de uma reta para a separação correta dos elementos de entrada. Sua arquitetura consiste nos seguintes elementos:

1) Uma camada de entrada (X).
2) Uma ou mais camadas escondidas (Hidden layers).
3) uma camada de saída (Y).

O principio de funcionamento da MLP é dado pela propagação do sinal de entrada por todas as camadas da rede até que chegue a saída, ou seja, os neurônios das camadas subsequentes utilizam como entrasa o sinal de saída dos neurônios das camadas anteriores, seguida do calculo do erro, utilizando as saídas produzidas pelos neurônios da última camada, e da correção dos pesos de todos os neurônios, a partir da última camada, minimizando seus erros. Desta forma a cada treinamento realizado a rede neural tende a aumentar sua chance de acerto.

Com o objetivo de tentar prever a aprovação ou não dos alunos os seguintes atributos foram escolhidos, com o intuito de indicar se o aluno está, ou não, estudando o conteúdo e realizando as atividasdes passadas com sucesso:

1) notaProva1
2) totalsub
3) igualACeml123
4) igualACeml45


* Explicar o modelo de _machine learning_ (ML) que você está trabalhando. 
* Explicar as etapas do treinamento e teste. 
* Caso tenha selecionado atributos, explicar a motivação para a seleção de tais atributos. 

## Códigos 

A rede neural foi codificada utilizando a linguagem de programacão Python. O programa utilizou a bibliotéca Pandas e numpy para auzilizar no processo de importar o arquivo de dados e realizar operaoes matemáticas com os mesmos:

```py
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

dataset = pd.read_csv('https://raw.githubusercontent.com/ect-info/ml/master/dados/DataBaseLop.csv')
```


* Mostrar trechos de códigos mais importantes e explicações.  

## Experimentos 

* Descrever em detalhes os tipos de testes executados. 
* Descrever os parâmentros avaliados. 
* Explicar os resultados. 
