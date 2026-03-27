# AI Investment Advisor

A full-stack AI-powered investment portfolio recommendation system that integrates Constraint Satisfaction Problem (CSP) optimization with Modern Portfolio Theory (MPT) using a live covariance matrix. The system leverages an LLM agent to generate human-like financial insights and produces downloadable PDF reports, enabling data-driven and explainable investment decisions.

---
## Architecture
Frontend (HTML/CSS/JS)  <-->  FastAPI Backend  <-->  Investment Agent (CSP + MPT + Covariance)
                                                              |                    |
                                                    Live Market Data (yfinance)  LLM (OpenAI)                               

---

## Project Structure

├── backend/
│   ├── main.py                  # FastAPI app entry point
│   ├── agent.py                 # Investment advisor agent + LLM integration
│   ├── csp_solver.py            # Constraint Satisfaction Problem logic
│   ├── mpt_calculator.py        # Modern Portfolio Theory + Covariance Matrix
│   ├── market_data.py           # Live market data fetching (yfinance)
│   ├── country_products.py      # Country-specific investment products (Python)
│   ├── country_specific_info.json  # Country-specific products (JSON)
│   ├── report_generator.py      # PDF report generation (ReportLab)
│   ├── models.py                # Pydantic models for request/response
│   └── requirements.txt         # Python dependencies
├── frontend/
│   ├── index.html               # Main webpage
│   ├── style.css                # Styling
│   └── app.js                   # JS to call the API and render results
├── .env.example                 # Environment variable template
├── REPORT.md                    # Comprehensive technical report
├── PRESENTATION.md              # 5-slide presentation
└── README.md

---
## Tech Stack

| Layer                     | Technology                           | Purpose                                                                     |
| ------------------------- | ------------------------------------ | --------------------------------------------------------------------------- |
| ⚙️ Backend API            | FastAPI + Uvicorn                    | High-performance API for handling requests and serving ML outputs           |
| 📊 Portfolio Optimization | python-constraint (CSP), NumPy (MPT) | Constraint-based portfolio selection + Modern Portfolio Theory calculations |
| 📈 Market Data            | yfinance (Yahoo Finance)             | Fetches real-time and historical stock market data                          |
| 🤖 AI / LLM Agent         | OpenAI GPT-4o-mini (with fallback)   | Generates investment insights and explanations                              |
| 📄 Reporting              | ReportLab                            | Generates downloadable PDF investment reports                               |
| 🎨 Frontend               | HTML5, CSS3, Vanilla JavaScript      | Lightweight and responsive user interface                                   |
| 📉 Data Visualization     | Chart.js                             | Interactive charts for portfolio performance 

---
## How to Run Locally

```bash
git clone git@github.com:Vangala09/ai-investment-advisor.git
cd ai-investment-advisor
pip install -r requirements.txt
python app.py
```
---

## Use Case

This project demonstrates how AI can be applied in finance to:

* Improve investment decisions
* Analyze portfolio performance
* Reduce financial risk

---

## Author

**Reshma Vangala**
**Viren**

