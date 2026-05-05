---
id: D1-state-of-the-art
type: D1
date: 2026-05-05
author: SCP
version: 0.4
status: Draft
project: KM-TFG-QL21
changelog: v0.4 - Finding 5 and key decisions completed
---

# D1: State-of-the-Art Synthesis

## 1. The Reproducibility Crisis
Poor documentation is a primary contributor to the reproducibility crisis in experimental science. In nanoscience, where processes are complex and equipment is expensive, an undocumented parameter change can make an entire run irreproducible. Knowledge is lost when students leave. Procedures cannot be verified without detailed records.

## 2. ELN Solutions
Commercial ELN platforms (Sapio, LabArchives, Benchling) were designed for life sciences. In nanoscience and microfabrication they present significant drawbacks: rigid workflows, high cost, vendor lock-in, and poor Git compatibility.

## 3. FAIR Principles
The FAIR principles (Findable, Accessible, Interoperable, Reusable) provide a well-established framework for evaluating documentation quality. All tool and format decisions in this project are justified against FAIR criteria. Markdown with YAML frontmatter aligned to Schema.org satisfies all four requirements without proprietary dependencies.

## 4. Documentation as Code
The DaC philosophy, as discussed at Write the Docs Berlin 2025, proposes treating documentation with the same rigour as software: version control, structured formats, peer review. This is directly applicable to research documentation and justifies the use of Git, Markdown, and YAML in this framework.

## 5. AI as Collaborator
AI tools reduce documentation friction but do not replace researcher judgement. Confidentiality, hallucination risk, and academic integrity require human oversight at every step. The framework positions AI as an optional Layer 3 that degrades gracefully when unavailable.

## Key Decisions
- Format: Markdown + YAML (open, Git-compatible, FAIR)
- Version control: Git + GitHub
- Reference management: Zotero (open-source, BibTeX)
- Editor: Obsidian (local-first, plain text)
- AI: optional Layer 3, never for scientific content