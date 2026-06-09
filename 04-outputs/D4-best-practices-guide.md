---
id: D4-best-practices-guide
type: GDE
date: 2026-06-03
author: SCP
project: KM-TFG-QL21
version: 1.0
status: Final
changelog: "v1.0 2026-06-03 Initial release"
---

# The 21st Century Lab Notebook
## Guide of Best Practices for Research Documentation

> A practical guide for students and researchers entering
> a laboratory for the first time. No prior knowledge of
> Git, YAML, or documentation theory required.

**Version:** 1.0
**Author:** Sergi Casado Prieto — IMB-CNM-CSIC / UAB
**Date:** June 2026
**Repository:** https://github.com/sergicasadoprieto-ctrl/tfg-quadern-laboratori-21c

---

## Who is this guide for?

This guide is for you if:

- You are starting a new research project and have no
  documentation system in place
- You have been using paper notebooks or Word documents
  and want something better
- You want your work to be reproducible, searchable,
  and traceable without spending hours on formatting
- You want to use AI tools to help with documentation
  without losing control of your data

You do not need to know Git, YAML, or any programming
language to use this framework. Everything in this
guide uses free, open-source tools that run on any
operating system.

---

## What this guide covers

1. Why documentation matters
2. The tools you need
3. How to start a new project
4. How to document day-to-day
5. How to use AI assistance (optional)
6. How to maintain the repository
7. Project closure checklist

---

---

## 1. Why Documentation Matters

### The problem

You finish a six-month project. Six months later,
a colleague asks you to reproduce one of your
results. You open your notes and find:

- A folder called `final_result_v2_NEW_fixed`
- A paper notebook with handwriting you can barely
  read
- An email chain with parameters scattered across
  twelve messages
- A Word document with no dates, no version history,
  and no explanation of why you made the decisions
  you made

This is not an unusual situation. It is the default.
And it has real consequences.

### The reproducibility crisis

Experimental science has a documentation problem.
Studies across disciplines consistently show that
a significant proportion of published results cannot
be reproduced, often because the original
experimental conditions were never properly recorded.

The cost is not just academic. In a nanofabrication
environment, a single undocumented change in a
process parameter, furnace temperature, photoresist
concentration, spin speed, can propagate through
an entire fabrication run without anyone knowing
when or why it was introduced. Months of work and
thousands of euros of materials can be lost because
one parameter was not written down.

### What good documentation looks like

Good documentation is not about writing more. It is
about writing the right things in the right place,
consistently, from day one.

A well-documented project has:

- A clear record of what was done, when, and by whom
- The reasoning behind every significant decision
- All experimental parameters, not just the ones
  that worked
- A version history that shows how the project
  evolved
- A structure that anyone can navigate without
  asking you for help

### The cost of starting late

Documentation is one of those things that is easy
to defer and very expensive to reconstruct. Every
day you wait, the cost of catching up increases.
Parameters you remember today will be gone in two
weeks. Context that seems obvious now will be
opaque in six months.

The single most effective thing you can do is
start on day one, with a structure already in
place, so that documentation is part of the
workflow rather than an addition to it.

That is what this framework is designed to make
possible.

---
---

## 2. The Tools You Need

All tools in this framework are free. None require
a subscription. All run on Windows, Mac, and Linux.

### Required

**Git** — version control system
- What it does: tracks every change you make to
  every file, forever
- Why you need it: without Git, you have no version
  history, no audit trail, and no way to recover
  a previous version of your work
- Download: https://git-scm.com/downloads
- Time to install: 5 minutes

**GitHub** — remote repository hosting
- What it does: stores your repository online,
  makes it accessible to your team, and protects
  against data loss
- Why you need it: your local Git repository is
  only on your computer. GitHub is the backup and
  the collaboration layer.
- Create a free account: https://github.com
- Note: GitHub is owned by Microsoft and is not
  open-source. If your institution has strict data
  sovereignty requirements, GitLab or Gitea on an
  institutional server are equivalent alternatives.

