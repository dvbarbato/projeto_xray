# projeto_xray - Classificador de Imagens

 Project status(Active)
 
# Objetivo do Projeto

O objetivo desse projeto é distinguir radiografias normais e de pacientes com pneumonia utilizando conceitos de Machine Learning.

# Métodos

  - EDA
  - Normalização de dados
  - Extração e Normalização de pixels das imagens
  - Construção e treinamento da rede neural.
  
# Tecnologias

  - Python
  - Pandas
  - Numpy
  - Seaborn
  - Tensorflow
  - Keras
  - OpenCV
  - Scikit-learn
  
# Descrição do Projeto

Para este projeto foi disponibilizado através da plataforma Kaggle(https://www.kaggle.com/competitions/knust-computer-vision-challenge/overview/description) um conjunto de dados com 5.856 imagens de raios-X (JPEG) divididas em 2 categorias (Pneumonia/Normal).
As imagens de raios-X foram selecionadas de pacientes pediátricos de um a cinco anos do Centro Médico Infantil e Mulheres de Guangzhou.

# Steps

- Importação das bibliotecas necessárias
- Extração dos Pixels das Imagens
- Normalização dos dados
- Execução das bases de treinamento e testes
- Construção e treinamento da rede neural
- Avaliação da rede neural
- Salvar a rede neural e seus pesos em arquivos json e hdf5
- Carregamento do arquivo contendo os pesos da rede neural.
  
# Conclusão

Ao construir a rede neural com a ativação sigmoid na ultima camada e compilar com o otimizador 'Adam' utilizando a metrica de 'accuracy' pode-se notar que na propria base de treinamento chegou em uma acurácia de 94%.

O erro (loss) começou com valor de aproximadamente 5, mas foi reduzindo a cada época chegando ao valor de 0.15. Enquanto que a accuracy iniciou com valor de 0,81 chegando ao valor de 94% o que mostou uma tendência de alta enquanto o erro diminuiu abruptamente entre a época 0 e 2 e se manteve na faixa de 0,15 a 0,20 até a última época.

Ao submeter cada uma das 1172 imagens de teste  à rede neural e aplicando o fator de probabilidade 50% de acerto para comparar X_teste com y_teste(onde estão as respostas corretas da rede neural) obteve uma taxa de acerto de 94%.

Atraves da matriz de confusao nota-se que 813 imagens com pneumonia foram classificadas corretamente e 26 imagens com pneumonia foram classificadas como Normal. Por outro lado tem 283 imagens normais que foram classificadas corretamente e 50 imagens normais classicadas como pneumonia.

Ao observar o recall na classe pneumonia o algoritmo conseguiu identificar 97% das imagens com uma precisão de 94%. 
Por outro lado o algoritmo conseguiu identificar 85% das imagens como normal estando correto em 92% dos casos.

Logo, pode -se notar que o desempenho para classificar as imagens como NORMAL pode ser melhorado futuramente ao executar testes com métricas diferentes para tentar aumentar o valor do Recall da respectiva classe.



# Imagens e gráficos

### Exemplos com imagens 
![Captura de Tela 2023-03-09 às 21 47 28](https://user-images.githubusercontent.com/92690205/224195309-d0425d6b-6a2a-45b1-8cc9-a2e44df1f7d4.png)

### Distribuição do Dataset contendo 4273 imagens indicando pneumonia e 1583 indicando normalidade 
![Captura de Tela 2023-03-09 às 21 48 06](https://user-images.githubusercontent.com/92690205/224195316-12b5234b-4d73-4943-ac5d-71989caa05e2.png)

### Gráficos indicando o erro e acurácia

![Captura de Tela 2023-03-10 às 00 19 59](https://user-images.githubusercontent.com/92690205/224214879-9ac05b70-f9ba-46d0-b2ed-7b2b98c4c04f.png)

### Matriz Confusão
![Captura de Tela 2023-03-10 às 00 19 24](https://user-images.githubusercontent.com/92690205/224214862-5c2d1624-f26b-446d-a108-c4df62045d84.png)


# Contact
  https://www.linkedin.com/in/david-barbato-9961b631/
