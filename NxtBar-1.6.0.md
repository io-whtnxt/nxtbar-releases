# NxtBar 1.6.0

## Video Engine (MiniMax H3) template

- New built-in service template for the MiniMax-H3 video engine (`mlx-serve`): the host popover gets a click-to-toggle start/stop row with a live status dot, probing the engine's `/v1/models` endpoint. Start/stop run over ssh as launchd-scoped `kickstart` / `kill TERM` on the job label — never name-pattern kills, so unrelated processes can't be caught in the crossfire.

## Fixes

- Template services now report live status and can actually be stopped. The prober was fetching the raw `{host}`-placeholder URL as written, which is invalid, so template-defined services (Video Engine, ComfyUI, Homebridge) pinned to offline forever and their stop arm was unreachable. Status probes now resolve placeholders from the service's own fields, symmetric with how start/stop commands already resolved.
