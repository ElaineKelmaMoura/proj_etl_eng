# Projeto ETL - Engenharia de Dados

## 📌 Objetivo

Implementar um pipeline de dados distribuído utilizando Docker, Kafka e Spark,
processando dados financeiros e armazenando em camadas no Amazon S3.

---

## 🏗  Arquitetura Atual (v1)

Fluxo de dados:

PostgreSQL → Kafka → Kafka Connect → Amazon S3 (Bronze) → Apache Spark

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


