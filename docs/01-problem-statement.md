# Problem Statement

Modern software systems continuously accumulate **technical debt**, which negatively impacts their evolution, maintainability, and overall quality.

While existing tools (e.g., static analyzers) can detect low-level issues such as code complexity or duplication, they present important limitations:

- They lack contextual understanding of software design decisions.
- They do not explicitly relate findings to **Non-Functional Requirements (NFRs)**.
- They do not provide intelligent or actionable recommendations for improvement.

Among NFRs, **maintainability** is one of the most critical, as it directly affects the cost, effort, and risk associated with software evolution.

Currently, there is a lack of intelligent systems capable of:

- Interpreting code structure and metrics in context.
- Identifying technical debt specifically linked to NFRs.
- Providing explainable and structured improvement strategies.

This research proposes the design of a **multiagent system supported by Artificial Intelligence**, capable of analyzing source code repositories, detecting technical debt associated with a specific NFR, and generating actionable recommendations.

The core research problem can be stated as:

> How can a multiagent system, supported by AI techniques, improve the detection and analysis of technical debt associated with non-functional requirements, specifically maintainability, in software repositories?