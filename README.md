# Projeto ETL - Engenharia de Dados

## 📌 Objetivo

Implementar um pipeline de dados distribuído utilizando Docker, Kafka e Spark,
processando dados financeiros e armazenando em camadas no Amazon S3.

---

## 🏗  Arquitetura Atual (Infraestrutura + Bronze)

Fluxo de dados:

PostgreSQL → Kafka → Kafka Connect → Amazon S3 (Bronze) → Apache Spark


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
- Kafka Connect
- AWS S3
- Apache Spark (Master + Worker)
- Jupyter Lab
- Python (PySpark)

---

## 📂 Estrutura do Projeto


---

## 📈 Resultados Obtidos

- Cluster Spark distribuído funcionando
- Kafka Connect enviando dados para S3
- Estrutura Bronze armazenando dados em JSON
- Ambiente totalmente containerizado

---
