# jsonl-runner

Batch prompt runner with retries and progress

Small but I use it weekly.

## What it does

- Idempotent: skips ids already present in the output
- Concurrent workers with a rate ceiling
- Retries failed items with backoff, logs them aside
- JSONL in, JSONL out: stream-safe for huge inputs

## How to use

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Install

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── dependabot.yml
│   └── pull_request_template.md
├── docs/
│   ├── development.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE
├── Makefile
├── SECURITY.md
├── batch.py
├── prompts.sample.jsonl
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT - see [LICENSE](LICENSE).
