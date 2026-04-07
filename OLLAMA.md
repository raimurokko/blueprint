# OLLAMA.md — Project Context for Local Models via Ollama

This file provides context for AI models running locally through Ollama,
including open-weight models from Meta (Llama), Mistral, and others.

## Project Overview

<!-- Describe your project in 2-3 sentences -->
_TODO: Add project description._

## Tech Stack

- **Language:** Python 3.12+ / Go 1.22+
- **Frameworks:** <!-- e.g., FastAPI, Click, Cobra -->
- **Database:** <!-- e.g., DuckDB, SQLite, PostgreSQL -->
- **Testing:** pytest / go test
- **Local LLM:** Ollama (llama3, mistral, codestral, qwen2.5, deepseek-coder, yi)

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
  Format: `File: path — Model: Llama 3 70B (Meta) via Ollama`
- **Privacy**: No PII in logs. DSGVO/GDPR compliant.
- **Local models**: Data processed locally stays local. Do not send
  sensitive data to external APIs when a local model suffices.

## Common Commands

```bash
# Ollama
ollama list                          # List installed models
ollama run llama3                    # Interactive chat
ollama run codestral                 # Code assistance

# Python
python -m pytest tests/
ruff check src/ && ruff format src/

# Go
go test ./... && go vet ./...
```

## Available Local Models (via Ollama)

| Model | Provider | Best For |
|---|---|---|
| llama3 / llama3.1 | Meta | General purpose, coding |
| codestral | Mistral AI | Code generation, completion |
| mistral / mixtral | Mistral AI | General purpose, reasoning |
| qwen2.5 / qwen2.5-coder | Alibaba (通义千问) | Coding, multilingual |
| deepseek-coder-v2 | DeepSeek (深度求索) | Code generation |
| yi / yi-coder | 01.AI (零一万物) | Coding, general purpose |
| phi3 | Microsoft | Lightweight, fast |
| gemma2 | Google DeepMind | Lightweight, general |
| starcoder2 | BigCode / Hugging Face | Code completion |

## Key Files

| File | Purpose |
|---|---|
| `AI-TRANSPARENCY.md` | AI usage disclosure, human-in-the-loop policy |
| `CREDITS.txt` | Third-party and AI model credits |
| `CONTRIBUTING.md` | Contribution guidelines (DCO) |
| `LICENSE.txt` | MIT License |
