# NxtBar 1.8.0

## Configurable inference servers (all hosts)

- Settings → host → new **Inference Servers** section: add any OpenAI-compatible `/v1/models` endpoint (label + base URL) per host. The app probes each endpoint itself and renders the roster in the popover's Inference section next to aggregator-reported servers — no aggregator changes needed. Works for local and remote hosts alike, including tunneled engines (e.g. this Mac's `127.0.0.1:8000` → Studio oMLX).
- Display-only in v1: no start/stop, no per-endpoint auth (endpoints reuse the host's stored token, same as the Unsloth lane). Engine lifecycle stays with each engine's own mechanism.

## Fixes

- Host config now carries an explicit inference-endpoint list, so features like the Unsloth lane and tunneled-engine rows no longer depend on hand-edited config files.
