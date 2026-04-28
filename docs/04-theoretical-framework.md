# Theoretical Framework

## 1. Technical Debt

The concept of **technical debt** was introduced by Cunningham (1992) to describe the long-term consequences of suboptimal technical decisions made during software development.

Technical debt represents the gap between the current implementation and an optimal solution, leading to:

- Increased maintenance cost
- Reduced system quality
- Slower development velocity

Kruchten et al. (2012) expanded this concept by identifying different types of technical debt:

- Code debt
- Design debt
- Architecture debt
- Test debt

In this research, technical debt is analyzed in relation to **Non-Functional Requirements (NFRs)**, particularly maintainability.

---

## 2. Non-Functional Requirements (NFRs)

Non-Functional Requirements define the **quality attributes** of a system, including:

- Performance
- Security
- Usability
- Maintainability
- Scalability

Unlike functional requirements, NFRs describe **how the system behaves** rather than what it does.

According to ISO/IEC 25010, maintainability includes:

- Modularity
- Reusability
- Analyzability
- Modifiability
- Testability

This research focuses on maintainability due to its direct relationship with technical debt.

---

## 3. Software Maintainability

Maintainability refers to the ease with which software can be:

- Understood
- Modified
- Tested
- Extended

Low maintainability is commonly associated with:

- High cyclomatic complexity (McCabe, 1976)
- Long methods and large classes
- Code duplication
- Tight coupling
- Low cohesion

These indicators can be measured using static analysis tools.

---

## 4. Static Code Analysis

Static code analysis evaluates source code without executing it.

Common metrics include:

- Cyclomatic complexity
- Lines of code (LOC)
- Code duplication
- Dependency structures

Tools such as Radon, Lizard, and Semgrep allow automated extraction of these metrics.

However, static analysis has limitations:

- It lacks contextual understanding
- It cannot infer design intent
- It does not generate meaningful recommendations

This limitation motivates the integration of AI-based approaches.

---

## 5. Artificial Intelligence in Software Engineering

Artificial Intelligence has increasingly been applied to software engineering tasks, including:

- Code generation
- Code review
- Bug detection
- Refactoring recommendations

Recent advances in **Large Language Models (LLMs)** enable:

- Semantic understanding of code
- Natural language explanations
- Context-aware reasoning

LLMs can analyze not only syntax but also:

- Code intent
- Design patterns
- Architectural implications

This makes them suitable for identifying and explaining technical debt.

---

## 6. Multiagent Systems

A **multiagent system (MAS)** consists of multiple autonomous agents that interact to solve complex problems.

According to Wooldridge (2009), agents are entities capable of:

- Perceiving their environment
- Making decisions
- Acting independently

Multiagent systems are effective for:

- Decomposing complex tasks
- Distributing responsibilities
- Improving modularity and scalability

In this research, the analysis process is divided into specialized agents:

- Code ingestion
- Repository analysis
- Debt detection
- Recommendation generation
- Reporting

---

## 7. Integration of Static Analysis and AI

A key limitation of traditional tools is their reliance on **quantitative metrics only**.

Modern approaches propose combining:

- Static analysis → objective evidence
- AI (LLMs) → contextual reasoning

This hybrid approach enables:

- Detection based on measurable indicators
- Interpretation of results in context
- Generation of actionable recommendations

This research adopts this integration as a central design principle.

---

## 8. Research Gap

Existing technical debt detection tools:

- Focus primarily on metrics
- Do not explicitly relate findings to NFRs
- Do not provide intelligent recommendations

There is a lack of systems that:

- Align technical debt analysis with NFRs
- Integrate semantic reasoning
- Use modular architectures for analysis

This research addresses this gap through a multiagent, AI-supported approach.

---

## 9. LLMs and AI-Augmented Software Engineering (Modern Perspective)

Recent advances in AI, particularly **Large Language Models (LLMs)** such as GPT-4, Claude, CodeLlama, and StarCoder, have transformed software engineering.

LLMs enable:

- Semantic code understanding
- Automated reasoning over code structure
- Natural language explanations
- Generation of refactoring suggestions

Unlike traditional tools, LLMs provide:

- Context-aware analysis
- Design-level insights
- Human-readable explanations

However, challenges remain:

- Non-deterministic outputs
- Potential hallucinations
- Lack of grounding in formal metrics

---

## 10. Hybrid AI + Static Analysis Approaches

Modern research emphasizes combining:

- Static analysis (precision)
- LLM reasoning (context)

This enables:

- Evidence-based detection
- Contextual interpretation
- Intelligent recommendations

This research adopts this hybrid paradigm.

---

## 11. AI Agents and Agentic Architectures

Recent trends (2024–2026) introduce **AI agent-based systems**, where:

- Multiple agents collaborate
- Each agent has a specialized role
- Systems operate in coordinated pipelines

Frameworks such as:

- LangChain Agents
- AutoGen
- CrewAI

demonstrate the effectiveness of this paradigm.

This research aligns with these trends by proposing a **multiagent system for technical debt analysis**.

---

## 12. Relevance in the AI Era

This research is relevant because it:

- Moves beyond traditional metric-based tools
- Incorporates AI for semantic understanding
- Applies multiagent architectures to software quality analysis

It contributes to the intersection of:

- Software Engineering
- Artificial Intelligence
- Software Architecture
- Developer Productivity Tools

---

## References (Suggested)

- Cunningham, W. (1992). The WyCash portfolio management system.
- McCabe, T. (1976). A Complexity Measure.
- Kruchten, P., Nord, R., & Ozkaya, I. (2012). Technical Debt: From Metaphor to Theory.
- ISO/IEC 25010:2011. Systems and software quality models.
- Wooldridge, M. (2009). An Introduction to MultiAgent Systems.
- OpenAI (2023–2025). GPT-4 Technical Reports.
- Meta AI (2023). CodeLlama.
- BigCode Project (2023). StarCoder.