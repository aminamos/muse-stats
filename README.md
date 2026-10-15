# muse-stats

Usage statistics for Muse Code, mirroring `omp stats --summary`.
Reads the local session store. No cost estimates: usage is
subscription-covered.

## Usage

```sh
muse-stats            # writes /tmp/muse-stats.html, open it in a browser
muse-stats --serve    # serve it at http://127.0.0.1:8487/muse-stats.html
```

## What it reports

- Sessions count and coverage window from `session-index.db`
- Requests, input/output/cached tokens, cache read/write, avg duration
- Per-model breakdown table

Data source: `~/.local/share/muse` (`session-index.db` plus
per-session `session.jsonl` `model_completed` events).

## License

MIT.
