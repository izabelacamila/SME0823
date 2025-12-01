# Atividade: Modelos de Regressão Generalizados (GLM)

Este repositório contém a resolução da atividade prática sobre Modelos de Regressão para dados de contagem, desenvolvida como parte da disciplina de Modelos de Regressão e Aprendizado Supervisionado II.

<details>
<summary><h1 align="center"> Informações da Disciplina </h1></summary>

**Instituição:** ICMC - USP (Universidade de São Paulo)

**Curso:** SME0823 - Modelos de Regressão e Aprendizado Supervisionado II (2025)

**Docente:** Profa. Dra. Cibele Russo

**Aluna:** Izabela Camila Souza Silva

</details>

<details>
<summary><h1 align="center"> Objetivo do Estudo </h1></summary>

O objetivo deste trabalho foi analisar fatores associados ao número de espirros diários (*nsneeze*) em pacientes com rinite alérgica. Através de técnicas de modelagem estatística, investigou-se o impacto de variáveis comportamentais e ambientais na sintomatologia dos pacientes.

</details>

<details>
<summary><h1 align="center"> Sobre os Dados </h1></summary>

O dataset utilizado contém informações clínicas e demográficas de 1200 pacientes:

* **nsneeze**: Número de espirros (Variável Resposta - Contagem).
* **pollen**: Concentração de pólen no ar.
* **alcohol**: Consumo de álcool (0=Não, 1=Sim).
* **antihist**: Uso de anti-histamínico (0=Não, 1=Sim).
* **smoker**: Tabagismo (0=Não, 1=Sim).
* **age**: Idade do paciente.

</details>

<details>
<summary><h1 align="center"> Metodologia Aplicada </h1></summary>

A análise foi conduzida em Python, seguindo as seguintes etapas:

1. **Análise Exploratória de Dados (EDA):** Visualização de distribuições, boxplots e correlações (Spearman).
2. **Ajuste de Modelo de Poisson:** Primeira abordagem para dados de contagem.
3. **Diagnóstico de Superdispersão:** Cálculo da estatística de dispersão de Pearson e Teste de Cameron & Trivedi (1990).
4. **Ajuste de Modelo Binomial Negativo:** Correção da superdispersão identificada.
5. **Comparação de Modelos:** Uso de métricas de ajuste (AIC, BIC, Deviance) e Teste da Razão de Verossimilhança (LRT).
6. **Validação Cruzada:** Divisão em treino (70%) e teste (30%) para avaliação de métricas preditivas (EQM e EAM).
7. **Predição e Efeitos Marginais:** Estimativa do impacto clínico das variáveis e previsão para perfis específicos de pacientes.

</details>

<details>
<summary><h1 align="center"> Principais Resultados </h1></summary>

* Detectou-se superdispersão excessiva no modelo de Poisson, tornando-o inadequado para inferência.
* O Modelo Binomial Negativo apresentou melhor ajuste estatístico (menor AIC e correção dos erros padrão).
* **Conclusões Clínicas:**
    * O uso de anti-histamínicos reduz significativamente a contagem de espirros.
    * Álcool e Tabagismo são fatores de risco que aumentam a frequência de espirros.
    * Existe uma relação positiva entre a concentração de pólen e os sintomas.

</details>

<details>
<summary><h1 align="center"> Tecnologias Utilizadas </h1></summary>

* **Linguagem:** Python 3
* **Bibliotecas:**
    * pandas & numpy (Manipulação de dados)
    * statsmodels (Modelagem estatística GLM e testes)
    * seaborn & matplotlib (Visualização de dados)
    * scikit-learn (Métricas e separação de dados)

</details>


---
*Desenvolvido por Izabela Camila Souza Silva - 2025*
