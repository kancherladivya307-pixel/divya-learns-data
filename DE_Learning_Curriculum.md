# Data Engineering Learning Curriculum

**Student:** Divya
**Goal:** Become a proficient Data Engineer, then learn MLOps, then learn to integrate Anthropic/Claude into data workflows
**Pace:** ~30 minutes per day, most days
**Estimated duration:** 14-20 months end to end
**Method:** One sub-step at a time, project-based, with deep understanding of the "why" before the "how"
**Documentation:** Everything tracked in a dedicated GitHub learning repo, eventually used as portfolio

---

## Guiding Principles

1. **Understand before you memorize.** If you can't explain the "why" in your own words, we haven't finished the topic.
2. **Consistency beats intensity.** 30 minutes every day beats 4 hours once a week.
3. **Type everything yourself.** Copy-pasting teaches your fingers nothing.
4. **Errors are the teacher.** When something breaks, that's where real learning happens.
5. **Document as you go.** Future-you will thank present-you.
6. **No dumb questions.** Ask "baby questions" any time.
7. **Depth over breadth.** It's better to know SQL deeply than to know ten tools shallowly.
8. **Build projects.** Every phase ends with a hands-on project that you push to GitHub.

---

## How Each Session Works

1. Start with a quick review of where we left off last time
2. Learn one concept with the "why" first, then the "what," then the "how"
3. Do a hands-on exercise
4. Debug any errors together
5. Document what you learned in your learning repo
6. Get a small homework for practice between sessions
7. Next session starts with reviewing the homework

---

# PHASE 0 — Environment & Documentation Setup

**Duration:** 1 week
**Why this phase exists:** Before any learning, you need a place to put what you learn. We're going to set up your "learning infrastructure" — the repo, the note-taking system, the habit. This takes one session and then pays off for the next 14 months.

## Topics

- **0.1** Create a dedicated GitHub repo (`de-learning-journey`) for this entire journey
- **0.2** Set up folder structure (phases, notes, exercises, projects)
- **0.3** Learn basic Markdown for taking notes
- **0.4** Set up your practice environment (laptop + existing EC2 as needed)
- **0.5** Establish a "daily learning log" template
- **0.6** Soft skills kickoff: how to keep a learning journal, how to rubber-duck debug, how to ask good questions

## Deliverable
A working GitHub repo with folder structure, a README explaining the journey, and your first daily log entry.

---

# PHASE 1 — Foundational Data Concepts (Theory)

**Duration:** 4-5 weeks
**Why this phase exists:** This is the conceptual bedrock of data engineering. Every tool you learn later will make sense because you understood these ideas first. Most people skip this and struggle forever. We're not going to skip it. **There is no coding in this phase** — just concepts, diagrams, and understanding.

## 1A — What is Data, Really?

- Data vs information vs knowledge
- Structured, semi-structured, unstructured data
- Data types (numeric, categorical, temporal, text, binary)
- Why data matters to a business

## 1B — Databases 101

- What is a database, why we need them
- **OLTP vs OLAP** — the single most important distinction in data engineering
- Relational databases vs NoSQL
- **ACID properties** (Atomicity, Consistency, Isolation, Durability)
- **BASE properties** (eventual consistency)
- Primary keys, foreign keys, indexes, constraints
- **Normalization** (1NF, 2NF, 3NF) and **denormalization** — when and why
- **Entity-Relationship Diagrams** (ER diagrams)

## 1C — Data Warehousing Fundamentals

- What is a data warehouse, why it's different from a database
- **Inmon vs Kimball** — the two schools of thought
- The modern data stack: operational → ingestion → storage → transformation → serving
- **Data Warehouse vs Data Lake vs Data Lakehouse**
- Staging, raw, curated, semantic layers
- **Slowly Changing Dimensions** (SCD Type 1, 2, 3, 6) — classic interview topic
- Fact tables and dimension tables
- **Star schema vs snowflake schema vs galaxy schema**
- **Grain of a fact table** — trips up 90% of juniors
- Surrogate keys vs natural keys

## 1D — Data Modeling

