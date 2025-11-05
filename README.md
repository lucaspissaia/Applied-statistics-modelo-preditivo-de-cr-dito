# 📊 Applied Statistics - Modelo Preditivo de Credit Scoring

Este repositório contém o Projeto Integrado de **Estatística Aplicada** do **MBA em Data Science & AI da FIAP (10DTSR)**.

O objetivo foi desenvolver um modelo preditivo de **Credit Scoring** para a fintech *Quantum Finance*, utilizando técnicas estatísticas para analisar o perfil de clientes e prever o risco de inadimplência.

---

## 🔬 Metodologia e Análise Estatística

O projeto seguiu um pipeline estatístico completo para identificar os fatores mais relevantes na composição do score de crédito.

### 1. Análise Descritiva e Análise de Correlação
* Foi realizada uma análise descritiva para entender a distribuição, média e mediana de todas as variáveis (numéricas e categóricas).
* Uma **Matriz de Correlação** foi gerada para medir a relação linear entre as variáveis e a variável alvo (`score`).
* **Principais Insights:**
    * `vl_imovel` (Valor do Imóvel) e `vl_salario` (Valor do Salário) mostraram a correlação positiva mais forte com o `score`.
    * `tempo_servico` e `qtd_cartoes` também apresentaram correlação positiva moderada.

### 2. Tratamento de Multicolinearidade
* Durante a análise de correlação, identificamos alta multicolinearidade (correlações fortes entre variáveis de *entrada*), o que pode distorcer os coeficientes do modelo.
* **Ações:**
    * `casa_propria` e `vl_imovel` (0.75): Removemos `casa_propria`.
    * `idade` e `tempo_servico` (0.77): Removemos `idade`.

### 3. Modelagem com Regressão Linear
* A **Regressão Linear** foi a técnica estatística escolhida para criar o modelo preditivo, por sua interpretabilidade e adequação ao problema.

### 4. Otimização e Avaliação do Modelo
* **Modelo Inicial:** Acurácia de **58%**.
* **Otimização:** Após uma análise mais profunda dos dados, percebeu-se que valores *zero* em variáveis importantes (como `vl_imovel`) estavam prejudicando o modelo. Ao aplicar um tratamento específico (peso) para esses valores, o modelo foi re-treinado.
* **Modelo Final:** Acurácia de **63.8%** e um Erro Médio de 80.68.

---

## 💡 Conclusões e Recomendações

* O estudo estatístico provou que variáveis como valor do imóvel, salário e tempo de serviço são preditores significativos do score de crédito.
* O tratamento de multicolinearidade e a análise detalhada da distribuição dos dados (como valores zero) foram cruciais para melhorar a performance do modelo.
* Para trabalhos futuros, recomenda-se a clusterização de variáveis (como `tempo_servico`) e a inclusão de dados mais diretos de inadimplência (ex: tempo de atraso de pagamento).

## 🛠️ Stack Tecnológica

* **Linguagem:** Python
* **Técnicas:** Estatística Descritiva, Análise de Correlação (Multicolinearidade), Regressão Linear.
* **Ferramentas:** Pandas, NumPy, Scikit-learn (?).

## 👥 Autores

* Erika Koyanagui
* Lucas Huber Pissaia
* Matheus Raeski