### Recommended

**Obsidian** — plain text editor and knowledge manager
- What it does: lets you write Markdown files with
  YAML frontmatter, visualise connections between
  notes as a knowledge graph, and search across
  your entire vault instantly
- Why you need it: Obsidian is the best editor for
  the QL21 workflow. It validates YAML frontmatter
  automatically, renders Markdown in real time, and
  supports wikilinks between notes.
- Download: https://obsidian.md
- Note: Obsidian is not open-source but is free
  for personal and academic use.
- Time to install: 5 minutes

**Zotero** — reference manager
- What it does: builds a structured database of
  papers, equipment manuals, and technical references.
  Exports references in BibTeX format for use in
  LaTeX.
- Why you need it: if you are writing a thesis or
  paper, Zotero saves hours of manual reference
  formatting. The browser connector captures
  metadata automatically with one click.
- Download: https://www.zotero.org
- Time to install: 5 minutes

### Optional

**GitHub Desktop** — graphical Git interface
- What it does: lets you commit, push, and pull
  without using the command line
- Why you might need it: if you have no prior Git
  experience, GitHub Desktop removes the biggest
  barrier to adoption
- Download: https://desktop.github.com

**Ollama** — local AI model runner
- What it does: runs AI language models locally
  on your computer, without sending data to
  external servers
- Why you might need it: if your institution has
  confidentiality requirements that prevent the
  use of cloud AI services, Ollama provides
  equivalent functionality with full data
  sovereignty
- Download: https://ollama.com

### What you do not need

- A subscription to any service
- A powerful computer (Markdown and Git run on
  any hardware)
- Programming knowledge (the framework works with
  plain text files)
- An internet connection to write documentation
  (Git works offline; push when you have connectivity)

---

---

## 3. How to Start a New Project

This section walks you through the complete setup
of a new project from scratch. Follow the steps
in order. The whole process takes about 30 minutes
the first time and less than 10 minutes for every
project after that.

### Step 1: Create the repository on GitHub

1. Go to https://github.com and log in
2. Click **New repository**
3. Name it following your project acronym,
   for example: `my-project-2026`
4. Set it to **Public** or **Private** depending
   on your institution's policy
5. Do NOT add a README, .gitignore, or licence
   (you will create these manually)
6. Click **Create repository**
7. Copy the repository URL shown on the next page

### Step 2: Clone the repository locally

Open a terminal (or GitHub Desktop) and run:

```bash
git clone https://github.com/username/my-project-2026.git
cd my-project-2026
```

### Step 3: Create the folder structure

```bash
mkdir 00-governance
mkdir 01-literature
mkdir 02-framework
mkdir 03-pilot
mkdir 04-outputs
mkdir 05-journal
```

Each folder has a specific purpose:

| Folder | Purpose |
|--------|---------|
| 00-governance | Manifests, SOW, confidentiality agreements |
| 01-literature | Papers, notes, references.bib |
| 02-framework | Templates and naming convention |
| 03-pilot | Laboratory logs, ZN notes, reports |
| 04-outputs | Final deliverables |
| 05-journal | Personal notes, session summaries |

### Step 4: Copy the templates

Copy the four core templates from the QL21 kit
to `02-framework/templates/`:

TPL-LOG.md → Laboratory log TPL-ZN.md → Zettel Note TPL-RPT.md → Weekly report TPL-PROJ.md → Project initialisation

### Step 5: Fill in the governance manifests

Copy the three manifests from the QL21 kit to
`00-governance/` and fill in the following fields:

**user-profile.yaml**
```yaml
name: "Your Full Name"
acronym: "YFN"
jobTitle: "Your role"
worksFor:
  name: "Your institution"
projectContext:
  name: "Your project name"
  startDate: "YYYY-MM-DD"
  supervisor:
    name: "Supervisor name"
    affiliation: "Institution"
```

