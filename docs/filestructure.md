production-scheduler/
│
├── app/
│   ├── __init__.py
│   ├── ui/
│   │   ├── home.py
│   │   ├── machines.py
│   │   ├── jobs.py
│   │   ├── scheduler.py
│   │   ├── results.py
│   │   └── components/
│   │       ├── gantt_chart.py
│   │       └── tables.py
│   │
│   ├── core/
│   │   ├── data_models.py
│   │   ├── optimizer.py
│   │   ├── constraints.py
│   │   ├── ai_insights.py
│   │   └── utils.py
│   │
│   ├── services/
│   │   ├── exporter.py      # PDF/Excel exporters
│   │   └── storage.py       # simple SQLite or json
│   │
│   └── main.py              # Streamlit entry point
│
├── assets/
│   └── sample_data/
│       ├── machines.csv
│       ├── jobs.csv
│       └── example_schedule.json
│
├── docs/
│   ├── 01-requirements.md
│   ├── 02-poc-architecture.md
│   ├── 03-data-model.md
│   ├── 04-optimization-model.md
│   ├── 05-ui-flow.md
│   ├── 06-testing-checklist.md
│   └── 07-next-steps-mvp.md
│
├── tests/
│   ├── test_optimizer.py
│   ├── test_constraints.py
│   └── test_gantt.py
│
├── requirements.txt
└── README.md
