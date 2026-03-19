# skill-organize

Portable `organize-skills` assets for skill and workflow driven assistants.

This repo now includes both forms:

- `organize-skill.md` (skill spec)
- `organize-workflow.md` (workflow/command spec)

## What it can do

The `organize-skills` package is designed to clean up and standardize large skill/workflow libraries.

- Build a full inventory first (skills, workflows, combined total).
- Split inventory by scope/source (global vs local).
- Produce a type breakdown to reveal overlap and clutter.
- Select taxonomy depth automatically:
  - `Main -> Sub -> Leaf` for larger libraries (>= 40 combined).
  - `Main -> Sub` for smaller libraries (< 40 combined).
- Propose keep/merge/deprecate actions before changes.
- Report reduction metrics (before, after, reduction, percentage).
- Generate docs artifacts for maintainers:
  - `docs/skills-main-sub-map.md`
  - `docs/workflows-main-sub-map.md`
  - `docs/skills-workflows-cleanup-plan.md`

## Skill vs Workflow

- **Skill file** is for assistants that load skills from `SKILL.md` conventions.
- **Workflow file** is for command/workflow runners (including Antigravity command style).

If you want compatibility across tools, install both.

## One-click install (PowerShell)

Run from the repo root:

```powershell
$skill = Join-Path $PWD "organize-skill.md";
$workflow = Join-Path $PWD "organize-workflow.md";
New-Item -ItemType Directory -Force -Path "$HOME/.config/opencode/skills/organize-skills" | Out-Null; Copy-Item $skill "$HOME/.config/opencode/skills/organize-skills/SKILL.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.claude/skills/organize-skills" | Out-Null; Copy-Item $skill "$HOME/.claude/skills/organize-skills/SKILL.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.codex/skills/organize-skills" | Out-Null; Copy-Item $skill "$HOME/.codex/skills/organize-skills/SKILL.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.gemini/antigravity/global_workflows" | Out-Null; Copy-Item $workflow "$HOME/.gemini/antigravity/global_workflows/organize-skills.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.gemini/commands" | Out-Null; Copy-Item $workflow "$HOME/.gemini/commands/organize-skills.md" -Force;
Write-Host "Installed for OpenCode, Claude, Codex, Antigravity, Gemini"
```

## One-click install (macOS/Linux)

Run from the repo root:

```bash
skill="$(pwd)/organize-skill.md" && workflow="$(pwd)/organize-workflow.md" && \
mkdir -p "$HOME/.config/opencode/skills/organize-skills" && cp "$skill" "$HOME/.config/opencode/skills/organize-skills/SKILL.md" && \
mkdir -p "$HOME/.claude/skills/organize-skills" && cp "$skill" "$HOME/.claude/skills/organize-skills/SKILL.md" && \
mkdir -p "$HOME/.codex/skills/organize-skills" && cp "$skill" "$HOME/.codex/skills/organize-skills/SKILL.md" && \
mkdir -p "$HOME/.gemini/antigravity/global_workflows" && cp "$workflow" "$HOME/.gemini/antigravity/global_workflows/organize-skills.md" && \
mkdir -p "$HOME/.gemini/commands" && cp "$workflow" "$HOME/.gemini/commands/organize-skills.md" && \
echo "Installed for OpenCode, Claude, Codex, Antigravity, Gemini"
```

## LLM CLI install

```bash
python -m pip install -U llm
llm --version
```

## Verify paths

- OpenCode: `~/.config/opencode/skills/organize-skills/SKILL.md`
- Claude: `~/.claude/skills/organize-skills/SKILL.md`
- Codex: `~/.codex/skills/organize-skills/SKILL.md`
- Antigravity: `~/.gemini/antigravity/global_workflows/organize-skills.md`
- Gemini: `~/.gemini/commands/organize-skills.md`

## Current status in this repo

- Skill present: `organize-skill.md`
- Workflow present: `organize-workflow.md`
- Result: both are available.
