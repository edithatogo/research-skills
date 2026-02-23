# Research Skills - Comprehensive Research Automation

**Version:** 2.0.0  
**SKILL.md Specification:** v2.0 (arXiv:2602.12430)

Comprehensive research automation skills integrating Anthropic's agent skills approach with academic research workflows.

---

## Installation

```bash
# Universal installer
agent-skill install edithatogo/research-skills --platform all

# Platform-specific
cd research-skills
bash adapters/claude-code/install.sh  # Claude Code
bash adapters/gemini-cli/install.sh   # Gemini CLI
bash adapters/qwen-cli/install.sh     # Qwen CLI
```

---

## Skills Overview

### 1. Literature Search
**Trigger:** `/research:search`

Automated literature search across academic databases.

- **Database Connectors:** PubMed, Scopus, Web of Science, OpenAlex
- **Search Strategy Generator:** Boolean logic, MeSH terms
- **Deduplication Engine:** Remove duplicate results
- **Citation Export:** BibTeX, EndNote, Zotero formats

### 2. Evidence Synthesis
**Trigger:** `/research:synthesize`

Systematic review and evidence synthesis automation.

- **PRISMA Automation:** Flow diagram generation
- **Data Extraction:** Structured extraction forms
- **Risk of Bias:** Cochrane RoB tools
- **Meta-Analysis:** Statistical pooling (when applicable)

### 3. Writing Assistant
**Trigger:** `/research:write`

Academic writing support and manuscript preparation.

- **Manuscript Structure:** IMRAD formatting
- **Citation Manager:** In-text citations, reference lists
- **Journal Selector:** Match manuscript to journals
- **Response to Reviewers:** Draft revision letters

### 4. Data Analysis
**Trigger:** `/research:analyze`

Statistical analysis guidance and visualization recommendations.

- **Statistical Advisor:** Test selection guidance
- **Visualization Recommender:** Chart type selection
- **Reproducibility Checker:** Methods verification
- **Power Analysis:** Sample size calculations

### 5. Collaboration
**Trigger:** `/research:collaborate`

Research collaboration and project management.

- **Coauthor Manager:** Role assignment, task tracking
- **Version Control:** Git integration for manuscripts
- **Response to Reviewers:** Collaborative revision

---

## MCP Integrations

| Connector | Description |
|-----------|-------------|
| `pubmed` | PubMed/MEDLINE database access |
| `scopus` | Scopus abstract and citation database |
| `openalex` | OpenAlex open research catalog |
| `zotero` | Zotero reference management |
| `overleaf` | Overleaf LaTeX editor integration |
| `osf` | Open Science Framework project management |
| `crossref` | Crossref DOI and metadata API |

---

## Cross-Repository Dependencies

This repository depends on:

| Repository | Skills |
|------------|--------|
| **humanizer-next** | scientific-writing, reasoning-diagnostics, citation-management |
| **conductor-next** | conductor-implement, conductor-review |
| **knowledge-work-plugins-next** | health/systematic-review, health/manuscript-prep, health/grant-writer |

---

## Usage Examples

### Literature Search
```bash
# Search PubMed
/research:search --database pubmed --query "diabetes AND metformin" --max-results 50

# Search multiple databases
/research:search --databases pubmed,scopus,openalex --query "cancer immunotherapy"

# Export results
/research:search --export bibtex --output references.bib
```

### Evidence Synthesis
```bash
# Start systematic review
/research:synthesize --new --topic "Vitamin D supplementation"

# Generate PRISMA flow diagram
/research:synthesize --prisma --included 25 --excluded 150

# Extract data from studies
/research:synthesize --extract --studies included-studies.xlsx
```

### Writing Assistant
```bash
# Structure manuscript
/research:write --structure --type "systematic-review"

# Format citations
/research:write --citations --style "vancouver" --references references.bib

# Select journal
/research:write --journal-selector --topic "public health" --impact-factor ">3"
```

### Data Analysis
```bash
# Statistical test selection
/research:analyze --statistical-advisor --data-type "continuous" --groups 2

# Generate visualization
/research:analyze --visualize --chart-type "forest-plot" --data meta-analysis.csv

# Check reproducibility
/research:analyze --reproducibility-check --methods-section methods.md
```

---

## Security

- **Permission Tier:** tier-2
- **Capabilities:** read_files, network_access, query_apis, write_documents
- **Restricted:** modify_external_databases, access_personal_data

---

## License

MIT License - See LICENSE file for details.

---

## References

1. Renjun Xu, Yang Yan. "Agent Skills for Large Language Models: Architecture, Acquisition, Security, and the Path Forward." arXiv:2602.12430. February 2026.

2. PRISMA Group. "PRISMA 2020 Explanation and Elaboration." BMJ 2021.

3. Cochrane. "Cochrane Handbook for Systematic Reviews of Interventions." Version 6.3, 2022.

4. Anthropic. "Claude Agent Skills." October 2025.

---

*Documentation Status: Draft v2.0*  
*Last Updated: 2026-02-24*
