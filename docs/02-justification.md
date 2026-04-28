# Justification

The continuous growth of software systems leads to the accumulation of **technical debt**, which directly impacts software quality and evolution.

One of the most affected aspects is **maintainability**, a critical Non-Functional Requirement (NFR) that determines how easily a system can be understood, modified, and extended.

Poor maintainability results in:

- Increased development costs
- Higher risk of defects
- Reduced productivity
- Slower response to business changes

Although existing tools can measure code metrics, they present significant limitations:

- They operate at a syntactic level, without understanding context.
- They do not relate findings to NFRs explicitly.
- They do not provide actionable or intelligent recommendations.

Recent advances in **Artificial Intelligence, particularly Large Language Models (LLMs)**, open new possibilities for:

- Interpreting code beyond syntax
- Understanding design intent
- Generating contextual recommendations

Additionally, the use of **multiagent systems** allows the decomposition of complex analysis tasks into specialized components, improving modularity, scalability, and interpretability.

This research is justified because it proposes:

- A novel integration of AI and multiagent systems for software analysis
- A shift from metric-based analysis to **NFR-oriented analysis**
- A system capable not only of detecting issues but also suggesting solutions

The results of this work may contribute to:

- Improving software quality practices
- Supporting developers in decision-making
- Advancing research in AI-assisted software engineering