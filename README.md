# Day 8 — Multi-Agent Ontology Builder
### AI Skills Bootcamp · Day 8 of 30

An autonomous multi-agent system that builds a structured knowledge graph from any domain.

---

## What It Does

1. **Plans** — ResearchPlanner picks 8-12 Wikipedia articles via Groq LLM
2. **Fetches** — Wikipedia Mediawiki API (clean plain-text, up to 12,000 chars)
3. **Extracts** — LLM pulls entities & relationships from chunked text
4. **Builds** — NetworkX DiGraph with multi-source node tracking
5. **Analyzes** — CoverageAnalyzer scores completeness per source, detects gaps
6. **Visualizes** — 6-tab Streamlit dashboard with 3D graph

---

## Quick Start

```bash
git clone https://github.com/YOUR_USERNAME/ai-skills-bootcamp.git
cd ai-skills-bootcamp
pip install -r requirements.txt
streamlit run app.py
```

Get a free Groq API key at https://console.groq.com

---

## File Structure

```
ai-skills-bootcamp/
├── app.py           # Streamlit UI — 6-tab dashboard
├── builder.py       # OntologyBuilder — LLM extraction + multi-source tracking
├── coverage.py      # CoverageAnalyzer — scoring + gap detection
├── planner.py       # ResearchPlanner — Wikipedia article selection
├── requirements.txt
├── .env.example
└── README.md
```

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| LLM | Groq · qwen/qwen3.8-27b |
| Knowledge Graph | NetworkX DiGraph |
| Visualization | Plotly (3D + charts) |
| UI | Streamlit 1.32+ |
| Data Source | Wikipedia Mediawiki API |
| HTTP | httpx |

---

## Example Output — Reinforcement Learning

- 383 nodes · 721 edges · 15 source clusters
- 71-72% completeness on core articles
- Gaps auto-detected with fill suggestions

---

## Author

**Tsegai Yhdego, Ph.D.**
Postdoctoral Researcher · R-SEAT Center · FAMU-FSU
AI Skills Bootcamp · 2026
