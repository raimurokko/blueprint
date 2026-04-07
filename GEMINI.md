# GEMINI.md — Project Context for Google Gemini

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
src/          — Source code
data/         — Data files (not in git)
  raw/        — Raw input data
  processed/  — Transformed data
  output/     — Results, exports
docs/         — Documentation
tests/        — Test suite
notebooks/    — Jupyter notebooks
```

## Coding Conventions

- Python: PEP 8, type hints, format with `ruff`
- Go: `gofmt`, `go vet`, idiomatic patterns
- Commits: DCO sign-off required (`git commit -s`)
- All code must be reviewed by a human before merge

## Important Rules

- **Human-in-the-loop**: All AI-assisted code must be reviewed and approved
  by a human developer before being committed. See `AI-TRANSPARENCY.md`.
- **No secrets in code**: Use `.env` or `config.yaml` for credentials.
- **Credit AI-generated media**: Attribute in `CREDITS.txt`.
  Format: `File: path — Model: Gemini Pro (Google DeepMind)`
- **Privacy**: No PII in logs. DSGVO/GDPR compliant.

## Common Commands

```bash
# Python
python -m pytest tests/
ruff check src/ && ruff format src/

# Go
go test ./... && go vet ./...
```

## Key Files

| File | Purpose |
|---|---|
| `AI-TRANSPARENCY.md` | AI usage disclosure, human-in-the-loop policy |
| `CREDITS.txt` | Third-party and AI model credits |
| `CONTRIBUTING.md` | Contribution guidelines (DCO) |
| `LICENSE.txt` | MIT License |
| `config.yaml.example` | Configuration template |
| `.env.example` | Environment variables template |
