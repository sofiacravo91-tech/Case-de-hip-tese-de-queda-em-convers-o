# 📊 Probabilidade aplicada a conversão — Case de Business Data Analytics

Este repositório contém um **estudo de caso completo e realista** de **probabilidade aplicada a negócio**, simulando decisões que um **Business/Data Analyst** enfrenta em empresas **SaaS B2B**.

O objetivo não é apenas calcular números, mas **traduzir estatística em decisão de negócio**.

---

## 🧠 Contexto de Negócio

Empresa SaaS B2B que vende um **plano mensal** para bares e restaurantes.

### Funil de conversão:

1. **Lead** (cadastro no site)
2. **Trial** (teste gratuito)
3. **Cliente pago**

### Dados históricos esperados:

* Leads no mês: **2.000**
* Lead → Trial: **40%**
* Trial → Pago: **25%**
* Conversão total esperada: **10%**

👉 Esperado: **200 clientes pagos**

### Resultado observado:

* Trials iniciados: **760**
* Clientes pagos: **170**
* Conversão real: **8,5%**

Surge a pergunta central do negócio:

> **Isso é apenas variação natural ou houve uma mudança real no processo?**

---

## 🎯 Perguntas de Negócio Respondidas

Este case responde perguntas comuns em contextos reais:

* A queda observada pode ser explicada por aleatoriedade?
* Qual a probabilidade de observar um resultado tão baixo?
* Quando vale a pena investigar ou pausar uma campanha?
* Como justificar decisões com base em dados para stakeholders?

---

## 📐 Abordagem Estatística

### 1. Modelagem

* Cada lead é tratado como um **evento Bernoulli** (converte ou não)
* Número de clientes pagos modelado como:

> **Distribuição Binomial**
> (X \sim Binomial(n=2000, p=0.10))

---

### 2. Métricas principais

* Média esperada:
  (\mu = np = 200)

* Desvio padrão:
  (\sigma = \sqrt{np(1-p)} \approx 13,4)

* Intervalo esperado (~95%):
  **[173, 227] clientes pagos**

Resultado observado (**170**) está **abaixo do intervalo esperado**.

---

### 3. Probabilidade do ocorrido

Calculada via **aproximação normal da binomial**:

* Z-score ≈ **-2,24**
* Probabilidade acumulada:

> **P(X ≤ 170) ≈ 1,25%**

Interpretação:

> Se a taxa real fosse 10%, esse resultado ocorreria cerca de **1 vez a cada 80 meses**.

---

## 🧪 Teste de Hipótese

### Hipóteses formuladas:

* **H₀ (nula):** taxa de conversão permanece em **10%**
* **H₁ (alternativa):** taxa de conversão é **menor que 10%**

Como o p-value ≈ **1,25% (< 5%)**, há **evidência estatística contra H₀**.

⚠️ Importante: isso **não prova causalidade**, apenas indica que o resultado é improvável sob o cenário histórico.

---

## 🧠 Conclusão de Negócio

* A queda observada **não parece ser apenas ruído estatístico**
* Justifica investigação imediata
* Próximos passos recomendados:

  * Segmentação de leads
  * Comparação antes vs depois da campanha
  * Análise de qualidade e perfil dos clientes

---

## 🚀 Próximas Extensões do Case

* Teste por segmento (bares pequenos vs grandes)
* Simulação de cenários alternativos
* Implementação em Google Sheets
* Versão em Python / SQL

---

## 🧩 O que este projeto demonstra

* Probabilidade aplicada a negócio
* Pensamento analítico estruturado
* Tradução de dados em decisão
* Comunicação clara com stakeholders

---

## 👤 Autora

**Sofia**
Business / Data Analytics • SaaS • Tecnologia

---

📌 *Este repositório foi criado com foco em aprendizado prático e preparação para entrevistas técnicas e de negócio.*
