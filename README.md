# skill-organize

Portable `organize-skills` workflow spec you can copy into multiple coding assistants.

## File in this repo

- `organize-skill.md`

## One-click install (PowerShell)

Run from the repo root:

```powershell
$src = Join-Path $PWD "organize-skill.md";
New-Item -ItemType Directory -Force -Path "$HOME/.config/opencode/skills/organize-skills" | Out-Null; Copy-Item $src "$HOME/.config/opencode/skills/organize-skills/SKILL.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.claude/skills/organize-skills" | Out-Null; Copy-Item $src "$HOME/.claude/skills/organize-skills/SKILL.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.codex/skills/organize-skills" | Out-Null; Copy-Item $src "$HOME/.codex/skills/organize-skills/SKILL.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.gemini/antigravity/global_workflows" | Out-Null; Copy-Item $src "$HOME/.gemini/antigravity/global_workflows/organize-skills.md" -Force;
New-Item -ItemType Directory -Force -Path "$HOME/.gemini/commands" | Out-Null; Copy-Item $src "$HOME/.gemini/commands/organize-skills.md" -Force;
Write-Host "Installed for OpenCode, Claude, Codex, Antigravity, Gemini"
```

## One-click install (macOS/Linux)

Run from the repo root:

```bash
src="$(pwd)/organize-skill.md" && \
mkdir -p "$HOME/.config/opencode/skills/organize-skills" && cp "$src" "$HOME/.config/opencode/skills/organize-skills/SKILL.md" && \
mkdir -p "$HOME/.claude/skills/organize-skills" && cp "$src" "$HOME/.claude/skills/organize-skills/SKILL.md" && \
mkdir -p "$HOME/.codex/skills/organize-skills" && cp "$src" "$HOME/.codex/skills/organize-skills/SKILL.md" && \
mkdir -p "$HOME/.gemini/antigravity/global_workflows" && cp "$src" "$HOME/.gemini/antigravity/global_workflows/organize-skills.md" && \
mkdir -p "$HOME/.gemini/commands" && cp "$src" "$HOME/.gemini/commands/organize-skills.md" && \
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
