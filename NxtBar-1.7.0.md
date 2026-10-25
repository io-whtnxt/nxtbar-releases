# NxtBar 1.7.0

## Inference providers (Mac Studio)

- New Inference section in the Studio popover: live rows for every inference server the Studio aggregator reports (Unsloth, Laguna DFlash, oMLX, KNXT TTS, YuE2, SheetSage2, TimesFM) with per-server state dots and per-model status. Servers collapse by default; expansion sticks across polls.
- Start/stop controls where the backend allows it (DFlash, TTS, TimesFM, YuE2; Unsloth model load/unload with confirmation). Stopping an engine frees its GPU memory; status rows reflect it live.
- LM activity now renders only when models are actually resident (no more empty "LM Studio, no models loaded" row), and legacy lane rows are retired in favor of the Inference section.

## Menu bar + reliability

- Unsloth becomes the primary menu-bar lane (supersedes LM Studio) when the host reports an Unsloth endpoint, using the host's stored token.
- New network-error badge in the menu-bar icon when a host is unreachable at the transport layer (usually Tailscale down), so a dead tailnet reads differently from an app-level error.
- Popover toggle rows and Docker rows render as proper pill controls; Studio popover screenshot-verified.

## Fixes

- Template services report live status and can be stopped (prober resolves `{host}` placeholders from each service's own fields).
