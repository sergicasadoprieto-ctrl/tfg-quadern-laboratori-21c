# 📓 QL21 — El Quadern de Laboratori del Segle XXI

> **The 21st Century Lab Notebook** — A practical, reusable documentation framework for experimental nanoscience research.

![Status](https://img.shields.io/badge/status-active-1B5E20?style=flat-square) ![Phase|84](https://img.shields.io/badge/phase-II%2FIII-4CAF50?style=flat-square) ![Version](https://img.shields.io/badge/manifest-v1.2-1B5E20?style=flat-square) ![License](https://img.shields.io/badge/license-CSIC%20Restricted-F57C00?style=flat-square) ![Institution](https://img.shields.io/badge/IMB--CNM-CSIC-263238?style=flat-square) ![University](https://img.shields.io/badge/UAB-2025--2026-263238?style=flat-square)

---

## What is this?

Modern experimental research suffers from a persistent problem: scientists know how to run experiments, but rarely document them well. Knowledge gets lost. Results are hard to reproduce. Documentation is always the last priority.

**QL21** addresses that gap by building a modern, reusable documentation framework — a system of templates, naming conventions and governance manifests that any student or researcher can adopt from day one of a new project.

The pilot environment is **IMB-CNM-CSIC**, one of the largest nanofabrication research centres in Spain. The framework is applied to a real research context, without touching any confidential data.

---

## Key Features

| Feature | Description |
| --- | --- |
| 📁 **Governance Manifests** | YAML-based project, user and branding manifests for full context portability |
| 📄 **Reusable Templates** | Lab Logs, Zettel Notes, Reports — all with YAML frontmatter |
| 🔖 **Naming Convention** | `{PREFIX}-{DATE}-{TIME}-{AUTHOR}-{VERSION}` — unambiguous and Git-friendly |
| 🌿 **FAIR-aligned** | Findable, Accessible, Interoperable, Reusable — by design |
| 🤖 **AI-ready** | Manifests load as context for any LLM — no re-explaining needed |
| 📐 **Git-native** | Designed for version-controlled, collaborative research workflows |

---

## Repository Structure

```text
tfg-quadern-laboratori-21c/
│
├── 00-governance/
│   ├── sergi-casado-profile-1.1.yaml
│   ├── tfg-project-manifest-1.2.yaml
│   ├── tfg-branding-manifest-1.1.yaml
│   └── SOW-TFG-2026-SCP-RACO-v1.1.md
│
├── 01-literature/
│   ├── notes/
│   ├── references/
│   └── D1-state-of-the-art.md
│
├── 02-framework/
│   └── templates/
│
├── 03-pilot/
│   ├── logs/
│   └── data/
│
├── 04-outputs/
│   ├── D5-tfg-memory/
│   └── D6-defence-slides/
│
├── 05-journal/
│
├── README.md
├── CHANGELOG.md
├── LICENSE.md
└── .gitignore
```

---

## Naming Convention

All artefacts follow a strict naming pattern:

{PREFIX}-{YYYYMMDD}T{HHmmss}-{AUTHOR}-{VERSION}

**Example:** `ZN-20260407T162000-SCP-1.00.md`

| PREFIX | Type |
| --- | --- |
| `LOG` | Laboratory Log |
| `ZN` | Zettel Note |
| `RPT` | Weekly Report |
| `PROJ` | Project Document |
| `TPL` | Template |
| `SOW` | Statement of Work |
| `MNF` | Manifest |
| `AS` | Automatic Summary |

---

## Deliverables

| ID  | Deliverable                   | Phase | Status         |
| --- | ----------------------------- | ----- | -------------- |
| D1  | State-of-the-Art Synthesis    | I     | ✅ Complete     |
| D2  | Documentation Framework       | II    | ⏳ Pending      |
| D3  | Pilot Repository (abstracted) | III   | 🔄 In Progress |
| D4  | Guide of Best Practices       | IV    | ⏳ Pending      |
| D5  | Final TFG Memory              | IV    | 🔄 In Progress |
| D6  | Oral Defence Material         | IV    | ⏳ Pending      |

---

## How to Use This Framework

### Without AI — Layer 1 and 2

This framework is fully functional without any AI tool.

1. Copy the repository structure to your project folder
2. Fill in the governance manifests in `00-governance/`
3. Copy the templates from `02-framework/templates/` to your working folder
4. Follow the naming convention for every file you create
5. Write your logs, notes and reports in plain Markdown
6. Commit to Git after each session with a descriptive message

That is all that is required to achieve full traceability, reproducibility, and FAIR compliance.

### With AI assistance — Layer 3 (optional)

AI tools can reduce documentation friction but are never required. Use them only for structural and formatting tasks — never for scientific content.

**Session 1 — Project initialisation**

### Starting a new project with this kit

**Session 1 — Project initialisation**

## Prompt 1 — Generate the SOW

Attach: oferta-proyecto.pdf + TPL-sow.md 
Goal: AI extracts and maps official data from the PDF into the structured Markdown template. 
Key Rule: No data invention; leave unknown fields as [RELLENAR].

## Prompt 2 — Generate the project manifest

Attach: TPL-project-manifest.yaml + user-profile.yaml 
Goal: AI cross-references the SOW (already in context) with your researcher profile to create the project's "Digital DNA". 
Format: Output strictly in YAML for machine-readability.

## Prompt 3 — Repository structure + recommended templates

No attachments needed — context is already active 
Goal: AI proposes a Git-ready directory structure and justifies which templates are critical for this specific research stage. 
Output: Visual tree format + justified list.

## Prompt 4 — Session closure

No attachments needed — context is already active 
Goal: Generate the session's trail: a Zettel Note (ZN) for atomic knowledge and an Automatic Summary (AS) for project tracking. 
Action: Save both to 05-journal/ following the naming convention.

**Session 2+ — Continuing work**

Attach: user-profile.yaml + project-manifest.yaml + last AS 
AI reconstructs full context in seconds "Today I want to work on: [TASK]"

> **Rule:** Attach only what has changed since the last session. The `project-manifest.yaml` is the memory of the project.

---

## Governance

| Item | Detail |
| --- | --- |
| Governance model | RACO / ECSS-M |
| Statement of Work | SOW-TFG-2026-SCP-RACO v1.1 |
| Scope rule | If it is not in the SOW, it is out of scope |
| Confidentiality | CSIC Restricted — signed agreement |
| IP Owner | CSIC — disclosure requires written authorisation |

---

## Requirements

| Requirement | Details |
| --- | --- |
| Git | Version control |
| Obsidian | Recommended editor for Markdown + YAML |
| Python | Optional — automation scripts |
| LaTeX / Marp | Final memory and defence slides |
| AI / LLM | Optional — AI-assisted documentation workflows |

---

## People

| Role | Name | Affiliation |
| --- | --- | --- |
| Student / Author | Sergi Casado Prieto | UAB |
| CSIC Tutor | Esteve Farrés Berenguer | IMB-CNM-CSIC |
| Academic Tutor | Francisco José Fabra Cervellera | UAB |

---

## License

© 2026 IMB-CNM-CSIC & Universitat Autònoma de Barcelona. All rights reserved. See [LICENSE](LICENSE.md) for details.

---

_QL21 · TFG · IMB-CNM-CSIC / UAB · 2026_