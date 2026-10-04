# Vietnam IT Job Market AI Pipeline (`vn-it-jobs-ai`)

An end-to-end Data Engineering and AI pipeline that collects, processes, and analyzes IT job market trends in Vietnam. The project integrates **Text-to-SQL** for quantitative analytical queries and **Retrieval-Augmented Generation (RAG)** for semantic job and skill matching.

---

## 📌 Project Objectives

1. **Data Engineering**: Build a structured pipeline to ingest, clean, and standardize Vietnamese IT job listings from Kaggle and live job portals.
2. **Database Analytics (Text-to-SQL)**: Store processed job attributes (salaries, locations, experience requirements, skill tags) in PostgreSQL / DuckDB to support SQL-based analytics and automated query generation.
3. **Semantic Assistant (RAG)**: Leverage LLMs and vector embeddings to answer qualitative questions based on full job descriptions, tech stack requirements, and career path recommendations.

---

## 📁 Repository Structure

```text
vn-it-jobs-ai/
├── data/
│   ├── raw/               # Raw Kaggle dataset and scraped files (gitignored)
│   └── sample/            # Small sample data files for repository testing
├── docs/                  # Project documentation & weekly logs
│   └── journal_week1.md   # Initial dataset analysis notes
├── notebooks/             # Data exploration & prototyping
│   └── 01_explore_kaggle_data.ipynb
├── src/                   # Production-ready source code (ETL, Scrapers, RAG)
├── .gitignore
├── LICENSE
└── README.md

🗺️ Project Roadmap
[x] Phase 1: Exploratory Data Analysis (Kaggle Vietnam Jobs Dataset)

[ ] Phase 2: Data Cleaning & Schema Normalization

[ ] Phase 3: Web Scraper Implementation (Collecting missing descriptions & recent posts)

[ ] Phase 4: Database Ingestion (PostgreSQL / DuckDB setup)

[ ] Phase 5: Text-to-SQL Pipeline Development

[ ] Phase 6: RAG Engine & Vector Store Integration

[ ] Phase 7: Evaluation & User Interface

⚙️ Setup & Installation
1. Prerequisites
Python 3.10+

Git

2. Quickstart
Clone the repository and set up a virtual environment:

git clone [https://github.com/duyditrongmua/vn-it-jobs-ai.git](https://github.com/duyditrongmua/vn-it-jobs-ai.git)
cd vn-it-jobs-ai

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows (PowerShell):
.\venv\Scripts\Activate.ps1
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

📊 Dataset Notice
The raw jobs.csv file contains raw job market data and is not committed to GitHub (excluded via .gitignore).

To reproduce the notebooks, place your source CSV files inside the data/raw/ directory or run the sample scripts under data/sample/.

📜 License
Distributed under the MIT License. See LICENSE for more information.