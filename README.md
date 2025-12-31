# Diabetes Prediction with MLflow (MLOps Project)

---

## 🇧🇷 Português

###  Visão Geral do Projeto

Este projeto implementa um **pipeline end-to-end de Machine Learning** para **previsão de diabetes**, com foco em **Engenharia de Machine Learning e MLOps**. O objetivo principal não é apenas treinar um modelo preditivo, mas demonstrar como estruturar, rastrear, versionar e avaliar modelos de forma **reproduzível e profissional**, utilizando **MLflow**.

---

###  Problema

Prever a progressão/ocorrência de diabetes a partir de variáveis clínicas, utilizando modelos de Machine Learning supervisionados.

---

###  Dataset

O dataset utilizado é o **Diabetes Dataset** (amplamente utilizado em estudos acadêmicos e benchmarks), contendo variáveis numéricas relacionadas a características clínicas dos pacientes.

* Features: variáveis clínicas numéricas
* Target: valor contínuo relacionado à progressão da doença

---

###  Pipeline de Machine Learning

O pipeline implementado segue as seguintes etapas:

1. Carregamento e exploração dos dados
2. Separação em conjuntos de treino e teste
3. Treinamento de modelo Random Forest
4. Hyperparameter tuning com GridSearch
5. Avaliação com Mean Squared Error (MSE)
6. Rastreamento de experimentos com MLflow
7. Versionamento e salvamento de artefatos do modelo

---

###  Modelagem e Hyperparameter Tuning

Foi utilizado o algoritmo **Random Forest Regressor**, com ajuste automático de hiperparâmetros, incluindo:

* `n_estimators`
* `max_depth`
* `min_samples_split`
* `min_samples_leaf`

O melhor modelo é selecionado automaticamente com base na métrica de avaliação.

---

###  Avaliação

A métrica utilizada para avaliação foi:

* **Mean Squared Error (MSE)**

Essa métrica permite comparar diferentes execuções (runs) e selecionar o melhor modelo de forma objetiva.

---

###  MLflow e MLOps

O MLflow é utilizado para:

* Rastreamento de experimentos (runs)
* Registro de hiperparâmetros
* Registro de métricas
* Salvamento de artefatos do modelo
* Inferência de assinatura do modelo

O projeto detecta automaticamente se o MLflow está sendo executado em modo local (`file`) ou servidor (`http`), adaptando o processo de logging do modelo.

Isso simula um cenário real de produção, onde modelos podem ser registrados e versionados.

---

###  Como Executar o Projeto

1. Criar ambiente virtual
2. Instalar dependências:

```bash
pip install -r requirements.txt
```

3. Executar o notebook ou script de treinamento
4. Iniciar o MLflow UI:

```bash
mlflow ui
```

5. Acessar em: `http://127.0.0.1:5000`

---

###  Tecnologias Utilizadas

* Python
* Scikit-learn
* MLflow
* Pandas / NumPy
* Jupyter Notebook

---

###  Conclusão

Este projeto demonstra a transição de um modelo de Machine Learning experimental para um **pipeline rastreável, reproduzível e pronto para produção**, aplicando conceitos fundamentais de **MLOps** e **Engenharia de Machine Learning**.

---

## 🇺🇸 English

###  Project Overview

This project implements an **end-to-end Machine Learning pipeline** for **diabetes prediction**, with a strong focus on **Machine Learning Engineering and MLOps**. The goal is not only to train a predictive model, but to demonstrate how to structure, track, version, and evaluate ML models in a **reproducible and production-oriented way** using **MLflow**.

---

###  Problem Statement

Predict diabetes progression/outcome based on clinical features using supervised Machine Learning models.

---

###  Dataset

The project uses the **Diabetes Dataset**, a widely adopted dataset in academic research and ML benchmarks.

* Features: numerical clinical attributes
* Target: continuous value related to disease progression

---

###  Machine Learning Pipeline

The implemented pipeline includes:

1. Data loading and exploration
2. Train-test split
3. Random Forest model training
4. Hyperparameter tuning using GridSearch
5. Evaluation using Mean Squared Error (MSE)
6. Experiment tracking with MLflow
7. Model artifact versioning and storage

---

###  Modeling and Hyperparameter Tuning

A **Random Forest Regressor** was used, with automated hyperparameter tuning, including:

* `n_estimators`
* `max_depth`
* `min_samples_split`
* `min_samples_leaf`

The best model is automatically selected based on evaluation metrics.

---

###  Evaluation

The evaluation metric used was:

* **Mean Squared Error (MSE)**

This metric allows objective comparison between different experiment runs.

---

###  MLflow and MLOps

MLflow is used for:

* Experiment tracking
* Hyperparameter logging
* Metric logging
* Model artifact storage
* Model signature inference

The pipeline automatically detects whether MLflow is running locally (`file`) or as a tracking server (`http`), adapting the model logging strategy accordingly.

This approach closely resembles real-world production ML systems.

---

###  How to Run the Project

1. Create a virtual environment
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the training notebook or script
4. Start MLflow UI:

```bash
mlflow ui
```

5. Access at: `http://127.0.0.1:5000`

---

###  Technologies Used

* Python
* Scikit-learn
* MLflow
* Pandas / NumPy
* Jupyter Notebook

---

###  Conclusion

This project demonstrates the transition from an experimental Machine Learning model to a **reproducible, trackable, and production-ready ML pipeline**, applying key **MLOps and Machine Learning Engineering** principles.
