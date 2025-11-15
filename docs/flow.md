graph TD
    A[User / Client] --> B[Streamlit UI]
    B --> C[Backend Services]
    C --> D[OR Optimization Engine]
    C --> E[AI Insight Engine]
    C --> F[Export Service]
    C --> G[Storage Layer]
    
    subgraph Streamlit UI
        B1[Job Input Form]
        B2[Machine Input Form]
        B3[Schedule Viewer / Gantt]
        B4[AI Insight Panel]
        B5[Export Buttons PDF/XLS]
    end
    B --> B1
    B --> B2
    B --> B3
    B --> B4
    B --> B5
    
    subgraph Backend Services
        C1[Data Service]
        C2[Optimization Engine]
        C3[AI Insight Engine]
        C4[Export Service]
    end
    C --> C1
    C --> C2
    C --> C3
    C --> C4
