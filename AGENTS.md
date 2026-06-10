# AGENTS.md

Guidance for AI agents working in this repository.

## Repository overview

This is a **GitHub profile README** repository (`AleksandrWeber/AleksandrWeber`). It contains a single tracked file, `README.md`, which GitHub renders on the owner's profile page.

There is **no application source code**, build system, test suite, or package manager configuration in this repo.

## Cursor Cloud specific instructions

### Services

| Service | Required | Notes |
|---------|----------|-------|
| *(none)* | — | No servers, databases, or containers are part of this repository |

### Development workflow

1. Edit `README.md`.
2. Commit and push to `main` (or open a PR).
3. GitHub renders the markdown on the profile automatically.

### Local preview (optional)

To preview how the README renders without pushing:

```bash
pip install --user markdown
python3 - <<'PY'
import markdown
from pathlib import Path
readme = Path("README.md").read_text()
html = f"<!DOCTYPE html><html><body>{markdown.markdown(readme)}</body></html>"
Path("/tmp/profile-readme-preview/index.html").write_text(html)
PY
mkdir -p /tmp/profile-readme-preview
python3 -m http.server 8765 --directory /tmp/profile-readme-preview
```

Then open `http://127.0.0.1:8765/` in a browser.

### Lint / test / build

| Task | Command | Status |
|------|---------|--------|
| Lint | N/A | No linter configured |
| Test | N/A | No test suite |
| Build | N/A | No build step |

### Environment variables

None required for this repository.

### External projects mentioned in README

The README references separate projects (Figmatic, VSCode Voicey) that live in other repositories. They are not part of this workspace.
