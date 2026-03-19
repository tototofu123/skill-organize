---
name: organize-skills
description: Audit and reorganize skills/workflows with totals, type breakdown, and 2-layer or 3-layer taxonomy.
argument-hint: "<objective or scope, optional>"
uses:
  - skill-authoring-workflow
  - skill-master-hub
  - skill-sync-tracker
outputs:
  - docs/skills-main-sub-map.md
  - docs/workflows-main-sub-map.md
  - docs/skills-workflows-cleanup-plan.md
---

# /organize-skills - Global Skill and Workflow Organizer

$ARGUMENTS

---

Run the local workflow at `workflows/organize-skills.md` with the same arguments.

Required behavior:

1. Print inventory first:
   - total skills
   - total workflows
   - combined total
   - global vs local split
   - type breakdown
2. Pick taxonomy mode:
   - 3-layer (`Main -> Sub -> Leaf`) when combined >= 40
   - 2-layer (`Main -> Sub`) when combined < 40
3. Show organization plan before actions.
4. Produce keep/merge/deprecate recommendations.
5. Report reduction metrics (before/after/reduction/%).
6. Update required docs under `docs/`.
7. Print explicit inventory lists (skills/workflows/type buckets), with full lists saved in docs when long.

Return a compact final report with counts, taxonomy depth, and file paths.
