# DMS - Database Migration Service

Faz a migração da bancos de dados para a AWS de forma segura e rápida.

O database de origem permance disponível durante a migração.

Suporta:

* **Migrações Homogêneas:** mesma engina (ex.: Oracle -> Oracle);
* **Migrações Heterogêneas:** engines diferentes (ex.: Micrososft SQL Server -> Aurora).

Faz replicação contínua com CDC (Change Data Capture).

Você deve criar instâncias EC2 para executar as tasks de replicação.

![](./imagens/dms.png)

**Sources:**

* On-premises e databases em instâncias EC2: Oracle, MS SQL Server, MySQL, MariaDB, PostgreSQL, MongoDB, SAP, DB2;
* Azure: Azure SQL Database;
* Amazon RDS: todos, incluindo Aurora;
* Amazon S3;
* DocumentDB.

**Targets:**

* On-premises e databases em instâncias EC2: Oracle, MS SQL Server, MySQL, PostgreSQL, SAP;
* Amazon RDS;
* Redshift, DynamoDB, S3;
* OpenSearch Service;
* Kinesis Data Streams;
* Apache Kafka;
* DocumentDB e Amazon Neptune;
* Redis e Babelfish.

---

## AWS Schema Conversion Tool (SCT)

Converte o seu schema de database de uma engine para outra.

* Exemplo OLTP: SQL Server ou Oracle para MySQL, PostgreSQL, Aurora;
* Exemplo OLAP: Teradata ou Oracle para Amazon Redshift.

Utilize instâncias `compute-intensive` para otimizar as conversões de dados.

![](./imagens/sct.png)

Você só precisa utilizar SCT em migrações heterogêneas.

---

## Continuous Replication

![](./imagens/continuous.png)

---

## Multi-AZ Deployment

![](./imagens/multiAZ.png)