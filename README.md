# 🔴 RedditMindStream — Real-Time Reddit Sentiment & Trend Intelligence Pipeline

> Built by **Lakshman Rajith Rongala** | University of New Haven | [LinkedIn](https://www.linkedin.com/in/lakshmanrajith) | [Portfolio](https://heartfelt-zabaione-89c939.netlify.app) | [GitHub](https://github.com/rajith1612)

![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

---

## 🚀 Overview

**RedditMindStream** is an end-to-end data engineering pipeline that extracts live Reddit posts and comments using the **Reddit API (PRAW)**, orchestrates ingestion with **Apache Airflow**, stores raw data in **AWS S3**, transforms with **AWS Glue**, and loads analytics-ready data into **Amazon Redshift** — delivering real-time sentiment trends and subreddit intelligence via dashboards.

Built to answer intelligence questions like:
- 📈 What topics are trending on Reddit right now?
- 😡😊 What is the overall sentiment of a subreddit?
- 🔥 Which posts are going viral and why?
- 🕐 When is Reddit most active?

---

## 🏗️ Architecture

```
Reddit API (PRAW)
        ↓
Apache Airflow (Orchestration & Scheduling)
        ↓
Apache Celery (Distributed Task Queue)
        ↓
PostgreSQL (Metadata & Task State)
        ↓
AWS S3 (Raw Data Lake)
        ↓
AWS Glue (ETL & Schema Crawling)
        ↓
Amazon Athena (Ad-hoc Querying)
        ↓
Amazon Redshift (Data Warehouse)
        ↓
Power BI / Metabase (Dashboard)
```

---

## ✨ Features

- 📡 **Reddit API Ingestion** — Extracts posts, comments, scores, and metadata from any subreddit
- 📅 **Airflow Orchestration** — Scheduled DAGs for automated daily ingestion
- ☁️ **AWS Data Lake** — Raw data stored in S3 with Glue crawlers for schema discovery
- 🔍 **Athena Querying** — Ad-hoc SQL queries directly on S3 data
- 🏭 **Redshift Warehouse** — Analytics-ready tables for trend and sentiment analysis
- 📊 **Sentiment Dashboards** — Visualize trending topics, sentiment scores, and engagement

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Data Extraction | Reddit API (PRAW), Python |
| Orchestration | Apache Airflow, Celery |
| Message Queue | Redis |
| Metadata Store | PostgreSQL |
| Data Lake | AWS S3 |
| ETL | AWS Glue |
| Query Engine | Amazon Athena |
| Data Warehouse | Amazon Redshift |
| Containerization | Docker, Docker Compose |
| Language | Python, SQL |

---

## 📁 Project Structure

```
RedditMindStream/
├── airflow/
│   ├── dags/                 # Airflow DAG definitions
│   └── config/               # Airflow configuration
├── pipelines/
│   ├── reddit_pipeline.py    # Reddit API extraction
│   ├── aws_s3_pipeline.py    # S3 upload pipeline
│   └── aws_redshift_pipeline.py  # Redshift load pipeline
├── etls/
│   ├── reddit_etl.py         # ETL transformation logic
│   └── aws_etl.py            # AWS ETL helpers
├── utils/                    # Utility functions
├── config/                   # Configuration files
├── docker-compose.yml        # Docker setup
└── README.md
```

---

## 📊 Dashboard Preview

The sentiment dashboard tracks:
- **Trending Topics** — Top posts by upvotes and comments
- **Sentiment Score** — Positive/negative/neutral trends by subreddit
- **Engagement Metrics** — Comment velocity and award rates
- **Time Analysis** — Peak activity hours and posting patterns

---

## 📈 Key Results

| Metric | Result |
|--------|--------|
| Subreddits Tracked | 10+ |
| Posts Ingested Daily | 5,000+ |
| Pipeline Latency | < 1 hour |
| Sentiment Categories | Positive, Negative, Neutral |
| Dashboard KPIs | Trends, sentiment, engagement, timing |

---

## ⚙️ Setup & Usage

```bash
# Clone the repo
git clone https://github.com/rajith1612/RedditMindStream.git
cd RedditMindStream

# Set up configuration
cp config/config.conf.example config/config.conf
# Add your Reddit API credentials and AWS keys

# Start all services with Docker
docker-compose up -d

# Access Airflow UI
# Open http://localhost:8080
# Username: admin | Password: admin

# Trigger the pipeline
# Enable and trigger the reddit_dag in Airflow UI
```

---

## 🔑 Prerequisites

- Reddit API credentials (Client ID, Secret) from `reddit.com/prefs/apps`
- AWS Account with S3, Glue, Athena, Redshift access
- Docker and Docker Compose installed

---

## 📬 Contact

**Lakshman Rajith Rongala**
- 📧 Email: lakshmanrajith777@gmail.com
- 💼 LinkedIn: [linkedin.com/in/lakshmanrajith](https://www.linkedin.com/in/lakshmanrajith)
- 🌐 Portfolio: [heartfelt-zabaione-89c939.netlify.app](https://heartfelt-zabaione-89c939.netlify.app)
- 🐙 GitHub: [github.com/rajith1612](https://github.com/rajith1612)
