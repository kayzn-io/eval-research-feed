# kayzn.io AI Agent Evaluation Newsfeed

A weekly feed of notable new research on **evaluating AI agents**: how to measure whether
an agent works, whether the judges scoring it can be trusted, and whether it still works
today.

Curated by [kayzn.io](https://www.kayzn.io). Each entry covers one paper, names the number
the paper reported, and says what it changes for a team running agents in production.

Read it on the web at [kayzn.io/whats-new](https://kayzn.io/whats-new/), or subscribe.

## Subscribe

| Format | URL |
| --- | --- |
| RSS 2.0 | `https://kayzn-io.github.io/eval-research-feed/feed/feed.xml` |
| JSON Feed 1.1 | `https://kayzn-io.github.io/eval-research-feed/feed/feed.json` |

Both carry the most recent entries, newest first.

## Reading it as data

Beyond the two standard feeds there is a plainer JSON shape, and a permanent file per
weekly issue. Everything is served with `Access-Control-Allow-Origin: *`, so it can be
fetched from a browser.

| Path | What it is |
| --- | --- |
| `feed/index.json` | Recent entries, newest first |
| `feed/issues/index.json` | Every issue published, newest first, with its date and headlines |
| `feed/issues/<date>.json` | One weekly issue, complete and permanent |

An entry looks like this:

```json
{
  "id": "doi:10.1007/s44163-026-02012-6",
  "headline": "Confident-looking models can still be quietly wrong",
  "paragraphs": [
    "...",
    "...",
    "..."
  ],
  "paper_title": "Explanation audits reveal silent failures of machine ...",
  "paper_url": "https://doi.org/10.1007/s44163-026-02012-6",
  "paper_published": "2026-08-24",
  "issue_date": "2026-08-27",
  "issue_range": "Aug 21-27, 2026",
  "themes": [
    "evaluation-metrics",
    "production-monitoring",
    "interpretability",
    "reproducibility"
  ]
}
```

`paragraphs` is the entry body, in three parts: the situation, what was measured, and
what it implies. `id` is stable, so it is safe to deduplicate on.

## What is in scope

**Included:** research on agent evaluation, LLM-as-a-judge design and calibration,
reliability and release gating, and production monitoring of agents. Peer-reviewed work
and preprints both.

**Excluded, deliberately:**

- **Vendor and product news of any kind**, including ours. This is research only.
- Leaderboard results with no contribution to how the evaluation itself was done.
- New agent capabilities with no measurement story attached.
- Anything whose only claim to relevance is that it involves an LLM.

Every entry links the paper so you can check it. Where a result is single-seed, or the
judge's agreement with human labels is unreported, the entry says so.

## Corrections

If an entry misreads a paper, open an issue with the entry `id` and what it got wrong.
Corrections are worth more to us than coverage.

## Licence

Entry text is © kayzn.io. Paper titles, author names and findings belong to their authors
and are cited with a link to the original work.
