---
description: Show GCF proxy token savings statistics for the current session or overall usage.
---

# GCF Stats

Show the user their gcf-proxy token savings.

Check if `/tmp/gcf-proxy-stats.json` exists and read it. The file contains:
- `calls`: number of tool calls rewritten
- `json_bytes`: total JSON bytes received
- `gcf_bytes`: total GCF bytes sent
- `bytes_saved`: total bytes saved
- `pct_saved`: percentage reduction
- `est_tokens_saved`: estimated tokens saved

Present the stats in a clear format. If the file doesn't exist, explain that gcf-proxy writes stats when running with `--stats-file` and suggest wrapping a server with `/gcf-proxy:setup`.
