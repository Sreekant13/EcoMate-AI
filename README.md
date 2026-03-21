# EcoMate-AI

EcoMate-AI analyzes receipts, bills, and daily activities to estimate your carbon footprint and recommend greener choices, powered by multimodal AI.

Upload an image of a receipt or describe your day in plain text. The app extracts individual activities, maps them to verified CO₂ emission factors, and generates a personalized sustainability report with actionable tips.

**[View Live Demo](https://shamikofficial.github.io)** &nbsp;|&nbsp; **[Portfolio](https://shamikofficial.github.io)**

---

## Features

- **Multimodal input** — upload receipt images or enter free-form text
- **OCR extraction** — reads items, quantities, and services from scanned receipts
- **CO₂ estimation** — maps activities to verified global emission factors
- **Personalized tips** — AI-generated suggestions ranked by impact
- **Global comparison** — contextualizes your footprint against regional and world averages
- **Interactive visualizations** — category breakdowns and trend charts

## Tech stack

| Layer | Tools |
|---|---|
| Frontend | Streamlit |
| Backend | FastAPI |
| AI / OCR | OpenAI GPT-4o, Vision API |
| Data | pandas, NumPy |
| Visualization | Plotly, Matplotlib |

## Getting started

```bash
git clone https://github.com/ShamikOfficial/EcoMate-AI.git
cd EcoMate-AI
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env        # add your OpenAI API key
streamlit run app/main.py
```

## Project structure

```
EcoMate-AI/
├── app/
│   ├── main.py             # Streamlit frontend
│   ├── api.py              # FastAPI backend
│   ├── genai_model.py      # GenAI inference layer
│   ├── services/           # Carbon calculation logic
│   └── utils/              # Preprocessing helpers
├── data/                   # Emission factor datasets
└── requirements.txt
```

## How it works

1. User uploads a receipt image or types a description of their activities
2. OCR pipeline extracts line items and quantities
3. Each item is classified and matched to an emission factor (kg CO₂e)
4. Total footprint is calculated and broken down by category
5. GPT-4o generates ranked, personalized recommendations

## License

MIT
