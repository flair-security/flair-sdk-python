# flair-sdk-python

flair-sdk-python is the official Python client SDK for the `flair-core` REST API, with sync and async support via `httpx` and full Pydantic v2 models. Like the Go SDK, it's a thin client that tracks the API contract; see the [FLAIR org overview](https://github.com/flair-security/.github) for how it fits in.

**Status:** pre-MVP scaffolding — no Python source yet, and on the roadmap ("future") rather than active development, sequenced after `flair-core`'s API stabilizes.

## Stack

- Python 3.12+
- httpx 0.28+
- pydantic v2

## Getting started

```bash
# Install
pip install -e ".[dev]"

# Unit tests
pytest tests/unit/

# Integration tests (requires a running flair-core instance)
FLAIR_CORE_URL=http://localhost:8080 pytest tests/integration/ -m integration

# Linter + type check
ruff check .
mypy flair_sdk/

# Generate from OpenAPI
openapi-python-client generate --path openapi/flair-core-v1.yaml --config openapi-config.yaml

# Build package
python -m build
```

## Documentation

Docs live in [flair-docs](https://github.com/flair-security/flair-docs) — the docs site itself is still under construction.

## Contributing

See the org-wide [CONTRIBUTING.md](https://github.com/flair-security/.github/blob/main/CONTRIBUTING.md).

## Security

See the org-wide [SECURITY.md](https://github.com/flair-security/.github/blob/main/SECURITY.md) for how to report vulnerabilities.

## License

Apache License 2.0 — see [LICENSE](LICENSE).
