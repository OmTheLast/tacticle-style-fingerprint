# Tactical Style Fingerprint launch kit

Draft material only. Nothing in this file has been posted. Replace the marked placeholders with your own voice before publishing, and do not present the model's output as universal tactical truth.

Core factual hook:

> I processed all 380 matches of the 2015/16 Premier League to build five-dimensional tactical fingerprints. One result: Liverpool and Tottenham were the closest tactical pair in the model.

Links:

- Live demo: https://tactical-style-fingerprint.vercel.app
- Repository: https://github.com/OmTheLast/tactical-style-fingerprint

## LinkedIn — technical but accessible

`[OM: ADD PERSONAL INTRO—WHY THIS QUESTION INTERESTED YOU.]`

I built Tactical Style Fingerprint, an interpretable football analytics project using StatsBomb event data from all 380 matches of the 2015/16 Premier League.

Instead of labelling teams as simply “possession” or “counterattacking,” the system represents each team across five calculated dimensions: attacking territory, pass verticality, pressing intensity, attacking width, and counterattacking tendency. Population z-scores make the different units comparable, and Euclidean distance finds the nearest tactical profiles.

One result: Liverpool and Tottenham Hotspur are the closest pair in this model at distance `0.620`. They are especially close across territory, verticality, pressing, and width, with a larger difference in counterattacking tendency.

The similarity engine is deterministic—the LLM does not choose the matches. Featherless/Qwen receives the calculated values and limitations and explains why two teams are close or different.

`[OM: ADD ONE THING YOU LEARNED WHILE DEFINING OR VALIDATING THE METRICS.]`

Live demo: https://tactical-style-fingerprint.vercel.app

Code and methodology: https://github.com/OmTheLast/tactical-style-fingerprint

## X / Twitter — short and result-driven

`[OM: ADD YOUR OWN OPENING PHRASE.]`

I turned event data from all 380 matches of the 2015/16 Premier League into five-dimensional tactical fingerprints.

Closest pair in the model: Liverpool ↔ Tottenham — distance `0.620`.

The similarity is calculated with transparent metrics + z-scored Euclidean distance. The LLM only explains the evidence.

Demo: https://tactical-style-fingerprint.vercel.app

Code: https://github.com/OmTheLast/tactical-style-fingerprint

## Reddit / football analytics community — methodology first

**Possible title:** I built five-dimensional tactical fingerprints from the 2015/16 Premier League's StatsBomb event data

`[OM: ADD A BRIEF NON-PROMOTIONAL INTRO AND THE COMMUNITY YOU ARE POSTING TO.]`

I wanted to test whether team style could be represented with a small set of defensible event-data proxies rather than broad labels. I calculated five season-level features for all 20 teams:

1. completed passing share from the final third;
2. distance-weighted attempted-pass verticality;
3. high-zone pressures per 100 opposition passes;
4. width of final-third Pass/Carry destinations;
5. StatsBomb From-Counter possessions per 100 eligible possession changes.

I standardized each feature across the league and used equal-weight Euclidean distance. Liverpool–Tottenham is the closest pair at `0.620`; Leicester's lower territory but league-high verticality and counter rate produces a very different profile.

There are important caveats: Territory and Verticality correlate at `-0.839`, Width is sensitive after standardization, From Counter is a provider label, and event data cannot observe true team shape or off-ball width. The repository keeps those limitations visible.

`[OM: ADD THE SPECIFIC KIND OF FEEDBACK YOU WANT—METRIC DEFINITIONS, NORMALIZATION, OR VISUALIZATION.]`

Methodology/code: https://github.com/OmTheLast/tactical-style-fingerprint

Demo: https://tactical-style-fingerprint.vercel.app

## Hacker News / Show HN — architecture and trade-offs

**Possible title:** Show HN: Interpretable tactical similarity from 380 Premier League matches

`[OM: ADD A SHORT PERSONAL MOTIVATION.]`

I built an interpretable tactical-similarity engine for the 2015/16 Premier League using StatsBomb Open Data.

The offline Python/pandas pipeline derives five season-level metrics, standardizes them across the 20-team population, and calculates every pairwise Euclidean distance. Validated CSV outputs are versioned and served by FastAPI; a Next.js interface renders fingerprints, neighbours, and feature-level differences.

The AI layer is deliberately downstream. Featherless/Qwen receives the already-calculated comparison, definitions, and limitations, and generates a grounded explanation. It does not calculate metrics or select similar teams.

One result is Liverpool–Tottenham at distance `0.620`, the closest pair in the model. The main limitations are disclosed in the interface and README, including correlated features, Width sensitivity, provider-defined counter annotations, and the inability of event data to measure off-ball structure.

`[OM: ADD WHAT YOU WOULD MOST LIKE TECHNICAL FEEDBACK ON.]`

Demo: https://tactical-style-fingerprint.vercel.app

Repository: https://github.com/OmTheLast/tactical-style-fingerprint

## Before publishing anything

- Replace every `[OM: ...]` placeholder.
- Check that the live demo is awake and healthy.
- Keep “distance” as distance; do not rewrite it as a percentage or probability.
- Say “within this five-feature 2015/16 model,” not “these teams were objectively identical.”
- Mention at least one modelling limitation in longer posts.
- Adjust wording to the norms of the specific community; do not cross-post identical copy everywhere.