**project-manifest.yaml**
```yaml
name: "Project full name"
acronym: "PROJECT-ACRONYM"
description: >
  One paragraph describing what this project is
  about and what problem it addresses.
governance:
  statementOfWork: "SOW-filename"
  scopeRule: "If it is not in the SOW, it is out of scope."
```

**branding-manifest.yaml** (optional)
Fill in your preferred colours and fonts, or
leave the QL21 defaults as they are.

### Step 6: Create the README and CHANGELOG

**README.md** — minimum content:
```markdown
# Project Name

Short description of the project.

## People
- Student: Your name
- Supervisor: Supervisor name
- Institution: Your institution

## Structure
Standard QL21 folder structure.
```

**CHANGELOG.md** — minimum content:
```markdown
# Changelog

## [0.1.0] — YYYY-MM-DD

### Added
- Initial repository structure
- Governance manifests v1.0
- Core templates
```

### Step 7: First commit

```bash
git add .
git commit -m "feat: initialise project structure v0.1.0"
git push -u origin main
```

Your project is now set up. From this point, every
session follows the daily workflow described in
Section 4.

---

---

## 4. How to Document Day-to-Day

This section describes the daily workflow. Follow
this pattern for every session, every day.

### Before the session

Open the last entry in your CHANGELOG or the last
AS file in `05-journal/`. Read it. This reconstructs
the context of where you left off without having to
open any other file.

If you are using AI assistance, load the three
governance manifests and the last AS file before
starting. See Section 5 for details.

### During the session: the LOG file

Every laboratory session, coding session, or
significant work block gets a LOG file. Create one
by copying `TPL-LOG.md` to `03-pilot/logs/` and
renaming it following the naming convention:

LOG-{YYYYMMDD}T{HHmmss}-{YOUR_ACRONYM}-1.00.md

Example:

LOG-20260114T090000-ABC-1.00.md

Fill in the YAML frontmatter first:

```yaml
---
id: LOG-20260114T090000-ABC-1.00
type: LOG
date: 2026-01-14
author: ABC
project: MY-PROJECT
status: Draft
---
```

Then write the body of the log following the
six sections:

**1. Objective**
One sentence. What did you want to achieve today?

**2. Activity**
What did you do, step by step? Be specific.
Include equipment names, parameter values,
sample IDs, and software versions. Do not
summarise. Write it as you would tell a
colleague who needs to repeat the exact same
procedure tomorrow.

**3. Observations**
What did you see? Include unexpected results,
anomalies, and anything that surprised you.
Do not interpret yet. Just record.

**4. Decisions**
What decisions did you make and why? What
alternatives did you consider? This section
is the most valuable one for future you.
In six months, you will not remember why you
chose one approach over another. Write it down.

**5. Next Steps**
What needs to happen before the next session?
Be specific and actionable.

**6. References**
Links to related LOG files, ZN notes, or
external sources.

### When you have an insight: the ZN file

A Zettel Note captures one idea, observation,
or insight. It is not a log of what you did.
It is an atomic unit of knowledge that can
connect to other notes and grow over time.

Create a ZN file by copying `TPL-ZN.md` to
`05-journal/` and renaming it:

ZN-{YYYYMMDD}T{HHmmss}-{YOUR_ACRONYM}-1.00.md

The rule is: one ZN, one idea. If you need to
write about two ideas, create two ZN files.
This keeps each note focused and searchable.

Good candidates for a ZN:

- An unexpected result that needs further
  investigation
- A concept from a paper that is relevant
  to your project
- A decision you made and the reasoning
  behind it
- A connection between two things you had
  not noticed before

### At the end of the week: the RPT file

Every week, create a weekly report by copying
`TPL-RPT.md` to `03-pilot/` and renaming it:

RPT-{YYYYMMDD}T{HHmmss}-{YOUR_ACRONYM}-1.00.md

Fill in the six sections:

1. **BLUF** — one paragraph summarising the week.
   Write this last.
