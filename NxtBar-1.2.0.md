## NxtBar 1.2.0

### LM Studio model panel

Choose which model LM Studio has loaded without opening its GUI.

On any Mac with the `lms` CLI installed, the host popover gains an **LM Studio** section:

- Every downloaded model, with the resident ones listed first and their live context length
- Tap an unloaded model to load it at LM Studio's defaults
- Tap a resident model to unload it. A model that is mid-generation asks first
- The options control sets context length, GPU offload, and TTL at load time
- Embedding models are listed separately and carry no context controls, since they have no use for them

Loads keep running when the popover closes, so a large model still shows its progress when you reopen it.

### Generic service integrations

Add your own services with HTTP or shell status checks and start/stop commands, configured in Settings rather than in code. Credentials resolve from the Keychain at run time and are never written to the config file.

### Notes

The LM Studio section only appears when the `lms` CLI is present. Installing LM Studio does not install its CLI, so a Mac with the app but no CLI sees NxtBar exactly as before, with no error and no empty state.

The host popover is slightly wider to fit model names.
