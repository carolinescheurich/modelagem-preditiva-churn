# 🏋️‍♀️ Análise de Churn na Academia Model Fitness

## Contexto do Projeto
Este projeto realiza uma Análise Exploratória de Dados (EDA) e*modelagem preditiva de churn para a academia Model Fitness nos Estados Unidos.  

O objetivo é identificar padrões de comportamento que levam à saída de clientes (churn) e propor estratégias direcionadas para aumentar a retenção e o engajamento.

## 🎯 Objetivos da Análise
1. Explorar o perfil e o comportamento dos clientes da academia.  
2. Identificar os principais fatores relacionados à rotatividade.  
3. Construir modelos preditivos de churn e avaliar sua performance.  
4. Segmentar os clientes em clusters para propor estratégias personalizadas de retenção.  

## 📂 Estrutura dos Dados
O dataset contém **4.000 clientes** e **14 variáveis**, com informações como:

| Variável | Descrição |
|--------|----------|
| `Churn` | Indicador de saída do cliente |
| `gender` | Gênero |
| `Near_Location` | Proximidade da academia |
| `Partner` | Funcionário de empresa parceira |
| `Promo_friends` | Inscrição por indicação |
| `Contract_period` | Duração do contrato |
| `Age`, `Lifetime` | Perfil e tempo de permanência |
| `Avg_class_frequency_total` | Frequência geral |
| `Avg_additional_charges_total` | Gastos extras |

O objetivo é entender como essas variáveis influenciam a decisão de abandonar a academia.

## ⚙️ Metodologia

### 1. **Preparação dos Dados**
- Leitura e inspeção do dataset  
- Tratamento de valores ausentes e padronização  
- Criação de variáveis auxiliares para a análise  

### 2. **Análise Exploratória (EDA)**
- Distribuição do churn por características sociodemográficas  
- Análise de frequência de uso e gastos  
- Comparações entre grupos fiéis vs. em risco  

### 3. **Modelagem Preditiva**
Modelos aplicados:
- Regressão Logística  
- Random Forest  

**Métricas avaliadas:**
- Acurácia  
- Precisão  
- Recall  
- AUC-ROC  

O **Random Forest** apresentou o melhor desempenho geral, sendo mais eficiente para identificar clientes em risco de churn.

### 4. **Agrupamento (Clustering)**
Técnicas aplicadas:
- K-Means  
- Agrupamento hierárquico  

Foram identificados **5 clusters** com perfis distintos de risco e engajamento.

## 📈 Principais Insights e Conclusões

- **Clientes com contratos curtos e baixa frequência** apresentam o maior risco de churn.  
- Proximidade da academia, indicação de amigos e programas parceiros contribuem para **maior retenção**.  
- **Alta permanência e frequência** são fatores decisivos para manter o cliente engajado.  
- A segmentação revelou grupos que demandam **estratégias diferentes** de relacionamento:

| Cluster | Perfil | Churn | Estratégia |
|--------|--------|-------|------------|
| 2 | Novos, baixa frequência e contratos curtos | **58,6%** | Engajamento imediato |
| 3 | Gastos extras mas pouco ativos | **28%** | Incentivo ao uso da academia |
| 1 e 4 | Engajados e estáveis | **3,6% / 8,2%** | Fidelização |
| 0 | Clientes muito fiéis | **0%** | Recompensas e reconhecimento |

📌 **Principais direcionamentos de negócio:**
- Estimular contratos longos desde o início  
- Programas sociais e eventos para aumentar a frequência  
- Personalização de ofertas com base nos clusters identificados  

## 🛠️ Tecnologias e Bibliotecas Utilizadas
O projeto foi desenvolvido em Python, utilizando:

- **Pandas**, **NumPy** → manipulação e análise de dados  
- **Matplotlib** e **Seaborn** → visualizações  
- **Scikit-learn** → modelagem preditiva e clustering  
- **SciPy** → análise estatística  
- **Jupyter Notebook** → execução e documentação da análise  