2. **Completed this week** — what did you finish?
3. **In progress** — what are you working on?
4. **Blockers** — what is stopping you?
5. **Decisions made** — what was decided and why?
6. **Next week** — what are your priorities?

The RPT is not a diary. It is a structured record
that anyone on the team can read and understand
without asking you questions.

### After the session: commit to Git

Every session ends with a commit. No exceptions.

```bash
git add .
git commit -m "docs: add LOG session 2026-01-14"
git push
```

Follow the Conventional Commits convention for
commit messages:

| Prefix | Use for |
|--------|---------|
| feat | New artefact or template |
| docs | Log, note, or report entry |
| fix | Correction to an existing file |
| chore | Repository maintenance |
| refactor | Renaming or restructuring |

### Update the CHANGELOG

At the end of each significant session or week,
add an entry to `CHANGELOG.md`:

```markdown
## [0.1.X] — YYYY-MM-DD

### Added
- LOG-20260114T090000-ABC-1.00.md: session description

### Changed
- Updated project-manifest with new deliverable
```

The CHANGELOG is your project diary at the macro
level. The LOG files are your project diary at the
micro level. Together they give you complete
traceability at any scale.

### The naming convention

All files follow this pattern:

{PREFIX}-{YYYYMMDD}T{HHmmss}-{AUTHOR}-{VERSION}.md

| Prefix | Document type |
|--------|---------------|
| LOG | Laboratory log |
| ZN | Zettel Note |
| RPT | Weekly report |
| PROJ | Project document |
| TPL | Template |
| SOW | Statement of Work |
| AS | Automatic Summary |

The timestamp ensures files sort chronologically
in any file system. The author acronym makes
attribution unambiguous. The version number
tracks document evolution.

---

---

## 5. How to Use AI Assistance (Optional)

This section is optional. The framework works
completely without AI. Read Section 3 and 4 first
and make sure your project is already set up before
using AI assistance.

### Before you start: what AI needs

AI tools have no memory between sessions. Every
time you start a new conversation, the AI starts
from zero. To reconstruct context, you need to
attach the following files manually at the start
of every session:

**Always attach:**
- `00-governance/user-profile.yaml`
- `00-governance/project-manifest.yaml`

**Also attach if available:**
- The last AS file from `05-journal/`
- The last RPT file from `03-pilot/`

Without these files, the AI cannot know who you
are, what your project is, or what you did last
session. With them, context is reconstructed
in seconds.

### Choose your AI tool

Any AI assistant works with this framework.
The choice depends on your confidentiality
requirements:

| Tool | Data goes to | Best for |
|------|-------------|---------|
| ChatGPT / Claude | External servers | General use |
| Microsoft Copilot | Microsoft servers | Office 365 environments |
| Ollama (local) | Your computer only | Confidential research |

If your institution has restrictions on sharing
data with external services, use Ollama with a
local model. See https://ollama.com for setup
instructions.

### Session 1: Project Initialisation

Use these prompts in order when starting a new
project. Each prompt builds on the context
established by the previous one.

**Prompt 1 — Generate the SOW**

Attached: project-offer.pdf + TPL-PROJ.md

Generate a Statement of Work from the attached project offer. Fill in all fields you can extract directly from the document. Leave unknown fields as [FILL]. Do not invent any data. Output in Markdown.

**Prompt 2 — Generate the project manifest**

Attached: SOW (already in context) + user-profile.yaml

Generate the project manifest for this project. Use the SOW already in context and my user profile to fill in the fields. Output strictly in YAML. Do not add fields that are not in the template. Leave unknown fields as [FILL].

**Prompt 3 — Repository structure**

No attachments needed. Context is already active.

Propose a Git repository structure for this project following the QL21 standard (00-governance to 05-journal). Justify any additions specific to this project type. Output as a visual tree.

**Prompt 4 — Session closure**

No attachments needed. Context is already active.

Generate the session closure artefacts:

1. A Zettel Note (ZN) capturing the key insight from this session. One idea only.
2. An Automatic Summary (AS) for project tracking, covering what was done, what was decided, and what comes next.

