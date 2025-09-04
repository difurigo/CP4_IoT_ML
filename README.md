## Realizado por: Diego Furigo do Nascimento - RM: 558755

# 📊 Machine Learning e Análise de Dados — Consumo de Energia

Este projeto apresenta um estudo detalhado do dataset público [Individual Household Electric Power Consumption](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption), que contém medições de consumo elétrico em uma residência entre 2006 e 2010.  
Foram realizadas análises exploratórias, estatísticas, modelagem preditiva e técnicas de machine learning para identificar padrões e compreender o comportamento do consumo de energia.

---

## ⚙️ Tecnologias utilizadas
- **Pandas & NumPy** → manipulação e tratamento de dados  
- **Matplotlib & Seaborn** → visualização de gráficos e padrões  
- **Scikit-learn** → normalização, regressão, clustering e redução de dimensionalidade  
- **Statsmodels** → análise de séries temporais  

---

## 📂 Etapas do Projeto

### 1. Importação e exploração inicial
- Leitura do dataset em formato `.txt` e criação de DataFrame.
- Inspeção de dimensões, colunas, tipos de dados e estatísticas descritivas.
- Substituição de valores inválidos (`?`) por `NaN` e tratamento de dados faltantes.

### 2. Entendimento das variáveis
- Diferenciação entre **Global_active_power** (potência ativa que gera trabalho útil, como calor e movimento) e **Global_reactive_power** (potência reativa associada a campos elétricos e magnéticos, necessária para funcionamento de motores e transformadores).  

### 3. Criação e manipulação de variáveis
- Conversão da coluna `Date` para tipo `datetime`.  
- Extração de informações como **dia da semana**, **mês** e **ano**.  
- Criação da variável `Total_Sub_metering`, que soma `Sub_metering_1`, `Sub_metering_2` e `Sub_metering_3`.  

### 4. Análise Exploratória de Dados (EDA)
- Visualização das primeiras linhas do dataset.  
- Análise de consumo médio diário e mensal.  
- Comparação entre consumo em **dias de semana** e **finais de semana**.  
- Identificação do **dia de maior consumo** da série histórica.  
- Cálculo de correlações entre variáveis como `Global_active_power`, `Voltage` e `Global_intensity`.  

### 5. Visualizações
- **Gráfico de linha** mostrando a variação da potência ativa em um dia específico, destacando picos e mínimos.  
- **Histograma de distribuição da tensão (Voltage)**, permitindo observar sua dispersão.  
- Gráficos de consumo médio mensal e variações ao longo do tempo.  

### 6. Modelagem com Machine Learning
- **Pré-processamento**: normalização dos dados com `MinMaxScaler` e divisão em treino e teste.  
- **Regressão Linear** para previsão de variáveis contínuas.  
- **Regressão Polinomial** com `PolynomialFeatures` e `Pipeline`.  
- **K-Means Clustering** para agrupamento de padrões de consumo, avaliado com **Silhouette Score**.  
- **PCA (Análise de Componentes Principais)** para redução da dimensionalidade e melhor visualização dos clusters.  

### 7. Análise de Séries Temporais
- **Decomposição sazonal** do consumo para avaliar tendência, sazonalidade e ruído.  
- Uso da **Função de Autocorrelação (ACF)** para entender dependências temporais no consumo.  

### 8. Avaliação dos Modelos
- **Métricas de Regressão**:  
  - Erro Quadrático Médio (MSE)  
  - Coeficiente de Determinação (R²)  
- Comparação entre modelos lineares e polinomiais.  
- Visualização dos clusters obtidos com K-Means.  

---

## 🚀 Resultados alcançados
- Identificação de **padrões sazonais e diários** no consumo de energia.  
- Descoberta de **diferenças significativas** no consumo entre dias de semana e finais de semana.  
- Construção de modelos preditivos capazes de estimar o consumo com boa acurácia.  
- Agrupamento de perfis de consumo em clusters distintos via K-Means.  
- Redução de dimensionalidade com PCA para melhor interpretação dos dados.  

---

## 📌 Conclusão
Este projeto integra conceitos de **análise de dados, estatística, machine learning e séries temporais** para explorar e modelar um conjunto real de consumo elétrico.  
Ele pode ser expandido para aplicações práticas como previsão de demanda energética, eficiência no uso de recursos e identificação de padrões de comportamento em domicílios.

---
