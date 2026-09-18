# 🚗 Car Pricing Prediction

Projeto simples de **Machine Learning** para prever o preço de carros a partir de suas características, desenvolvido para fins educacionais como exercício de regressão com redes neurais.

## 📋 Sobre o projeto

O notebook `CarPricePredication.ipynb` implementa um pipeline completo de regressão utilizando **TensorFlow/Keras**, desde o carregamento e preparação dos dados até o treinamento e avaliação de uma rede neural profunda (Deep Neural Network) que estima o preço de um veículo com base em 8 variáveis de entrada.

## 🛠️ Tecnologias utilizadas

- **Python**
- **TensorFlow / Keras** — construção e treinamento do modelo
- **Pandas** — manipulação dos dados
- **NumPy** — operações numéricas
- **Seaborn / Matplotlib** — visualização de dados e curvas de treinamento
- **Google Colab** — ambiente de execução (notebook com badge "Open in Colab")

## 📊 Dados

Os dados são carregados a partir de um arquivo `train.csv`, convertidos em tensores e embaralhados antes da divisão em conjuntos de:

- **Treino:** 80%
- **Validação:** 10%
- **Teste:** 10%

## 🧠 Arquitetura do modelo

O modelo é uma rede neural sequencial (`tf.keras.Sequential`) com:

- Camada de entrada com 8 features
- Camada de **normalização** dos dados
- Múltiplas camadas densas (`Dense`) com ativação `ReLU`, variando entre 32 e 256 neurônios
- Camada de saída com 1 neurônio (valor previsto do preço)

**Configuração de treinamento:**
- Otimizador: `Adam` (learning rate = 0.000001)
- Função de perda: `MeanAbsoluteError` (MAE)
- Épocas: 600

## ▶️ Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/mrJoao28/Car-pricing-prediction-.git
   ```
2. Abra o notebook `CarPricePredication.ipynb` no Jupyter ou no Google Colab (há um botão de acesso direto no topo do notebook).
3. Instale as dependências necessárias, caso não esteja usando o Colab:
   ```bash
   pip install tensorflow pandas seaborn matplotlib numpy
   ```
4. Certifique-se de ter o arquivo `train.csv` no mesmo diretório do notebook.
5. Execute as células em sequência para treinar e avaliar o modelo.

## 📈 Resultados

Após o treinamento, o modelo é avaliado no conjunto de teste (`model.evaluate`) e é feita uma predição de exemplo comparada ao valor real, permitindo visualizar o desempenho do modelo na prática. A evolução da perda (loss) ao longo das épocas é plotada para acompanhar o processo de treinamento e validação.

## 🎯 Objetivo

Este projeto foi criado com fins **educacionais**, como prática de conceitos de preparação de dados, normalização, construção de redes neurais com Keras e avaliação de modelos de regressão.

## 👤 Autor

Desenvolvido por [João](https://github.com/mrJoao28).

## 📄 Licença

Projeto de estudo, livre para uso educacional.
