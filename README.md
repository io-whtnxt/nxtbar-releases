# NxtBar

A macOS menu bar monitor for your Macs. One status item per machine, showing CPU, RAM, GPU, disk,
and Docker container state at a glance, without opening anything.

## Install

1. Download the latest `NxtBar-x.y.z.dmg` from [Releases](https://github.com/io-whtnxt/nxtbar-releases/releases).
2. Open it and drag NxtBar to Applications.
3. Launch it. A gear icon appears in your menu bar; Settings lives there.

Requires macOS 13 or later. Universal build for Apple Silicon and Intel.

Signed and notarized by Apple, so there is no Gatekeeper warning and no right-click-to-open
dance. NxtBar updates itself — "Check for Updates…" is in the gear menu, and it checks in the
background on its own.

## What works today

Monitoring **the Mac you install it on** works out of the box: CPU, RAM, and disk are sampled
locally, and the reading appears in your menu bar immediately.

Monitoring a **second** Mac needs a small stats agent running on that machine, serving JSON over
HTTP, and a packaged installer for that agent does not ship yet. If you add a remote host in
Settings today, it will only work if you have built your own aggregator. A proper cross-platform
agent is the next thing being built — until then, treat multi-machine monitoring as
"bring your own agent."

## Updates

NxtBar uses [Sparkle](https://sparkle-project.org). Updates are signed with an EdDSA key and
verified before installation. The appcast feed is published from this repository.

## This repository

Releases and the update feed only. The application source is not public.
