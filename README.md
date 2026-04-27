# Memizy Multiplayer Plugin Registry

Official multiplayer plugin registry for the Memizy platform.

This repository stores plugin manifests grouped by trust level to help platform users and integrators discover multiplayer plugins with clear confidence signals.

## Trust Levels

- `official.json`: Core plugins maintained by the Memizy team.
- `verified.json`: Audited third-party plugins that have passed additional review.
- `community.json`: All other community-submitted plugins.

## How to Submit a Plugin

1. Fork this repository.
2. Add your plugin manifest entry to `community.json`.
3. Open a Pull Request describing your plugin and any relevant documentation.
4. Wait for review from maintainers.

If accepted, your plugin will be merged into `community.json`. Verified status can be granted later after additional audit.

### Key Manifest Fields:

* `id`: The unique URL or URN identifier of your plugin. (This is where the Memizy app will fetch the plugin from).
* `capabilities.types`: The exact OQSE item types your plugin knows how to handle.
* appSpecific.memizy.registry.isStandaloneFile: A boolean indicating whether the plugin is a standalone file that can be fully downloaded and run offline. If true, the Memizy app allows users to clone and edit the plugin in their local workspace.