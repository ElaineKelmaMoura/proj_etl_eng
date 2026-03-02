# Data Engineering Pipeline — PostgreSQL → Kafka → Spark → AWS S3 (Bronze / Silver / Gold)

## 📌 Objetivo

Pipeline completo de Engenharia de Dados com ingestão via PostgreSQL,
publicação em Kafka e processamento distribuído com Spark,
armazenando dados em um Data Lake no AWS S3 seguindo o padrão Bronze, Silver e Gold.Implementar um pipeline de dados distribuído utilizando Docker, Kafka e Spark,
processando dados financeiros e armazenando em camadas no Amazon S3.

---

## 🏗  Arquitetura

### Fluxo de Dados

PostgreSQL → Kafka → Spark → S3 (Bronze)
S3 Bronze → Spark → S3 Silver
S3 Silver → Spark → S3 Gold


            +-------------+
            | PostgreSQL  |
            +-------------+
                    |
                    v
            +-------------+
            |   Kafka     |
            +-------------+
                    |
                    v
            +-----------------+
            | Kafka Connect   |
            +-----------------+
                    |
                    v
            +-------------+
            |  AWS S3     |
            |  (Bronze)   |
            +-------------+
                    |
                    v
            +-------------+
            |  Apache     |
            |   Spark     |
            +-------------+

---

## ⚙️ Stack Utilizada

- Docker & Docker Compose
- PostgreSQL
- Apache Kafka
- Apache Spark (PySpark 3.5)
- AWS S3 (s3a)
- Parquet

---

## 📂 Estrutura do Projeto

notebooks/
 ├── ingestão_postgres_kafka.ipynb
 └── transformação_silver_gold.ipynb

---

##🔄 Camadas

Bronze

°Dados brutos armazenados no S3.

Silver

°Remoção de duplicidades
°Conversão de timestamps
°Tratamento de nulos
°Particionamento

Gold

°Agregações por Tipo
°Métricas de média e contagem
°Dados prontos para consumo analítico

---

## 📈 Resultados Obtidos

- Cluster Spark distribuído funcionando
- Kafka Connect enviando dados para S3
- Estrutura Bronze armazenando dados em JSON
- Ambiente totalmente containerizado

---
