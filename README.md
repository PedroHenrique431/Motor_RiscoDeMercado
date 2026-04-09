# 📊 Motor de Risco para Carteiras de Ações

Este projeto consiste no desenvolvimento de um motor de risco para simulação e análise de carteiras de ações, utilizando Python e dados reais de mercado.

A proposta é reproduzir, em ambiente controlado, a dinâmica de um portfólio semelhante ao de uma asset, desde a construção da carteira até a mensuração de risco e análise de cenários.

---

## 🚀 Principais funcionalidades

* Geração de carteiras fictícias baseadas na carteira do Ibovespa
* Definição de pesos e construção de benchmark comparável
* Coleta de dados históricos de preços via API (Brapi)
* Estimativa de risco com VaR paramétrico (Delta-Normal)
* Simulação de cenários de stress:
  * Descorrelacionado (quantis históricos)
  * Correlacionado (choques reais de mercado)
* Consolidação dos resultados em DataFrame final

---

## 🧠 Metodologia

### VaR (Value at Risk)

O VaR é calculado utilizando o modelo paramétrico (Delta-Normal), considerando a matriz de covariância entre os ativos:

* Captura volatilidade individual
* Incorpora correlação entre ativos
* Expressa o risco como percentual do PL

---

### Stress Testing

#### 🔹 Stress Descorrelacionado

* Baseado nos quantis 5% e 95% da distribuição histórica de retornos
* Avalia cenários extremos por ativo de forma independente

#### 🔹 Stress Correlacionado

* Utiliza choques históricos reais
* Preserva a estrutura de correlação entre os ativos
* Simula eventos de mercado mais realistas

---

## 📈 Estrutura do Projeto

O fluxo do projeto segue as seguintes etapas:

1. Seleção de ativos
2. Coleta de dados históricos
3. Cálculo de retornos e volatilidade
4. Construção da carteira e do benchmark
5. Cálculo de métricas de risco
6. Simulação de cenários de stress
7. Consolidação dos resultados

---

## 📦 Tecnologias utilizadas

* Python
* Pandas
* NumPy
* Brapi (API de dados de mercado)

---

## ⚠️ Observações

* Os dados utilizados são reais, porém a carteira é simulada
* O histórico utilizado é limitado (3 meses) devido à API gratuita
* O modelo tem caráter educacional, mas segue conceitos utilizados no mercado

---

## 🤝 Contato

Fico à disposição para trocas sobre modelagem de risco, portfólios e aplicações práticas em finanças.

---

