## Introdução

Este trabalho foi realizado por Bruno Guedes Spinelli, aluno do curso de Engenharia Biomédica da UFRN.

Existe uma grande evasão de alunos durante a disciplina de Lógica de Programação (LoP) derivada de diversos motivos, mas acredita-se que o maior causador dessa evasão seja a desmotivação decorrente das notas baixas do aluno. O objetivo deste trabalho é criar rede neural do tipo Self-Organizing Map (SOM) para tentar prever a situação final do aluno (reprovado ou aprovado) na disciplina LoP a partir da quantidade de submissões semanais do aluno, assim tornando possível a realização de feedbacks durante a disciplina que estimulem uma maior interação do aluno com o conteúdo ministrado e consequentemente aumentando sua chance de tirar notas melhores e diminuindo desta forma a evasão dos alunos.

A base de dados utilizada para treinar e testar a rede pode ser encontrada clicando [aqui], nela podemos observar as seguintes classificações de dados:

* **anoSubmissao, anoSigaa e anoTurma:** período em que foram realizadas as submissóes de atividades.
* **semana 1 - 21:** quantidade de atividades submetidas por semana.
* **descricaoTurma:** descrição da disciplina, turma e subturma.
* **turma:** descrição da turma do aluno.
* **situacao:** situação final do aluno.

## Metodologia


## Códigos

A rede neural foi codificada utilizando a linguagem de programacão Python. O programa utilizou as bibliotecas ```pandas```  para auxilizar no processo de importar o arquivo de dados , a bibliotéca e ```numpy``` para realizar operações matemáticas e também foi utilizado a bibliotéca ```minisom``` para criar a rede:

```py
import pandas as pd
import numpy as np
dataset =  pd.read_csv("https://raw.githubusercontent.com/ect-info/ml/master/dados/lop_submissao_semana.csv",index_col=False )
dataset.head()
```


<!-- Links -->

[aqui]: 

