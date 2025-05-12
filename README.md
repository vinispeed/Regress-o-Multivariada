# Projeto de Regressão Multivariada

Este projeto utiliza técnicas de regressão multivariada para prever o peso de indivíduos com base em diversas variáveis explicativas. O modelo principal utilizado é o **Lasso Regression**, com validação cruzada (k-fold) para avaliar o desempenho.

## Estrutura do Projeto

- **`Dados_Peso_Curso_IA.xlsx`**: Arquivo contendo os dados utilizados no projeto.
- **`regrecao_multivariada.ipynb`**: Notebook principal com a implementação do modelo e análise.

## Etapas do Projeto

1. **Exploração Inicial dos Dados**:
   - Verificação de valores nulos e tipos de dados.
   - Análise estatística descritiva e visualização gráfica.

2. **Pré-processamento dos Dados**:
   - Remoção de valores nulos.
   - Identificação e remoção de outliers com base no z-score.

3. **Análise de Correlação**:
   - Cálculo da matriz de correlação.
   - Identificação das variáveis mais relevantes para a previsão do peso.

4. **Modelagem**:
   - Configuração de validação cruzada (k-fold).
   - Treinamento e ajuste de hiperparâmetros para os modelos:
     - **Ridge Regression**
     - **Lasso Regression**
     - **Random Forest Regression**

5. **Avaliação do Modelo**:
   - Cálculo de métricas de desempenho: MAE (Erro Absoluto Médio).
   - Comparação entre os modelos com base na média e desvio padrão do MAE.

6. **Visualização dos Resultados**:
   - Gráficos de boxplot e linha para análise dos erros (MAE) por fold.

## Resultados

- **Melhor Modelo**: **Lasso Regression**
  - **Média do MAE**: 9.7371
  - **Desvio Padrão do MAE**: 2.3085
  - **Hiperparâmetro mais frequente**: `alpha = 0.01`

- **Conclusões**:
  - O modelo Lasso Regression apresentou o melhor desempenho geral, com menor erro médio e maior consistência entre os folds.
  - A presença de outliers em alguns folds indica que o modelo teve dificuldades em subconjuntos específicos dos dados.

## Requisitos

- Python 3.7 ou superior
- Bibliotecas utilizadas:
  - `pandas`
  - `numpy`
  - `seaborn`
  - `matplotlib`
  - `scikit-learn`

## Como Executar

1. Certifique-se de que o arquivo `Dados_Peso_Curso_IA.xlsx` está no mesmo diretório do notebook.
2. Abra o arquivo `regrecao_multivariada.ipynb` em um ambiente como Jupyter Notebook ou JupyterLab.
3. Execute as células sequencialmente para reproduzir os resultados.

## Autor

Este projeto foi desenvolvido por Marcos Vinicius da Silva como parte de um estudo sobre regressão multivariada.