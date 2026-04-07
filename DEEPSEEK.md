# DEEPSEEK.md — Project Context for DeepSeek Models (深度求索)

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

- **Human-in-the-loop (人机协作)**: All AI-assisted code must be reviewed and
  approved by a human developer. See `AI-TRANSPARENCY.md`.
- **No secrets in code**: Use `.env` or `config.yaml` for credentials.
- **Credit AI-generated media**: Attribute in `CREDITS.txt`.
  Format: `File: path — Model: DeepSeek Coder V2 (DeepSeek / 深度求索)`
- **Privacy**: No PII in logs. DSGVO/GDPR compliant.

## Key Files

| File | Purpose |
|---|---|
| `AI-TRANSPARENCY.md` | AI usage disclosure, human-in-the-loop policy |
| `CREDITS.txt` | Third-party and AI model credits |
| `CONTRIBUTING.md` | Contribution guidelines (DCO) |
| `LICENSE.txt` | MIT License |
