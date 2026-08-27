# Usage

The README covers the basics. This page collects the
longer examples and the notes that did not fit up front.

## Basic

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Notes

- Retries failed items with backoff, logs them aside
- Concurrent workers with a rate ceiling
