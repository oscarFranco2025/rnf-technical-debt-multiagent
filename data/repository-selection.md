# Repository Selection

## Objective

Define the criteria and selection of repositories to be used in the experimental evaluation of the proposed multiagent system.

---

## Selection Criteria

Repositories must meet the following conditions:

### 1. Public Availability
- Must be hosted on GitHub.
- Must be accessible without restrictions.

---

### 2. Code Quality Variability
- Include repositories with:
  - High quality
  - Medium quality
  - Low quality (expected technical debt)

---

### 3. Size Diversity
- Small: < 1,000 lines
- Medium: 1,000 – 10,000 lines
- Large: > 10,000 lines

---

### 4. Activity Level
- Prefer repositories with:
  - Multiple commits
  - Active development history

---

### 5. Language (Initial Scope)
- Python (recommended for PoC)
- Optional: JavaScript, Java, C#

---

## Selected Repositories (Initial Set)

| Name | URL | Language | Size | Expected Debt |
|-----|-----|--------|------|--------------|
| Flask | https://github.com/pallets/flask | Python | Medium | Low |
| Requests | https://github.com/psf/requests | Python | Medium | Medium |
| Legacy Sample | https://github.com/realpython/python-guide | Python | Large | Mixed |

---

## Rationale

Using diverse repositories allows:

- Testing system robustness
- Evaluating detection across different contexts
- Validating scalability of the approach

---

## Future Expansion

Future experiments may include:

- Industry-level repositories
- Microservices architectures
- Multi-language projects