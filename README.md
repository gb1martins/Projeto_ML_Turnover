# 📊 Projeto de Machine Learning - Predição de Rotatividade de Funcionários (HR Analytics)

Este projeto tem como objetivo prever a rotatividade de funcionários (Attrition) em uma empresa, utilizando algoritmos de Machine Learning aplicados sobre um conjunto de dados inspirado no IBM HR Analytics.


---

## 📌 Problema

A empresa enfrenta uma taxa de rotatividade de aproximadamente **16%**, gerando um impacto financeiro estimado em **R$ 45 milhões**. Antecipar a saída de funcionários tornou-se uma prioridade estratégica.

---

## 🎯 Objetivo

Construir um modelo preditivo capaz de identificar colaboradores com maior probabilidade de saída com base em variáveis demográficas, comportamentais e organizacionais, auxiliando o RH a tomar decisões preventivas.

---

## 🛠️ Metodologia

O pipeline adotado seguiu as etapas clássicas de Data Science:

- **Análise exploratória e estatística (EDA)**
- **Feature engineering avançada** (ex: RatioStayWithManager, BurnoutRisk, TenureRatio)
- **Criação de variáveis polinomiais e embeddings**
- **Tratamento de desbalanceamento** com `class_weight='balanced'`, threshold ajustado e uso de métricas robustas
- **Treinamento com modelos:**
  - Logistic Regression
  - Random Forest
  - LightGBM
  - CatBoost
  - Voting Ensemble (modelo final)
- **Validação cruzada e ajuste de hiperparâmetros (GridSearchCV)**

---

## 📈 Principais Resultados

- O modelo **Voting Ensemble** obteve o melhor desempenho com:
  - **F1-score = 0.34**
  - **Recall = 0.90** para a classe "Saiu"

- As principais variáveis preditoras foram:
  - `JobSatisfaction`
  - `OverTimeFlag`
  - `YearsAtCompany`
  - `EnvironmentSatisfaction`

---

## 🧠 Principais Insights

- Funcionários **jovens, solteiros e insatisfeitos**, que fazem **horas extras**, possuem maior risco de saída.
- Funcionários com **baixa satisfação geral** e **pouco tempo de empresa** também apresentam maior propensão a sair.
- A variável `BurnoutRisk` foi útil para identificar grupos vulneráveis.

---

## 🚀 Deployment e Próximos Passos

- **Modelo final exportado como `.pkl`**
- **API com Flask/FastAPI** (proposta para consumo por sistemas internos)
- **Monitoramento de performance e retraining** periódico sugeridos
- **Melhorias futuras:**
  - Uso de dados externos (ex: clima organizacional)
  - Integração com dashboards (Power BI, Tableau)
  - Modelos segmentados por departamento

---

## 📚 Conclusão

O projeto consolidou o aprendizado em ciência de dados com aplicação prática em um problema real. A solução proposta pode apoiar o RH na retenção de talentos, com impacto direto na redução de custos e melhora da performance organizacional.

---

## 📁 Estrutura do Projeto
Arquivo "turnover_model.ipynb"

