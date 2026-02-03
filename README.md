# Memory Keeper skill

Memory Keeper copies the OpenClaw memory journal files (`memory/*.md`, `MEMORY.md`, plus AGENTS/SOUL/USER/TOOLS/HEARTBEAT) into a dedicated archive folder or repo. Use it when you want to snapshot context before risky operations or ship a clean recovery bundle to another system.

## CLI entry point

```bash
python3 skills/memory-keeper/scripts/memory_sync.py [--workspace /path/to/workspace] [--target /path/to/archive] [--commit --message "msg" --remote https://your.git/repo.git --push]
```

## Key features

- `--skip-memory` avoids the `memory/` directory for small snapshots.
- `--allow-extra` lets you add extra files or glob patterns.
- `--commit` + `--push` let this skill fully manage the git archive if you configure a remote.

## Example

```bash
python3 skills/memory-keeper/scripts/memory_sync.py --target ~/clawdy-memories --commit --message "Nightly sync" --remote https://github.com/CrimsonDevil333333/clawdy-memories.git --push
```
