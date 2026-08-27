# Contributing

Contributions are welcome when they keep the project interpretable, auditable, and honest about what event data can measure.

## Start locally

Follow the [README setup](README.md#run-locally), then run:

```bash
.venv/bin/python -m pytest -q
npm --prefix frontend run lint
npm --prefix frontend run build
```

Raw StatsBomb JSON is deliberately not committed. The [offline-analysis instructions](README.md#reproduce-the-offline-analysis) explain how to rebuild the validated outputs.

## Proposing a tactical metric

Open an issue before a large implementation. A proposal should state:

- the exact mathematical formula and denominator;
- the StatsBomb events and fields required;
- exclusions, thresholds, and coordinate/orientation assumptions;
- what high and low values mean as football behaviour;
- why it measures style rather than team quality or execution success;
- important limitations and provider-specific dependencies.

Validate the logic on one match first. Show auditable example events and edge cases, then extend the unchanged definition to a season and verify match coverage before adding it to a fingerprint.

## Pull requests

1. Create a focused branch from `main`.
2. Keep metric logic separate from the runtime application and preserve raw intermediate counts where practical.
3. Add or update tests, documentation, assumptions, and limitations.
4. Run the existing backend tests, frontend lint, and production build.
5. Explain what changed, how it was validated, and whether any processed output intentionally changed.

Avoid mixing a modelling change with unrelated UI or infrastructure work. Never commit API keys, `.env`, `private_notes/`, or `data/raw/`.

By contributing, you agree that your contribution may be distributed under the repository's [MIT License](LICENSE). Provider data remains subject to the [StatsBomb Open Data terms](https://github.com/hudl/open-data).
