## NxtBar 1.3.1

### A host now tells you why it isn't reporting

"Offline" used to mean everything: powered off, wrong address, or simply a
machine NxtBar had no credentials for. A Mac that was up and serving perfectly
looked exactly like one that was unplugged.

Each failure now names itself:

- **Unauthorized** — the host wants a token and NxtBar doesn't have the right one
- **Host error 503** — the host answered, but not with stats
- **Bad response** — it answered with something that isn't stats
- **Offline** — now means only what it always claimed: the machine can't be reached

On an authorization failure the popover offers **Add token in Settings…**, which
opens Settings already on that host, next to the token field. That field has
always been there; nothing ever told you it was the thing you needed.

Settings' **Test** button keeps the underlying cause too, so a wrong port, a DNS
failure, and a timeout no longer all print the same word.
