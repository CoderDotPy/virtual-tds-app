# TDS Virtual TA 🤖

This project is a **Virtual Teaching Assistant** built for the **Tools for Data Science (TDS)** course in IIT Madras’ Online Degree in Data Science. It can automatically answer student questions using scraped Discourse posts and course content.

---

## 🔗 Live API Endpoint

📡 **API URL**:  
`[https://virtual-ta-app.onrender.com/api/](https://virtual-ta-app-28ts.onrender.com/query)`

Send a `POST` request with a student question (and optional file attachment) in JSON. Example:

```bash
curl "https://virtual-ta-app-28ts.onrender.com/query" \
  -H "Content-Type: application/json" \
  -d "{\"question\": \"Can I use gpt-4o-mini for this GA?\"}"

virtual-tds-app/
├── .gitignore
├── app.py                   # FastAPI app hosting the API
├── scraper_discourse.py     # ✅ Scraper for Discourse posts (date range supported)
├── scraper_course.py        # Scraper for course content
├── knowledge_base.db        # SQLite DB storing scraped data
├── requirements.txt         # Python dependencies
├── LICENSE                  # MIT License
└── README.md                # This file
