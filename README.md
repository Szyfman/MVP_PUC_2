# **Análise de Atrasos em Voos nos EUA**

Este projeto tem como objetivo construir um pipeline de dados na nuvem, utilizando a plataforma **Databricks Community Edition**, para investigar padrões, causas e impactos dos atrasos de voos nos Estados Unidos. Através de uma análise exploratória com uso de ferramentas como **Pandas**, **Seaborn** e **PySpark**, buscamos responder perguntas de negócio relevantes, apoiando a tomada de decisão com base em dados reais.

---

## **Estrutura do Projeto**

A estrutura do projeto está organizada da seguinte maneira:

- **MVP_2_PUC_Daniel_Szyfman.ipynb**: Contém o notebook principal com todo o fluxo do projeto, incluindo coleta, tratamento, modelagem e análise exploratória.
- **requirements.txt**: Lista todas as dependências necessárias para executar o projeto.
- Datasets utilizados para análises estão na **DBFS**.

---

## **Como Executar**

### **1. Clone o repositório**
```bash
git clone https://github.com/Szyfman/MVP_PUC_2.git
cd MVP_PUC_2
```

### **2. Crie um ambiente virtual Python e ative-o**
```bash
python -m venv venv
venv\Scripts\activate  # No Windows
```

### **3. Instale as dependências**
```bash
pip install -r requirements.txt
```

### **4. Abra o notebook localmente**
- **Localmente**: Abra o arquivo com o Jupyter Notebook:
  ```bash
  jupyter notebook MVP_2_PUC_Daniel_Szyfman.ipynb
  ```

### **Para Acesso ao Dataset**
- Acesse: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/4265032473881901/94608601343067/1282203946557660/latest.html

---

## **Resultados do Projeto**

A análise exploratória permitiu identificar padrões e fornecer respostas significativas às perguntas de negócio. A seguir, estão os resultados obtidos para cada uma das questões abordadas:

### 1. **Quais companhias aéreas apresentam maior proporção de voos com atraso?**

Após calcular a **proporção de voos com atraso** por companhia aérea, observamos que algumas companhias têm uma taxa significativamente maior de atrasos. As companhias **NK** (Norwegian Air) e **F9** (Spirit Airlines) têm os maiores percentuais de voos com atraso, indicando um desempenho abaixo da média em termos de pontualidade. Por outro lado, **HA** (Hawaiian Airlines) e **AS** (Alaska Airlines) apresentaram os menores percentuais de atrasos.

### 2. **Qual é o percentual de voos cancelados por companhia aérea?**

Ao calcular o percentual de voos cancelados, a **MQ** (Envoy Air) se destacou com o maior percentual de voos cancelados, atingindo **5.10%** dos seus voos. Em contraste, **HA** (Hawaiian Airlines) e **AS** (Alaska Airlines) mostraram os menores percentuais de cancelamento, com valores bem abaixo da média, indicando maior confiabilidade operacional.

### 3. **A distância ou o tempo de voo influenciam o atraso na chegada?**

A análise de correlação entre **distância** e **tempo de voo** com os **atrasos na chegada** revelou uma correlação muito fraca e negativa. Isso sugere que nem a distância nem o tempo de voo têm impacto significativo nos atrasos na chegada. Outros fatores operacionais, como condições climáticas ou problemas logísticos, provavelmente têm maior influência.

### 4. **Quais aeroportos concentram mais atrasos na decolagem e/ou chegada?**

Analisando os **atrasos nos aeroportos de origem** e **nos aeroportos de destino**, identificamos que os aeroportos **OAK**, **MSY** e **SNA** concentram os maiores números de atrasos, tanto na decolagem quanto na chegada. Esses aeroportos podem ser pontos críticos em termos de congestionamento ou problemas operacionais que afetam a pontualidade.

---

Esses resultados fornecem uma visão clara sobre os principais fatores que afetam os atrasos em voos, como a performance de companhias aéreas, as taxas de cancelamento e a eficiência dos aeroportos. A análise pode ser útil para otimizar processos operacionais e melhorar a experiência dos passageiros.

---

## **Aprendizados e Próximos Passos**

### **Aprendizados**

Durante a execução deste projeto, aprendemos diversas lições importantes, como:

- **Coleta e Manipulação de Dados**: A importância de coletar dados de diferentes fontes (Kaggle, por exemplo) e como transformá-los para análise, além de realizar a integração correta de tabelas de diferentes fontes de dados (como aeroportos e companhias aéreas).
  
- **ETL (Extração, Transformação e Carga)**: A construção de um pipeline de ETL eficiente, com foco em transformar dados brutos em informações relevantes para a análise de atrasos de voos, foi fundamental para a criação de um Data Lake estruturado e otimizado.

- **Modelagem de Dados e Análises**: A realização da modelagem de dados no formato de Data Lake (flat) e a análise exploratória com o uso de **PySpark**, **Pandas**, **Matplotlib** e **Seaborn** nos permitiu gerar insights valiosos sobre as companhias aéreas, aeroportos e as causas dos atrasos.

- **Visualizações**: A criação de visualizações simples, mas informativas, facilitou a compreensão dos resultados, ajudando a identificar padrões e insights sobre o desempenho das companhias aéreas e dos aeroportos.

### **Próximos Passos**

Apesar de termos atingido os principais objetivos do projeto, há algumas áreas que podem ser exploradas em futuras versões:

1. **Otimização do Pipeline de ETL**: Refatorar o código para aumentar a eficiência, evitando operações desnecessárias de leitura e gravação de dados, otimizando as transformações.
  
2. **Expansão da Análise**: Incluir mais variáveis, como condições climáticas, horários de pico ou eventos específicos, para aprofundar as conclusões sobre os fatores que mais influenciam os atrasos.

3. **Previsão de Atrasos**: Explorar modelos preditivos, como **modelos de machine learning**, para prever atrasos com base em dados históricos, oferecendo uma análise mais proativa.

4. **Integração com Ferramentas de BI**: Integrar os resultados com ferramentas como **Power BI** ou **Tableau** para visualizações interativas e dashboards mais detalhados, permitindo uma análise em tempo real.

5. **Melhorias no Catálogo de Dados**: Expandir o catálogo de dados com mais detalhes sobre a qualidade dos dados, dados ausentes e insights sobre as variáveis que mais afetam a performance dos voos.

Com esses próximos passos, podemos avançar ainda mais nas análises e transformar este projeto em uma ferramenta ainda mais poderosa para analisar e otimizar a performance da aviação.

---
