# Claude Code — Project Instructions

## Git Setup

- **GitHub user:** pa0l0s
- **Email:** pawelgr@gmail.com
- **Remote:** git@github.com:pa0l0s/plex-link.git
- **Default branch:** main
- **SSH key:** registered on GitHub — use SSH URLs always (`git@github.com:...`)
- **gh CLI:** not installed — use raw `git` commands only

## Git config (already set in this repo)

```
git config user.name "pa0l0s"
git config user.email "pawelgr@gmail.com"
```

If working in a new repo or worktree, run those two lines before committing.

## Standard workflow

```bash
# Stage specific files (never git add -A blindly)
git add <files>

# Commit with heredoc to preserve formatting
git commit -m "$(cat <<'EOF'
Short summary line

- bullet detail
- bullet detail

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
EOF
)"

# Push
git push
```

## Creating a new repo

1. User creates empty repo on github.com (no README, no .gitignore)
2. User provides SSH URL
3. Then:

```bash
git init
git branch -m main
git config user.name "pa0l0s"
git config user.email "pawelgr@gmail.com"
git add <files>
git commit -m "..."
git remote add origin git@github.com:pa0l0s/<repo>.git
git push -u origin main
```

## Notes

- Do not use `gh` CLI — it is not installed
- Do not use `--no-verify` or force push unless explicitly asked
- Repo is private on GitHub
