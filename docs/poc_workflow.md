POC_Workflow.md
Phase 1: Setup & Planning
Step 1: Define Scope

✅ Identify target users (e.g., small factories, workshops)

✅ Define POC goals:

Job input → optimized schedule → Gantt chart

Show AI insights (bottlenecks, priority suggestions)

Export schedule (PDF/Excel)

✅ Decide non-goals for POC (no multi-stage routing, no user accounts yet)

Step 2: Collect Sample Data

✅ Create sample machines dataset (ID, name, capacity)

✅ Create sample jobs dataset (ID, machine_required, processing_time, due_date, priority)

✅ Optional: real data from 1–2 pilot users

Phase 2: Environment & Tools
Step 3: Project Setup

✅ Create project folder (use structure suggested earlier)

✅ Setup virtual environment (venv / conda)

✅ Install required libraries:

pip install streamlit pandas plotly ortools openai


✅ Create .gitignore and initialize Git repo

Step 4: Create Markdown Docs for Planning

✅ 01-requirements.md

✅ 02-poc-architecture.md

✅ 03-data-model.md

✅ 04-optimization-model.md

✅ 05-ui-flow.md

✅ 06-testing-checklist.md

Phase 3: Backend (Core POC)
Step 5: Build Data Models

✅ Create data_models.py with:

Machine class

Job class

Schedule class

✅ Load sample data into Pandas DataFrames

Step 6: Implement OR Optimization

✅ Use OR-Tools CP-SAT solver

✅ Define variables: job start times

✅ Apply constraints:

One job per machine at a time

Due date priority

✅ Objective function: minimize makespan / delay

✅ Test optimizer on sample dataset

✅ Check for overlapping jobs → no overlaps

Step 7: AI Insight Engine (Optional POC)

✅ Simple rule-based insights:

Highlight machine bottlenecks

Flag jobs likely to be late

✅ Optional: connect GPT API to explain schedule

Phase 4: Frontend (Streamlit POC)
Step 8: Build UI Pages

✅ Home Page (home.py)

✅ Machine Input Page (machines.py)

✅ Job Input Page (jobs.py)

✅ Scheduler Page (scheduler.py)

✅ Results Page (results.py)

✅ Optional: AI Insight Panel

Step 9: Integrate OR Backend with Streamlit

✅ Add “Run Optimization” button

✅ Display Gantt chart with Plotly

✅ Show schedule summary: makespan, idle time

Step 10: Export Functionality

✅ Add “Download PDF” / “Export Excel” button

✅ Test export works correctly with sample schedule

Phase 5: Testing & Validation
Step 11: Unit & Integration Testing

✅ Test optimizer outputs valid schedules

✅ Test constraints are respected

✅ Test Gantt chart renders correctly

✅ Test exports are accurate

Step 12: Edge Case Testing

✅ Zero-duration jobs

✅ Missing data

✅ Overloaded machines

✅ Multiple jobs with same priority

Phase 6: Demo & Polish
Step 13: Polishing

✅ Streamlit theme / UI clean-up

✅ Sample datasets preloaded

✅ Include metrics panel: makespan reduction, idle time

Step 14: Demo Ready

✅ Prepare 1–2 demo scenarios

✅ Record video/screenshots for pitch

Phase 7: Checkpoints Before Funding Pitch

✅ POC works end-to-end (job input → optimized schedule → Gantt + AI insights → export)

✅ Metrics / success examples recorded

✅ Early user feedback collected (if possible)

✅ Markdown docs updated with POC details