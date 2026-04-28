# Methodology

This research follows an **experimental and design-oriented approach**, structured in the following phases:

---

## Phase 1: Problem Definition

- Identification of the research problem
- Selection of the target Non-Functional Requirement (Maintainability)
- Definition of research questions and objectives

---

## Phase 2: Theoretical Analysis

- Review of literature on:
  - Technical debt
  - Non-functional requirements
  - Software maintainability
  - Multiagent systems
  - AI in software engineering

---

## Phase 3: System Design

- Definition of a conceptual multiagent architecture:
  - Code Ingestion Agent
  - Repository Analyzer Agent
  - RNF Debt Detector Agent
  - Solution Recommender Agent
  - Report Generator Agent

- Definition of metrics and indicators of maintainability

---

## Phase 4: Implementation (PoC)

- Development of a Proof of Concept in Python
- Integration of:
  - Static analysis tools (Radon, Lizard, etc.)
  - LLM-based components for reasoning and recommendations

---

## Phase 5: Experimental Evaluation

- Selection of representative software repositories
- Execution of the system on selected repositories
- Collection of results:
  - Detected technical debt
  - Generated recommendations

---

## Phase 6: Analysis of Results

- Evaluation of:
  - Accuracy of detection
  - Relevance of recommendations
  - Explainability of outputs

- Comparison with traditional tools

---

## Phase 7: Conclusions and Future Work

- Identification of limitations
- Proposal of extensions:
  - Additional NFRs (performance, security, scalability)
  - Improved AI models