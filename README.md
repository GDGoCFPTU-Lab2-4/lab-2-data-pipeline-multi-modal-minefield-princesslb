# Multi-Modal Minefield Data Pipeline

**VinUni Codelab 3 Advanced — Day 14 | Team E403-01**

A multi-modal data ingestion pipeline that processes PDF, HTML, CSV, transcript, and legacy code sources into a unified knowledge base using Google Gemini AI.

---

## Team Members

| # | Name | GitHub | Gmail |
|---|------|--------|-------|
| 1 | Lưu Linh Ly | darlinhlyluu| lyluulinh.work@gmail.com |
| 2 | Dương Quang Đông | West2light | quangdong010203@gmail.com |
| 3 | Vương Hoàng Giang | Kai6704 | gvuonghoang123@gmail.com |
| 4 | Lê Tuấn Đạt | LeTuanDat2k4 | letuandat220@gmail.com |

---

## Project Structure

```
.
├── raw_data/                   # Input data sources
│   ├── lecture_notes.pdf
│   ├── demo_transcript.txt
│   ├── product_catalog.html
│   ├── sales_records.csv
│   └── legacy_pipeline.py
├── starter_code/
│   ├── orchestrator.py         # Pipeline orchestrator (Role 4)
│   ├── schema.py               # Unified document schema (Role 1)
│   ├── process_pdf.py          # PDF extractor with Gemini AI (Role 2)
│   ├── process_transcript.py   # Transcript cleaner (Role 2)
│   ├── process_html.py         # HTML catalog parser (Role 2)
│   ├── process_csv.py          # CSV processor (Role 2)
│   ├── process_legacy_code.py  # Legacy code analyzer (Role 2)
│   └── quality_check.py        # Data quality gate (Role 3)
├── processed_knowledge_base.json  # Output
├── .env                        # API keys (not committed)
└── README.md
```

## Setup

```bash
# 1. Create virtual environment
python -m venv venv
venv\Scripts\activate       # Windows
# source venv/bin/activate  # Linux/macOS

# 2. Install dependencies
pip install -r requirements.txt

# 3. Configure API key
# Edit .env and set your Gemini API key (get it at https://aistudio.google.com/app/apikey)
GEMINI_API_KEY=AIzaSy...
GEMINI_MODEL=gemini-2.0-flash-lite
```

## Run

```bash
python starter_code/orchestrator.py
```

Output will be saved to `processed_knowledge_base.json`.

---

## Roles

| Role | Responsibility |
|------|---------------|
| Role 1 | Schema Design & Enforcement |
| Role 2 | Multi-modal Data Extraction |
| Role 3 | Data Quality Gate |
| Role 4 | DevOps & Pipeline Orchestration |
