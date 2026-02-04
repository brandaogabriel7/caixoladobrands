---
{"dg-publish":true,"dg-path":"Tecnologia/Engenharia de Dados/Data Engineer Learning Path - Gabriel.md","permalink":"/tecnologia/engenharia-de-dados/data-engineer-learning-path-gabriel/","updated":"2026-01-23T14:24:21.334-03:00"}
---


> [!info] Construído com ajuda de IA
> Este roadmap foi criado com auxílio de inteligência artificial (Claude). O conteúdo foi curado e adaptado por mim para meu contexto, mas a IA ajudou a estruturar e detalhar o plano.

# Data Engineer Learning Path
*Tailored for experienced software developers*

---

## Phase 1: Foundations (2-3 weeks)
*Leverage your existing skills, fill gaps*

### SQL Mastery
- [ ] Advanced SQL: window functions, CTEs, recursive queries
- [ ] Query optimization & execution plans
- [ ] Practice: [LeetCode SQL](https://leetcode.com/problemset/database/) or [DataLemur](https://datalemur.com/)

### Data Modeling
- [ ] Dimensional modeling (star schema, snowflake)
- [ ] Data vault basics
- [ ] Slowly changing dimensions (SCDs)
- **Resource:** Kimball's *The Data Warehouse Toolkit* (skim chapters 1-4)

---

## Phase 2: Core Data Engineering (4-6 weeks)
*The meat of the transition*

### Python for Data
- [ ] Pandas & NumPy deep dive
- [ ] PySpark fundamentals
- [ ] Data validation with Pydantic/Great Expectations

### ETL/ELT Pipelines
- [ ] Build batch pipelines from scratch
- [ ] Understand ELT vs ETL trade-offs
- [ ] Incremental loading patterns

### Orchestration
- [ ] **Apache Airflow** — DAGs, operators, sensors
- [ ] Alternatives awareness: Prefect, Dagster
- **Project:** Build a multi-step pipeline with dependencies & error handling

---

## Phase 3: Big Data & Cloud (4-6 weeks)
*Scale up your skills*

### Apache Spark
- [ ] Spark architecture & RDDs vs DataFrames
- [ ] Spark SQL & optimization
- [ ] Handling skewed data & partitioning
- **Resource:** [Spark: The Definitive Guide](https://www.oreilly.com/library/view/spark-the-definitive/9781491912201/)

### Cloud Data Platforms (pick one to start)
- [ ] **AWS:** S3, Glue, Redshift, Athena, EMR
- [ ] **GCP:** BigQuery, Dataflow, Cloud Storage
- [ ] **Azure:** Synapse, Data Factory, ADLS
- **Project:** Build a cloud-native data pipeline end-to-end

### Data Warehousing
- [ ] Modern data warehouse architecture
- [ ] **dbt (data build tool)** — transformations, testing, docs
- [ ] Snowflake or Databricks basics

---

## Phase 4: Streaming & Advanced (3-4 weeks)
*Differentiate yourself*

### Real-time Data
- [ ] Apache Kafka fundamentals
- [ ] Stream processing concepts
- [ ] Kafka + Spark Streaming or Flink basics

### Data Quality & Governance
- [ ] Data contracts
- [ ] Great Expectations or dbt tests
- [ ] Data cataloging concepts

### Infrastructure as Code
- [ ] Terraform for data infrastructure
- [ ] Docker for data tools
- **Your DevOps background is a huge asset here!**

---

## Phase 5: Portfolio & Job Prep (2-3 weeks)

### Capstone Project Ideas
1. **End-to-end pipeline:** Ingest API data → transform with dbt → visualize
2. **Real-time dashboard:** Kafka → Spark Streaming → live metrics
3. **Data platform:** Build a mini lakehouse with Delta Lake

### Interview Prep
- [ ] System design for data pipelines
- [ ] SQL coding challenges
- [ ] Behavioral questions around data projects
- **Resource:** [DataEngineer.io Interview Guide](https://www.dataengineer.io/)

---

## Recommended Learning Resources

| Resource | Type | Focus |
|----------|------|-------|
| [DataCamp Data Engineer Track](https://www.datacamp.com/tracks/data-engineer-with-python) | Course | Comprehensive |
| [Zach Wilson's Data Engineering Bootcamp](https://www.youtube.com/@zachary-wilson) | YouTube | Free, practical |
| [Fundamentals of Data Engineering](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/) | Book | Theory + practice |
| [Start Data Engineering](https://www.startdataengineering.com/) | Blog | Project tutorials |

---

## Timeline Summary

| Phase | Duration | Status |
|-------|----------|--------|
| Foundations | 2-3 weeks | ⬜ Not started |
| Core Data Engineering | 4-6 weeks | ⬜ Not started |
| Big Data & Cloud | 4-6 weeks | ⬜ Not started |
| Streaming & Advanced | 3-4 weeks | ⬜ Not started |
| Portfolio & Job Prep | 2-3 weeks | ⬜ Not started |

**Total: ~15-22 weeks** (adjustable based on your pace)

---

*Last updated: January 2026*