- Conceptual vs logical vs physical data models
- How to model a real business process (we'll do one together)
- **Dimensional modeling** step by step
- **Data Vault** modeling (newer approach, used in some enterprises)
- **One Big Table (OBT)** approach
- How to read someone else's data model

## 1E — ETL vs ELT

- What ETL stands for and how it evolved
- What ELT is and why it replaced ETL in the cloud era
- When to still use ETL
- **Batch vs streaming vs micro-batch**
- Push vs pull ingestion
- **Full load vs incremental load vs CDC** (Change Data Capture)
- **Idempotency** — why pipelines should be rerunnable
- Backfilling historical data

## 1F — Data Engineering Lifecycle

- The 6 stages (generation, storage, ingestion, transformation, serving, reverse ETL)
- The "undercurrents" (security, data management, DataOps, orchestration, software engineering)
- Where a data engineer sits in a company
- **Data Engineer vs Data Scientist vs Data Analyst vs Analytics Engineer**

## 1G — Data Quality & Governance

- What is data quality (accuracy, completeness, consistency, timeliness, validity, uniqueness)
- **Data lineage** — where did this number come from?
- Data contracts
- Metadata and data catalogs
- **GDPR, HIPAA, CCPA** — privacy basics every DE needs to know
- **PII** (Personally Identifiable Information) handling

## 1H — Cloud Fundamentals

- What is cloud computing
- **IaaS vs PaaS vs SaaS**
- The three big clouds (AWS, Azure, GCP) at a high level
- Regions, availability zones, edge locations
- On-premises vs cloud vs hybrid
- **Shared responsibility model**
- Why everyone moved to the cloud

## 1I — Networking Basics for Data Engineers

- IP addresses, ports, DNS basics
- HTTP vs HTTPS
- SSH deeper
- VPCs, subnets, security groups (AWS context)
- Public vs private endpoints
- Why you can't just "connect to a database" from anywhere

## 1J — Security & Credentials Basics

- Authentication vs authorization
- Passwords, keys, tokens, certificates
- IAM concepts (users, roles, policies)
- Secrets management basics
- Why we never put passwords in code

## 1K — Data Engineering Math

- Stats basics: mean, median, mode, standard deviation, percentiles
- Distributions (normal, skewed, long-tail)
- Probability fundamentals
- Why DEs need this (for data quality checks and MLOps later)

## 1L — Soft Skills for Data Engineers

- Writing clear documentation
- Stakeholder communication
- Estimating work honestly
- Reading requirements
- Working with analysts and data scientists

## Deliverable
A complete set of notes in your learning repo covering every concept above, with your own diagrams and examples. A "cheat sheet" document you can refer back to forever.

---

# PHASE 2 — Linux, Command Line & Git

**Duration:** 2-3 weeks
**Why this phase exists:** Every data engineer lives in a terminal every day forever. If you're not comfortable on the command line, you'll be slow and frustrated for your entire career. Git is equally non-negotiable — it's how all engineers share code.

## Topics

- Linux filesystem and navigation
- **Essential commands:** ls, cd, cp, mv, rm, cat, grep, find, head, tail, wc, sort, uniq, awk, sed basics
- File permissions and ownership (chmod, chown)
- **Pipes and redirects** (|, >, >>, <, 2>)
- Environment variables
- Processes and jobs (ps, kill, &, nohup)
- SSH and SCP deeper
- Writing your first bash scripts
- **Git fundamentals** (init, add, commit, log, diff, status)
- Branches, merges, pull requests
- .gitignore
- **Git workflows** (feature branch, GitFlow, trunk-based)
- Resolving merge conflicts

## Deliverable
A GitHub repo of bash scripts you wrote, plus a personal Linux/Git cheat sheet in your learning repo.

---

# PHASE 3 — SQL Mastery

**Duration:** 5-6 weeks
**Why this phase exists:** SQL is THE #1 skill for a data engineer. It's tested in every DE interview, used in every DE job, and every tool we learn later will use some form of SQL underneath. Going deep pays off forever.

## Topics

- SQL history and dialects (ANSI, Oracle, T-SQL, PostgreSQL, Snowflake, HiveQL, Spark SQL)
- Basic queries (SELECT, FROM, WHERE, ORDER BY, LIMIT)
- Filtering and operators
- Aggregations (GROUP BY, HAVING, COUNT, SUM, AVG, MIN, MAX)
- **All join types with diagrams** (INNER, LEFT, RIGHT, FULL OUTER, CROSS, SELF)
- Subqueries vs CTEs (Common Table Expressions)
- **Window functions** — the #1 interview topic (ROW_NUMBER, RANK, DENSE_RANK, LAG, LEAD, partitioning)
- Date/time functions
- String functions
- CASE statements
- UNION vs UNION ALL
- Set operations (INTERSECT, EXCEPT)
- DDL (CREATE, ALTER, DROP, TRUNCATE)
- DML (INSERT, UPDATE, DELETE, MERGE)
- Transactions (BEGIN, COMMIT, ROLLBACK)
- Indexes and query optimization basics
- **EXPLAIN plans**
- Writing clean, readable SQL
- SQL anti-patterns to avoid

## Practice Platforms
- LeetCode (Database section)
- StrataScratch
- DataLemur
- HackerRank SQL

## Deliverable
**Solved 100+ SQL problems**, documented in your learning repo with your solutions and the concepts each one taught you.

---

# PHASE 4 — Python for Data Engineering

**Duration:** 5-6 weeks
**Why this phase exists:** Python is mandatory for modern data engineering. It's the glue that ties all the tools together. You already have some exposure from the DEF project — now we build real depth.

## Topics

- Python syntax basics (variables, types, operators, control flow)
- Data structures (list, tuple, dict, set)
- Functions, arguments, return values
- **List and dict comprehensions**
- File I/O (text, CSV, JSON, XML, Parquet)
- Exception handling (try/except/finally)
- Modules and packages
- Virtual environments (venv, pip, requirements.txt)
- **Object-oriented programming** (classes, inheritance)
- Decorators and context managers
- Generators and iterators
- Type hints and docstrings
- **pandas** — DataFrames, filtering, joining, grouping, pivot
- **NumPy** basics
- Connecting to databases (oracledb, psycopg2, snowflake-connector-python, pyodbc)
- Working with APIs (requests, JSON parsing)
- **boto3** for AWS
- Logging, argparse, config files
- Writing testable code
- **pytest** basics
- Code formatting (black, flake8, pylint, mypy)

## Deliverable
A mini-DEF project written from scratch in Python — reads a CSV, transforms it, writes to a database. Clean, tested, documented.

---

# PHASE 5 — Your Company Stack

**Duration:** 8-10 weeks
**Why this phase exists:** This is what makes you valuable at your current job. Every hour spent here directly improves your day-to-day work.

## 5A — Oracle Database Deep Dive

- Oracle architecture (instances, databases, tablespaces, schemas)
- Oracle data types
- Oracle-specific SQL (DUAL, ROWNUM, ROWID, sequences, hints)
- **PL/SQL basics** (procedures, functions, packages, triggers)
- Performance tuning basics
- **TOAD for Oracle** — the GUI your company uses: interface tour, running queries, schema browser, data export, explain plans

## 5B — Hadoop Ecosystem

- Why Hadoop exists and why we still need to know it
- **HDFS architecture** (NameNode, DataNode, blocks, replication)
- **YARN** (resource manager)
- **MapReduce paradigm** (conceptual — you won't write these, but you need to understand them)
- Hadoop vs Spark (why Spark replaced MapReduce)
- **Hive** — SQL on Hadoop, HiveQL, managed vs external tables, partitioning, bucketing, metastore, file formats (ORC, Parquet)
- **Sqoop** — RDBMS ↔ HDFS bridge, full/incremental/append/last-modified imports, exports, tuning
- **HBase** — conceptual overview (NoSQL on Hadoop)
- **Oozie** — Hadoop's scheduler (briefly, since your company uses AutoSys instead)
- **Impala / Presto / Trino** — interactive SQL engines
- Hadoop ecosystem map — so you know which tool does what

## 5C — AWS for Data Engineers

- IAM deeper (roles, policies, assume role, trust relationships)
- S3 deeper (buckets, prefixes, versioning, lifecycle, storage classes, encryption)
- EC2 deeper
- **EMR (Elastic MapReduce)** — what it is, how to spin up a cluster, running Spark/Hive on EMR, cluster sizing
- Glue basics
- Athena basics
- Redshift overview
- CloudWatch (logs, metrics, alarms)
- Lambda basics
- Step Functions conceptual
- **Cost management** — a real DE skill

## 5D — Snowflake Deep Dive

- Snowflake architecture (storage, compute, cloud services)
- Warehouses and scaling, suspend/resume
- Databases, schemas, tables, views, materialized views
- Snowflake-specific SQL (QUALIFY, FLATTEN, VARIANT, time travel, cloning)
- Stages (internal, external, user, table)
- File formats (CSV, JSON, Parquet, Avro)
- **COPY INTO** patterns and **Snowpipe**
- **Streams and Tasks** (native CDC + scheduling)
- **RBAC** (roles and grants)
- Performance (clustering keys, result cache, query profile)
- Resource monitors and credits
- **Zero-copy cloning, time travel, fail-safe** (unique Snowflake features)

## 5E — Enterprise DevOps & Scheduling Tools

- **AutoSys** — jobs, boxes, calendars, JIL syntax, dependencies, machines, sendevent commands
- **Jenkins** — jobs, pipelines, Jenkinsfile, Groovy basics, plugins, parameters, triggers
- **uDeploy (IBM UrbanCode Deploy)** — applications, components, environments, processes, snapshots, promoting releases
- **PuTTY** advanced features — session profiles, logging, tunnels, key management

## 5F — Shell Scripting for Enterprise Pipelines

- Writing production-grade shell scripts
- Error handling in bash (`set -e`, `set -u`, trap)
- Argument parsing
- Logging patterns
- Cron and when not to use it
- Writing reusable utility functions

## Deliverable
A project that mirrors real enterprise work: extract from Oracle via Sqoop → Hive on EMR → transform → load to Snowflake → orchestrated by a Jenkins + AutoSys + uDeploy workflow. Fully documented.

---

# PHASE 6 — Modern Data Engineering Tools

**Duration:** 8-10 weeks
**Why this phase exists:** These are the tools that the industry is moving toward. Even if your current company doesn't use them all, interviewers will ask, and your next company will.

## 6A — Apache Spark & PySpark

- Why distributed computing matters
- Spark architecture (driver, executors, cluster manager)
- RDDs, DataFrames, Datasets
- **Transformations vs actions** (lazy evaluation)
- Spark SQL
- **Performance tuning** (partitioning, shuffles, caching, broadcast joins, skew)
- Spark on EMR
- Spark on Databricks

## 6B — Apache Airflow (deeper)

- DAG design patterns
- All operator types, sensors, hooks, XCom
- Connections, variables, pools
- Task groups, dynamic task mapping
- SLAs and alerting
- Production best practices

## 6C — dbt (data build tool)

- What dbt is and why analytics engineers love it
- Models, sources, seeds, snapshots
- **Jinja templating** and macros
- Tests (schema tests, data tests, custom)
- Documentation and lineage graphs
- dbt Core vs dbt Cloud

## 6D — Containerization

- Docker deeper (Dockerfile, images, containers, volumes, networks)
- **docker-compose**
- **Kubernetes** conceptual (pods, services, deployments, namespaces)
- When a DE needs K8s vs not

## 6E — Kafka & Streaming

- Event-driven architecture
- Kafka architecture (brokers, topics, partitions, producers, consumers, consumer groups)
- Kafka Connect
- Schema registry
- Kafka Streams conceptually
- **When to choose streaming vs batch**

## 6F — Databricks

- Workspace, clusters, notebooks, jobs
- **Delta Lake deep dive** (ACID on data lakes, time travel, OPTIMIZE, VACUUM)
- Databricks SQL warehouses
- Unity Catalog
- **Databricks vs Snowflake** head-to-head

## 6G — Infrastructure as Code

- Terraform basics (providers, resources, state, modules)
- Writing Terraform for AWS
- Drift and state management
- AWS CloudFormation overview

## 6H — Data Quality & Observability

- Great Expectations
- dbt tests revisited
- Monte Carlo / Soda concepts
- Writing data quality checks yourself

## 6I — NoSQL & Specialized Databases

- **MongoDB** basics — document model, when to use
- **DynamoDB** basics — AWS's NoSQL, partition keys
- **Cassandra** conceptual — wide-column, when to use
- **Redis** basics — caching, session storage
- **ClickHouse / Druid** conceptual — real-time analytics databases
- **The decision framework: when to pick which database** (this is the actual skill)

## 6J — Data Visualization for DEs

- **Tableau** basics — connecting to Snowflake, building a simple dashboard
- **Power BI** basics — Microsoft shops use it everywhere
- **Looker** conceptual (LookML)
- How DEs support BI teams without becoming their unpaid help desk

## 6K — APIs & GraphQL

- REST API design principles
- Consuming REST APIs in pipelines
- **GraphQL** conceptual
- Authentication (API keys, OAuth, JWT)

## Deliverable
A modern data stack project: ingest API data → Kafka → Spark on Databricks → Delta Lake → dbt transforms → Tableau dashboard, orchestrated by Airflow, deployed via Terraform.

---

# PHASE 7 — MLOps Foundations

**Duration:** 8-10 weeks
**Why this phase exists:** Modern data engineers are expected to support ML workflows. Companies don't hire separate "MLOps engineers" anymore at most places — they expect DEs to do it. This phase makes you MLOps-literate.

## 7A — ML Crash Course for DEs

- ML vs DL vs AI
- Supervised, unsupervised, reinforcement learning
- Training, validation, test sets
- Features, labels, models
- Common algorithms at a high level (linear regression, logistic regression, decision trees, random forest, gradient boosting, neural networks)
- **Evaluation metrics** (accuracy, precision, recall, F1, ROC-AUC, RMSE, MAE)
- **Why data engineers need to understand ML**

## 7B — ML Lifecycle

- Problem framing
- Data collection and labeling
- Feature engineering
- Model training and evaluation
- **Deployment patterns** (batch, online, edge)
- Model monitoring (performance, drift, bias)
- Retraining triggers

## 7C — MLOps Tools

- **MLflow** (experiment tracking, model registry, deployment)
- **DVC** (Data Version Control)
- **Feast** (feature store)
- **FastAPI / BentoML** (model serving)
- **Evidently AI** (monitoring)
- CI/CD for ML with GitHub Actions

## 7D — End-to-End MLOps Project

- Use your existing DEF pipeline data
- Train a fraud detection model on the CLAIMS table
- Track experiments with MLflow
- Deploy the model with FastAPI
- Monitor with Evidently AI
- Retrain weekly via Airflow
- Log predictions back to Snowflake

## Deliverable
A complete MLOps extension to your DEF project, deployed and documented.

---

# PHASE 8 — Anthropic / Claude Integration

**Duration:** 3-4 weeks
**Why this phase exists:** AI is becoming part of every data pipeline. Learning to integrate Claude into your workflows puts you ahead of 95% of data engineers.

## Topics

- **Claude 101** (Anthropic Academy) — general introduction
- **Prompt engineering for data tasks** — writing prompts that produce reliable, structured output
- **Building with the Claude API** — API calls, tool use, streaming, caching
- **Model Context Protocol (MCP)** — connecting Claude to external tools and data sources
- **Agent Skills** — reusable markdown instructions that Claude auto-applies

## Deliverable
A Claude-powered data tool — for example: auto-generating data quality descriptions from table schemas, explaining pipeline failures in plain English, or documenting SQL queries automatically.

---

# PHASE 9 — Interview & Portfolio Prep

**Duration:** Ongoing, parallel to Phases 6-8
**Why this phase exists:** Learning is only valuable if it translates into a career. This phase runs alongside later phases so you're always job-ready.

## 9A — System Design for Data Engineers

- How to design a data pipeline from scratch in an interview
- Common system design patterns
- Whiteboard-style exercises
- Tradeoffs and decision frameworks

## 9B — Technical Interview Prep

- SQL interview problems (hard category)
- Python coding problems (DE flavored)
- Architecture and scenario questions
- Debugging scenarios

## 9C — Behavioral Interview Prep

- **STAR method** (Situation, Task, Action, Result)
- Common behavioral questions
- Telling your story convincingly

## 9D — Portfolio & Personal Brand

- Polishing your GitHub
- Building a portfolio website
- LinkedIn optimization
- **Writing blog posts about your projects** — massive credibility boost
- Contributing to open source

## 9E — Mock Interviews

- Simulated technical rounds
- Simulated behavioral rounds
- Post-interview debriefs

## Deliverable
A portfolio site, an optimized LinkedIn, 3+ blog posts about your projects, and confidence walking into any DE interview.

---

# Quick Reference: Phase Durations

| Phase | Topic | Duration |
|-------|-------|----------|
| 0 | Environment & Documentation Setup | 1 week |
| 1 | Foundational Data Concepts | 4-5 weeks |
| 2 | Linux, Command Line & Git | 2-3 weeks |
| 3 | SQL Mastery | 5-6 weeks |
| 4 | Python for Data Engineering | 5-6 weeks |
| 5 | Your Company Stack | 8-10 weeks |
| 6 | Modern Data Engineering Tools | 8-10 weeks |
| 7 | MLOps Foundations | 8-10 weeks |
| 8 | Anthropic / Claude Integration | 3-4 weeks |
| 9 | Interview & Portfolio Prep | Parallel to 6-8 |

**Total: ~14-20 months at 30 min/day**

---

# What We Are NOT Covering (and Why)

- **Writing your own database from scratch** — fascinating but overkill
- **Deep distributed systems theory** (Paxos, Raft, CAP theorem proofs) — we'll touch CAP at a high level
- **Rust/Go/Scala for DE** — Python is enough; pick these up later if needed
- **Advanced deep learning** — MLOps covers enough ML to support it, not to become a data scientist

---

# Progress Tracking

At the end of each phase, we'll update this document with:
- Completion date
- Key concepts mastered
- Projects delivered
- Links to your learning repo entries
- Notes on what was hardest and easiest

---

# Final Notes

This curriculum is a living document. As you learn, priorities may shift. New tools may emerge. You may discover you love one area and want to go deeper, or find another area less interesting than expected. That's normal and fine — we'll adjust as we go.

The only non-negotiable rule: **keep showing up**. Even 15 minutes on a tired day is better than zero. The students who finish are not the smartest — they are the most consistent.

Let's begin.
