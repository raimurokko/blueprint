# CLAUDE.md — Project Context for Claude Code (Anthropic)

## Project Overview

<!-- Describe your project in 2-3 sentences -->
_TODO: Add project description._

## Tech Stack

- **Language:** Python 3.12+ / Go 1.22+
- **Frameworks:** <!-- e.g., FastAPI, Click, Cobra -->
- **Database:** <!-- e.g., DuckDB, SQLite, PostgreSQL -->
- **Testing:** pytest / go test

## Project Structure

```
src/          — Source code (Python modules, Go packages)
data/         — Data files (not tracked in git)
  raw/        — Raw/unmodified input data
  processed/  — Transformed/cleaned data
  output/     — Results, exports
docs/         — Documentation
tests/        — Test suite
notebooks/    — Jupyter notebooks (if applicable)
```

## Coding Conventions

- Python: Follow PEP 8, use type hints, format with `ruff`
- Go: Follow `gofmt`, use `go vet`, idiomatic Go patterns
- Commits: Sign off with DCO (`git commit -s`)
- All code must be reviewed by a human before merge

## Important Rules

- **Human-in-the-loop**: All AI-generated code must be reviewed and approved
  by a human developer. See `AI-TRANSPARENCY.md`.
- **No secrets in code**: Use environment variables (`.env`) or `config.yaml`.
  Never commit credentials, API keys, or tokens.
- **Credit AI-generated media**: Any AI-generated images, diagrams, etc.
  must be attributed in `CREDITS.txt`. See `AI-TRANSPARENCY.md` Section 2.3.
- **Privacy first**: Never log PII, file paths, or GPS data.
  Follow DSGVO/GDPR principles.

## Common Commands

```bash
# Python
python -m pytest tests/              # Run tests
ruff check src/                      # Lint
ruff format src/                     # Format

# Go
go test ./...                        # Run tests
go vet ./...                         # Vet
go build ./...                       # Build
```

## Key Files

- `AI-TRANSPARENCY.md` — AI usage disclosure and human-in-the-loop policy
- `CREDITS.txt` — Third-party and AI model credits
- `CONTRIBUTING.md` — How to contribute (DCO required)
- `LICENSE.txt` — MIT License
- `config.yaml.example` — Configuration template
- `.env.example` — Environment variables template
