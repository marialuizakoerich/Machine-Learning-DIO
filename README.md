# Azure Machine Learning — ML na Prática (AutoML)

Este projeto documenta a criação, treinamento, registro e implantação de um modelo de **Machine Learning** utilizando o **Azure Machine Learning** com **ML Automatizado (AutoML)**, desenvolvido como parte de um laboratório prático.

---

## 🧠 Objetivo

Demonstrar, de forma prática, o fluxo completo de Machine Learning no Azure ML, incluindo:

- Criação do workspace
- Configuração do AutoML
- Treinamento de um modelo de regressão
- Registro do modelo
- Implantação em um ponto de extremidade
- Teste do modelo implantado

---

## 🛠️ Tecnologias Utilizadas

- Azure Machine Learning
- Azure Machine Learning Studio
- ML Automatizado (AutoML)
- Dataset tabular (Bike Rentals)

---

## 📌 Etapas do Projeto

### 1. Criação do recurso Azure Machine Learning

- Acesso ao **Portal do Azure**
- Criação de um novo recurso **Azure Machine Learning** via Marketplace
- Definição de:
  - Assinatura
  - Grupo de recursos
  - Nome do workspace

Após a validação, o recurso foi criado com sucesso.

---

### 2. Configuração do Workspace

- Configurações mantidas no padrão (ambiente de laboratório)
- Criação finalizada através da opção **Consultar + criar**

---

### 3. Criação e Treinamento do Modelo (AutoML)

#### 3.1 Criação do trabalho de ML Automatizado

No **Azure Machine Learning Studio**:

- Acesso ao menu **ML automatizado**
- Criação de um novo trabalho
- Preenchimento de:
  - Nome do trabalho
  - Nome do experimento
  - Descrição

---

#### 3.2 Tipo de tarefa e dados

- Tipo de tarefa: **Regressão**
- Criação de um novo conjunto de dados:
  - Tipo: **Tabular**
  - Fonte: **Arquivos da Web**

Dataset utilizado: https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/main/data/ml/daily-bike-share.csv


> Observação: Esta URL foi utilizada devido a problemas de validação na URL padrão do laboratório.

---

#### 3.3 Configuração da tarefa

- Coluna de destino (target): `rentals`
- Limites configurados conforme o laboratório
- **Encerramento antecipado** habilitado
- Tipo de validação: **Divisão de validação de treinamento**

Após a revisão das configurações, o trabalho de treinamento foi enviado.

---

### 4. Registro do Modelo

Após a conclusão do treinamento:

- O melhor modelo foi registrado
- Definição de:
  - Nome do modelo
  - Versão

O modelo ficou disponível no menu **Modelos** do Azure ML Studio.

---

### 5. Implantação do Modelo

- Tentativa inicial de implantação direta pelo modelo (opção indisponível)
- Implantação realizada via menu **Pontos de extremidade**
- Criação de um novo endpoint com:
  - Modelo selecionado
  - Configurações padrão
  - Contagem de instâncias: **1**

Após a implantação, o endpoint ficou ativo.

---

### 6. Teste do Modelo

- Acesso à aba **Testar** do ponto de extremidade
- Envio de dados de teste no formato **JSON**
- Validação do funcionamento do modelo implantado

---

## ✅ Resultado

O modelo foi treinado, registrado e implantado com sucesso, permitindo a realização de inferências por meio de um endpoint no Azure Machine Learning.
