## NxtBar 1.1.0

First installable release. NxtBar is now signed, notarized, and updates itself.

- **Signed and notarized by Apple.** No Gatekeeper warning, no right-click-to-open.
- **Universal build** for Apple Silicon and Intel Macs.
- **Automatic updates.** "Check for Updates…" lives in the gear menu, and NxtBar checks on its own in the background.
- **Launch at login** moved into Settings, replacing the hand-installed LaunchAgent.
- **Clean first run.** A fresh install starts with just the Mac it is running on.
- App icon.

### If you ran an earlier build

This release is signed with a different certificate than the ad-hoc builds before it, so macOS
treats it as a new app for Keychain purposes. You will be asked once to allow access to each
saved host token — choose **Always Allow**. It will not happen again on future updates.

NxtBar now installs to `/Applications`. If you have an older copy in `~/Applications`, delete it,
or both will start at login and compete for menu bar space.

### Requirements

macOS 13 or later.
