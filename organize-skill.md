---
name: organize-skills
description: Audit and reorganize skills and workflows with inventory totals, taxonomy, and cleanup recommendations.
argument-hint: "<objective or scope, optional>"
outputs:
  - docs/skills-main-sub-map.md
  - docs/workflows-main-sub-map.md
  - docs/skills-workflows-cleanup-plan.md
---

# Organize Skills and Workflows

Use this workflow to audit and reorganize skill and workflow libraries into a clear taxonomy with measurable cleanup outcomes.

## Inputs

- User objective and scope (optional)
- Global and local skill/workflow directories

## Required Behavior

1. Print inventory first:
   - total skills
   - total workflows
   - combined total
   - global vs local split
   - type breakdown
2. Pick taxonomy depth:
   - `Main -> Sub -> Leaf` when combined total >= 40
   - `Main -> Sub` when combined total < 40
3. Show the organization plan before making actions.
4. Produce keep/merge/deprecate recommendations.
5. Report reduction metrics:
   - before
   - after
   - reduction
   - reduction percentage
6. Update documentation outputs under `docs/`.
7. Print explicit inventory lists (skills/workflows/type buckets).
   - If lists are long, keep full lists in docs and return a compact console report.

## Output Contract

Return a compact final report with:

- inventory counts
- taxonomy depth selected
- file paths of updated outputs

## Suggested Execution Steps

1. Discover all skills and workflows in scope.
2. Count and classify by source (global/local) and type.
3. Select taxonomy mode based on total count.
4. Draft main/sub(/leaf) mapping.
5. Mark items as keep, merge, or deprecate with rationale.
6. Estimate and report consolidation impact.
7. Write docs and provide final summary.
