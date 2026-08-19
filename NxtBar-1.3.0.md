## NxtBar 1.3.0

### See what LM Studio is doing

The Mac Studio and any other monitored Mac running LM Studio now report their
resident models straight into the host popover, with a live status dot for each:

- **Steady dim** — loaded and idle
- **Pulsing amber** — processing a prompt
- **Pulsing green** — generating tokens

The dot is the point. A 90% GPU reading finally has an explanation next to it,
and you can tell from the menu bar whether a machine is actually working or just
holding a model in memory.

This works on remote machines, which previously showed no LM Studio state at
all. It is read-only there: model loading and unloading stay on hosts with the
`lms` CLI local to NxtBar, unchanged from 1.2.0.

A machine with LM Studio installed but nothing loaded says so in one line. A
machine that does not run models shows nothing at all, exactly as before.

### Menu bar order sticks

Status items now carry a stable identity, so reordering them with Cmd-drag
persists across launches and survives adding or removing a machine. Previously
placement followed whatever order the hosts happened to be created in.

### Settings from any popover

Every host popover has a gear button that opens Settings already selected to
that machine, instead of opening Settings and hunting for it in the sidebar.

### Requires

Reporting LM Studio activity needs the host's stats aggregator updated to match.
Machines still running an older aggregator keep working and simply show no
LM Studio section.
