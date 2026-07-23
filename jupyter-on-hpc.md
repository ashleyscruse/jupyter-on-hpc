---
name: Jupyter on HPC Template
project_type: workshop
domain:
  - career
status: active
started: 2026-01-01
target: ongoing
entities:
  - "[[morehouse]]"
  - "[[mscf]]"
  - "[[tacc]]"
people:
  - "[[scruse-ashley]]"
program: "[[mscf]]"
tags:
  - workshop
  - module
  - template
  - teaching
  - mscf
  - morehouse
  - jupyter
  - hpc
  - reusable
  - no-hard-deadline
---
# Jupyter on HPC Template

Reusable Jupyter-on-HPC guide (step-by-step for running Jupyter Notebook on HPC compute nodes) that other instructors can adopt into their courses. No hard deadline; reused on demand.

**Status:** Active (reusable template, periodic maintenance)

## Quick links
- Lead: [[scruse-ashley]]
- Owner: [[mscf]]
- Public URL: morehouse-supercomputing.github.io/jupyter-on-hpc
- Source repo: github.com/morehouse-supercomputing/jupyter-on-hpc

## Tasks
- [x] Initial guide published ✅ 2026-01-01
- [x] Both methods (SSH + tunnel, TACC Analysis Portal) covered ✅ 2026-01-01
- [ ] Periodic refresh against TACC changes (Vista, Frontera, etc.)
- [ ] Evaluate adopting into [[honeywell-course]] [due:: 2026-07-15]
- [ ] Pull into [[intro-to-hpc]] Session 1 prep materials [due:: 2026-09-01]

## Overview

### Goal
Maintain a reusable Jupyter-on-HPC template (step-by-step guide for running Jupyter Notebook on HPC compute nodes) that other instructors can adopt into their courses. Currently no hard deadline; reused on demand.

### Why this matters
Jupyter on HPC is one of the highest-friction infrastructure tasks for new HPC users (SSH tunnels, idev sessions, the TACC Analysis Portal). Centralizing it as a guide that any instructor can drop into their course removes that friction at scale. Same logic as [[sql-on-hpc]]: build the template once, let instructors adopt rather than rebuild.

### Two methods covered
1. SSH + idev + SSH tunnel (command line)
2. TACC Analysis Portal (web browser)

### Next action
Periodic refresh against TACC changes; decide whether to adopt into the Fall 2026 Honeywell course.

## Live dashboard

### Open tasks
```dataview
TASK
FROM "morehouse/workshops/modules/jupyter-on-hpc"
WHERE !completed AND (
  contains(file.path, "jupyter-on-hpc.md") OR
  contains(string(tags), "#task")
)
GROUP BY file.link
SORT due ASC
```

### Recently completed
```dataview
TASK
FROM "morehouse/workshops/modules/jupyter-on-hpc"
WHERE completed AND (
  contains(file.path, "jupyter-on-hpc.md") OR
  contains(string(tags), "#task")
)
GROUP BY file.link
SORT completion DESC
LIMIT 5
```
