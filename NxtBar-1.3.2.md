## NxtBar 1.3.2

### Frozen numbers no longer pass for current ones

When a host stops responding, NxtBar keeps its last reading rather than blanking
the panel, so a single dropped packet doesn't empty your menu bar. The cost was
that a machine which started failing kept showing plausible numbers that were
quietly minutes old.

Those readings are now dimmed and labelled with what went wrong and how old they
are, for example **Unauthorized · last reading 4m ago**. If the fix is a token,
the same one-click path into Settings is right there.

### Failed actions say so

Restarting a container or stopping a service used to fail silently: the spinner
stopped and nothing changed. A failure now names its cause in the popover, and
says **Unauthorized** rather than **HTTP 401**.
