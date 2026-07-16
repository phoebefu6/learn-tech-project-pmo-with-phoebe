# learn tech project PMO with phoebe

Run a data platform build like a pro - six 45-minute sessions that turn a vague "get all our
data into a warehouse" mandate into a controlled program.

You learn the PMO tools senior data and tech leaders actually use - project charter, milestone
architecture, dependency gates, risk register, RACI, and a delivery tracker - applied end to
end to one running case: **Northwind**, a fictional retailer building a governed data platform
from a raw dump through to production BI and AI/ML. Northwind and every number in it are made
up: a generic teaching case with dummy data, no real company.

## Sessions

1. **Frame the initiative & write the charter** - context, position (interim vs final), P1-P4 priorities
2. **Milestone architecture** - the 5-column milestone table, laddering M1-M6 across the DW-to-AI lifecycle
3. **Dependencies & hard gates** - dependency types, the hiring hard gate, critical path, parallel tracks
4. **The risk register** - probability x impact, severity tags, mitigation / owner / trigger
5. **Ownership & RACI** - one accountable per row, internal vs external, escalation
6. **Sizing, benchmarking & tracking** - benchmark the scope, the migration tracker, RAG status, go-live

Each session ends with a build-along, a 3-question quiz, a sources-covered list, and a cheat sheet.

## Run locally

```bash
python3 -m http.server 8646
# open http://localhost:8646
```

Static HTML/CSS/JS, no build step.

by Phoebe Fu
