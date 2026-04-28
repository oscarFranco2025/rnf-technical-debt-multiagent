# RNF Technical Debt Multiagent

##  Overview

This project presents a **research-oriented Proof of Concept (PoC)** for a multiagent system designed to analyze software repositories and identify **technical debt associated with Non-Functional Requirements (NFRs)**.

The initial focus is on the **Maintainability NFR**, aiming to detect structural and design issues in source code and generate **AI-based recommendations** for improvement.

---

##  Objective

To design and validate a **multiagent architecture** capable of:

- Analyzing source code repositories.
- Detecting technical debt linked to a specific NFR.
- Providing explainable and actionable improvement recommendations.

---

##  Research Context

This work is developed within a **Software Engineering research group (Semillero SOLID)** and contributes to the intersection of:

- Software Architecture
- Technical Debt Analysis
- Artificial Intelligence applied to Software Engineering
- Multiagent Systems

---

##  Problem Statement

Modern software systems accumulate technical debt that directly impacts **non-functional requirements**, especially maintainability.

Current tools:
- Focus on metrics (e.g., complexity, duplication)
- Lack contextual understanding
- Do not provide intelligent recommendations

This project addresses the need for:

> Intelligent, explainable, and automated analysis of technical debt aligned with NFRs.

---

##  Scope

### Phase 1 (Current)

- Definition of research problem
- NFR selection (Maintainability)
- Requirements specification
- Conceptual multiagent architecture design
- Identification of analysis metrics
- Definition of evaluation strategy

### Future Phases

- Implementation of multiagent system
- Integration with static analysis tools
- LLM-based reasoning for debt detection
- Automated report generation
- Experimental validation

---

##  Selected NFR: Maintainability

### Definition

Maintainability refers to the ease with which a software system can be:

- Understood
- Modified
- Tested
- Extended

### Technical Debt Indicators

The system will detect issues such as:

- High cyclomatic complexity
- Long methods and large classes
- Code duplication
- High coupling
- Low cohesion
- Lack of tests
- Violations of SOLID principles

---

##  Multiagent Architecture (Conceptual)

The system is composed of the following agents:

1. **Code Ingestion Agent**
   - Clones and prepares the repository.

2. **Repository Analyzer Agent**
   - Extracts structural and metric-based information.

3. **RNF Debt Detector Agent**
   - Identifies technical debt related to maintainability.

4. **Solution Recommender Agent**
   - Generates AI-based recommendations.

5. **Report Generator Agent**
   - Produces structured technical reports.

---

##  System Workflow

1. Input repository (URL or local path)
2. Repository analysis and metric extraction
3. Detection of technical debt (based on NFR)
4. AI-driven recommendation generation
5. Report generation

---

## 🧪 Research Questions

- Can a multiagent system improve technical debt detection compared to traditional tools?
- How effectively can LLMs interpret code quality issues?
- Can AI generate actionable and reliable refactoring recommendations?

---

##  Evaluation Metrics

The PoC will evaluate:

- Detection accuracy
- Relevance of recommendations
- Explainability of results
- Coverage of technical debt indicators
- Consistency across analyses

---

## 🛠️ Planned Technologies

- **Python**
- FastAPI
- Streamlit
- OpenAI API / LLMs
- GitPython
- Radon / Lizard / Semgrep

---

##  Repository Structure

```text
docs/             → Research documentation
requirements/     → Functional and non-functional requirements
architecture/     → System design and diagrams
research/         → Questions, hypotheses, metrics
prompts/          → AI prompts for agents
reports/          → Generated outputs
src/              → Implementation (future phase)
