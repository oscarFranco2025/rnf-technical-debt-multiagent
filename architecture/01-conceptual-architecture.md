# Conceptual Architecture

## Overview

This project proposes a multiagent system to detect technical debt associated with Non-Functional Requirements (NFR), focusing on maintainability.

---

## High-Level Architecture

```mermaid
flowchart TD
    U[User] --> UI[UI]
    UI --> API[API]
    API --> ORCH[Orchestrator]

    ORCH --> A1[Ingestion]
    ORCH --> A2[Analyzer]
    ORCH --> A3[Debt Detector]
    ORCH --> A4[Recommender]
    ORCH --> A5[Reporter]

    A1 --> GIT[Git]
    GIT --> REPO[Repository]

    A2 --> REPO
    A2 --> STATIC[Static Analysis]
    STATIC --> METRICS[Metrics]

    A3 --> METRICS
    A3 --> LLM[LLM]

    A4 --> LLM
    A4 --> SOL[Solutions]

    A5 --> METRICS
    A5 --> SOL
    A5 --> REPORT[Report]

    REPORT --> UI
```

---

## Agent Workflow

```mermaid
flowchart LR
    A1[Ingestion] --> A2[Analysis]
    A2 --> A3[Detection]
    A3 --> A4[Recommendation]
    A4 --> A5[Report]

    A2 --> M[Metrics]
    M --> A3

    A3 --> D[Debt]
    D --> A4

    A4 --> S[Solutions]
    S --> A5
```

---

## Sequence Diagram

```mermaid
sequenceDiagram
    participant User
    participant UI
    participant API
    participant ORCH
    participant A1
    participant A2
    participant A3
    participant A4
    participant A5
    participant LLM

    User->>UI: Input repo
    UI->>API: Request
    API->>ORCH: Start

    ORCH->>A1: Clone
    A1-->>ORCH: Ready

    ORCH->>A2: Analyze
    A2-->>ORCH: Metrics

    ORCH->>A3: Detect
    A3->>LLM: Analyze
    LLM-->>A3: Result
    A3-->>ORCH: Debt

    ORCH->>A4: Recommend
    A4->>LLM: Suggest
    LLM-->>A4: Solutions
    A4-->>ORCH: Output

    ORCH->>A5: Report
    A5-->>API: Done

    API-->>UI: Result
```

---

## Layered Architecture

```mermaid
flowchart TB
    subgraph Presentation
        UI[UI]
    end

    subgraph API_Layer
        API[API]
    end

    subgraph Orchestration
        ORCH[Orchestrator]
    end

    subgraph Agents
        A1[Ingestion]
        A2[Analyzer]
        A3[Detector]
        A4[Recommender]
        A5[Reporter]
    end

    subgraph Services
        GIT[Git]
        STATIC[Static]
        LLM[LLM]
        REPORTS[Reports]
    end

    subgraph Data
        REPO[Repository]
        OUTPUT[Output]
    end

    UI --> API
    API --> ORCH
    ORCH --> A1
    ORCH --> A2
    ORCH --> A3
    ORCH --> A4
    ORCH --> A5

    A1 --> GIT --> REPO
    A2 --> STATIC --> REPO
    A3 --> LLM
    A4 --> LLM
    A5 --> REPORTS --> OUTPUT
```

---

## Explanation

### Multiagent Design

The system is divided into specialized agents:

- Code Ingestion Agent: clones and prepares repository  
- Repository Analyzer Agent: extracts structural and metric data  
- NFR Debt Detector Agent: identifies maintainability issues  
- Solution Recommender Agent: proposes improvements  
- Report Generator Agent: produces final report  

---

### Hybrid Analysis

The system combines:

- Static analysis → objective metrics  
- LLM reasoning → semantic understanding  

---

### Key Benefits

- Modular architecture  
- Scalable design  
- Explainable results  
- AI-assisted recommendations  

---

## Technology Stack

- Python  
- FastAPI  
- Streamlit  
- OpenAI API  
- Radon / Lizard / Semgrep  
- GitPython  