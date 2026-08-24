# NxtBar 1.5.0

## Memory pressure monitoring

Hosts now report kernel memory-pressure level (the same signal Activity Monitor's pressure graph color-codes) alongside RAM:

- Popovers show a warning/critical chip under the RAM row when a host is under memory pressure, including live swap usage.
- Local hosts sample pressure directly via `kern.memorystatus_vm_pressure_level`; remote hosts pick it up automatically once their stats aggregator is updated (the new fields are optional — older aggregators keep working, the chip simply stays hidden).
- Swap usage (`vm.swapusage`) is collected alongside pressure for context when it matters most.

## Fixes

- `install-local.sh` now validates that the signing identity is a complete key+certificate pair (not just a certificate), and accepts `NXTBAR_SIGN_IDENTITY` to sign local installs with an alternative identity such as a Developer ID cert.
