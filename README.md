# Atividade Prática 1: Classificação de Raças de Cães com Transfer Learning

Este repositório contém a implementação da **Atividade Prática 1 da disciplina Tópicos para Computação 1 (2026.1)**, ministrada pela **Profa. Dra. Elloá B. Guedes** na **Escola Superior de Tecnologia (EST/UEA)**.

Nesta atividade foi desenvolvido um sistema de **classificação de imagens de raças de cães** utilizando **Transfer Learning** com a arquitetura **EfficientNetV2-S**.

---

# 📁 Estrutura do Projeto
```
├── TopicosI-AP1-TransferLearning.ipynb
├── models/
│ └── best_model.pth
├── training_log.csv
├── slides/
│ └── apresentacao.pdf
└── README.md
```


- **TopicosI-AP1-TransferLearning.ipynb** → Notebook com toda a implementação do treinamento e avaliação  
- **models/** → Modelos treinados salvos durante o treinamento  
- **training_log.csv** → Registro das métricas de treinamento  
- **slides/** → Apresentação com resultados e análise experimental  
- **README.md** → Documentação do projeto  

---

# ⚙️ Descrição da Atividade

O objetivo da atividade é aplicar **técnicas avançadas de treinamento de redes neurais profundas** para resolver um problema de **classificação multiclasse de imagens**.

O dataset utilizado foi o **Stanford Dogs Dataset**, que contém aproximadamente **20 mil imagens distribuídas em 120 raças de cães**.

Devido à grande variedade de classes e à similaridade visual entre algumas raças, o problema exige o uso de **modelos profundos e técnicas de regularização e otimização**.

---

# 🧠 Arquitetura Utilizada

O modelo escolhido foi a **EfficientNetV2-S**, uma arquitetura moderna de redes convolucionais profundas otimizada para **alto desempenho e eficiência computacional**.

Foi utilizada a técnica de **Transfer Learning**, onde:

- A rede pré-treinada em **ImageNet** é utilizada como extratora de características
- As camadas finais são adaptadas para o problema de **classificação de 120 raças**

Essa abordagem permite:

- Reduzir o tempo de treinamento
- Melhorar a capacidade de generalização
- Aproveitar características visuais aprendidas previamente

---

# 🔎 Técnicas Utilizadas

Durante o desenvolvimento foram aplicadas diversas técnicas para melhorar o desempenho do modelo.

## 🔸 Transfer Learning

Utilização de um modelo **pré-treinado** para aproveitar conhecimento previamente aprendido em grandes bases de imagens.

---

## 🔸 Data Augmentation

Foram aplicadas transformações nas imagens para aumentar artificialmente o conjunto de dados e reduzir overfitting:

- Random Horizontal Flip
- Random Rotation
- Random Resized Crop
- Normalização dos pixels

---

## 🔸 Taxa de Aprendizado Adaptativa

Foi utilizado um **scheduler de taxa de aprendizado**, permitindo ajustar dinamicamente o learning rate ao longo do treinamento, melhorando a convergência do modelo.

---

## 🔸 Regularização L2

Aplicação de **weight decay** no otimizador para penalizar pesos muito grandes e melhorar a capacidade de generalização da rede.

---

## 🔸 Early Stopping

Foi implementado **Early Stopping**, interrompendo o treinamento quando o desempenho no conjunto de validação deixa de melhorar após um determinado número de épocas.

Essa técnica evita **overfitting** e reduz o tempo de treinamento.

---

# 📊 Monitoramento do Treinamento

Durante o treinamento foram monitorados:

- **Loss de treinamento**
- **Loss de validação**
- **Acurácia de treinamento**
- **Acurácia de validação**
- **Tempo total de treinamento**

Essas métricas foram registradas e posteriormente utilizadas para gerar **gráficos de evolução do treinamento**.

---

# 📈 Visualização de Resultados

Foram gerados gráficos mostrando:

- Evolução da **loss durante o treinamento**
- Evolução da **acurácia durante o treinamento**
- Comparação entre **treino e validação**

Esses gráficos ajudam a analisar o comportamento do modelo e identificar possíveis problemas como **overfitting ou underfitting**.

---

# 📏 Avaliação no Conjunto de Teste

Após o treinamento, o modelo foi avaliado utilizando o conjunto de teste.

As métricas utilizadas incluem:

- **Acurácia**
- **Precisão (Precision)**
- **Recall**
- **F1-score**

Essas métricas permitem avaliar o desempenho do modelo em um cenário de **classificação multiclasse**.

---

# ⏱️ Monitoramento de Tempo de Treinamento

Foi realizado o monitoramento do **tempo total de treinamento**, permitindo avaliar o custo computacional do modelo e comparar diferentes configurações de treinamento.

---

# 🔢 Quantidade de Parâmetros

Foi calculado o número de parâmetros do modelo utilizando ferramentas de análise de arquitetura.

São apresentados:

- **Total de parâmetros**
- **Parâmetros treináveis**
- **Parâmetros congelados**

Essa análise ajuda a entender a **complexidade do modelo** e o impacto do Transfer Learning.

---

# 📊 Apresentação dos Resultados

Além do notebook, foi elaborado um **conjunto de slides** contendo:

- Descrição da arquitetura EfficientNetV2-S
- Metodologia utilizada
- Resultados experimentais
- Gráficos de treinamento
- Métricas obtidas no conjunto de teste

---

# 🧰 Tecnologias Utilizadas

- **Python**
- **PyTorch (`torch`, `torch.nn`, `torch.optim`)**
- **Torchvision**
- **NumPy**
- **Matplotlib**
- **Pandas**
- **Scikit-learn**
- **Torchinfo**

---

# 👥 Equipe

**Equipe 1**

| [<img src="https://github.com/thiagocordeirum.png?size=100" width=100><br><sub>Thiago Cordeiro</sub>](https://github.com/thiagocordeirum) | [<img src="https://github.com/cpc231341.png?size=100" width=100><br><sub>Cristiano Peniche</sub>](https://github.com/cpc231341) | [<img src="https://github.com/andradepv.png?size=100" width=100><br><sub>Paulo Andrade</sub>](https://github.com/andradepv) | [<img src="https://github.com/jaum36.png?size=100" width=100><br><sub>João Victor</sub>](https://github.com/jaum36) | [<img src="https://github.com/pedroituassu.png?size=100" width=100><br><sub>Pedro Ituassú</sub>](https://github.com/pedroituassu) |
|:---:|:---:|:---:|:---:|:---:|

Modelo utilizado pela equipe: **EfficientNetV2-S**

---

# 👩‍🏫 Orientação

- **Profa. Dra. Elloá B. Guedes**  
- **Disciplina:** Tópicos para Computação 1  
- **Instituição:** Escola Superior de Tecnologia – Universidade do Estado do Amazonas (EST/UEA)  
- **Período:** 2026.1