Save both to 05-journal/ following the naming convention.

### Session 2+: Continuing Work

From the second session onwards, attach only
what has changed since the last session.

Attached: user-profile.yaml + project-manifest.yaml + last AS from 05-journal/

Today I want to work on: [DESCRIBE YOUR TASK]

### What AI should never do

AI assistance is for structure and formatting only.
Never ask AI to:

- Record experimental observations on your behalf
- Interpret results or draw conclusions
- Write scientific content that requires judgement
- Generate data or parameters you have not measured

The boundary is clear: if it happened in the lab,
you write it. If it needs to be structured or
formatted, AI can help.

### A note on confidentiality

Each researcher and institution has different
policies regarding what can be shared with external
AI services. Before using any cloud-based AI tool,
check the data sharing policy of your institution.
For environments with strict data sovereignty
requirements, locally hosted AI models such as
Ollama provide equivalent functionality without
sending data to external servers.

---

---

## 6. How to Maintain the Repository

A repository that is not maintained becomes a
liability. This section describes the habits that
keep it useful over time.

### Commit frequency

Commit after every session. No exceptions. A commit
takes less than thirty seconds and creates a permanent
record of what you did. If you wait until the end
of the week, you will forget what changed and why.

A good commit message answers three questions:
- What changed? (the prefix: feat, docs, fix)
- What is it? (the subject: the file or component)
- Why? (optional but valuable for significant changes)

```bash
# Good commit messages
git commit -m "docs: add LOG photolithography session WAF-2026-003"
git commit -m "feat: add ZN diagonal loading insight"
git commit -m "fix: correct YAML indentation in project-manifest"
git commit -m "chore: update CHANGELOG to v0.1.5"

# Bad commit messages
git commit -m "update"
git commit -m "changes"
git commit -m "fix stuff"
```

### CHANGELOG maintenance

Update the CHANGELOG at the end of every significant
session or week. The CHANGELOG is not a Git log —
it is a human-readable summary of what happened and
why.

Structure every entry with three sections:

```markdown
## [0.1.X] — YYYY-MM-DD

### Added
- New files or artefacts created this session

### Changed
- Existing files modified and why

### Fixed
- Errors corrected
```

Keep entries short and specific. The CHANGELOG
should be readable in two minutes and give anyone
a complete picture of the project status.

### README maintenance

Update the README whenever the project status
changes significantly. The README is the first
thing anyone sees when they open the repository.
It should always reflect the current state, not
the initial plan.

At minimum, update:
- The deliverables table with current status
- The phase badge if the project has moved to
  a new phase
- Any new tools or dependencies added

### Naming convention discipline

Never rename a file after it has been committed.
If a file was committed with the wrong name, create
a new file with the correct name, copy the content,
and commit it as a correction. Do not use
`git mv` to rename committed files unless you
are confident about what you are doing.

If you find yourself creating files with similar
names because you are not sure which convention
to follow, stop and re-read Section 4. The naming
convention is fixed. There is no room for
interpretation.

### Version control for manifests

Governance manifests are versioned documents.
When you make a significant change to a manifest,
update the version number in the filename and
in the manifest header:

sergi-casado-profile-1.0.yaml → sergi-casado-profile-1.1.yaml

Keep the old version in the repository. Do not
delete it. The version history of the manifests
is part of the project record.

### GitHub Pages deployment

If you want to make your documentation accessible
from any device without requiring Git knowledge,
enable GitHub Pages:

1. Go to your repository on GitHub
2. Settings → Pages
3. Source: Deploy from a branch
4. Branch: main / root
5. Save

Your repository will be published at:

https://username.github.io/repository-name/

This makes the latest logs and reports accessible
from a tablet inside the lab without needing to
open a terminal.

### Backup strategy

GitHub is your primary backup. But GitHub going
down, or your account being suspended, would
leave you without access to your repository.

Two additional backups recommended:

1. **Local backup**: your working directory on
   your computer is already a full copy of the
   repository. Keep it.

2. **Cloud backup**: sync your local working
   directory to Google Drive, OneDrive, or any
   cloud storage service. This does not affect
   how Git works. The files remain plain text
   and fully editable offline.

---

## 7. Project Closure Checklist

Use this checklist when a project is complete,
when you are leaving a research group, or when
you are handing the project to a new researcher.
A closed project should be in a state where anyone
can open it, understand it, and continue it without
asking you a single question.

### Documentation checklist

- [ ] All LOG files are complete and committed.
      No session without a log.
- [ ] All ZN notes are linked to the relevant
      LOG files in their references field.
- [ ] All RPT files cover the complete project
      duration with no gaps.
- [ ] The CHANGELOG reflects every significant
      version from v0.1.0 to the final version.
- [ ] The README is up to date and reflects the
      final project status.
- [ ] All deliverables in the README table are
      marked as Complete or archived.

### Governance checklist

- [ ] The project manifest is updated with the
      actual end date and final status.
- [ ] The user profile reflects the tools and
      knowledge domains acquired during the project.
- [ ] The SOW is archived with a note indicating
      whether all objectives were met and which
      were not.
- [ ] Any deviations from the original scope are
      documented in the CHANGELOG or a dedicated
      ZN note.

### Repository checklist

- [ ] All files follow the naming convention.
      No exceptions.
- [ ] No binary files committed except figures
      and PDFs that are explicitly referenced.
- [ ] The .gitignore excludes OS files, editor
      configuration files, and any temporary files.
- [ ] The final commit message is clear and
      descriptive.
- [ ] The repository has been pushed to GitHub
      and is accessible from the remote URL in
      the project manifest.

### Knowledge transfer checklist

- [ ] A final AS (Automatic Summary) has been
      written covering the complete project:
      what was done, what worked, what did not,
      and what the next researcher should know
      before starting.
- [ ] All friction points and lessons learned
      are documented in the final RPT or a
      dedicated ZN note.
- [ ] Any institutional knowledge that is not
      in the logs, such as equipment quirks,
      supplier contacts, or undocumented
      procedures, has been written down.
- [ ] The repository URL has been shared with
      the supervisor and any future researchers
      who will continue this work.

### Final commit

```bash
git add .
git commit -m "chore: project closure - final commit"
git push
```

### Archival

After the final commit, tag the repository with
the project version:

```bash
git tag -a v1.0.0 -m "Project closure: final version"
git push origin v1.0.0
```

This creates a permanent, citable snapshot of
the repository at the moment of closure.

---

## Quick Reference Card

| Action | Command or file |
|--------|----------------|
| New session | Copy TPL-LOG.md, rename, fill in |
| New insight | Copy TPL-ZN.md, rename, fill in |
| End of week | Copy TPL-RPT.md, rename, fill in |
| Commit | git add . && git commit -m "..." |
| Push | git push |
| Update CHANGELOG | Edit CHANGELOG.md, add new entry |
| Reconstruct context | Read last CHANGELOG entry + last AS |
| Find a file | grep -r "search term" . |

---

## Troubleshooting

**YAML parsing error in Obsidian**
Check for missing spaces after colons, tab
indentation, or unquoted special characters.
See Annex L of the TFG memory for a complete
YAML syntax reference.

**Git push rejected**
Run git pull first to integrate remote changes,
then push again.

**File not found after renaming**
Never rename committed files outside of Git.
Use git mv to rename, or create a new file
and commit the old one as deleted.

**AI lost context mid-session**
Reload the governance manifests and the last
AS file. This reconstructs full context in
seconds.

**Obsidian not showing YAML as properties**
Go to Settings → Editor → Properties in document
and set to Visible.

---

*QL21 · TFG · IMB-CNM-CSIC / UAB · 2026*
*Repository: https://github.com/sergicasadoprieto-ctrl/tfg-quadern-laboratori-21c*