---
icon: cube
---

# Build Swarm

The Build Swarm, represented by `Gaea.Swarm.exe` is the heart of Gaea. It is the Build Engine that takes the terrain recipe created in the Gaea UI and builds it with high performance.

The Swarm is a separate command line executable so it runs faster without a UI burdening it. Gaea's UI uses it in the background when building high resolution terrains for maximum performance.

## Options

All options for the Build Swarm for a specific file can be set in the [build-options](../../using-gaea/build-and-export/build-options/ "mention").&#x20;

Some additional options can be set via [command-line-automation.md](../automation/command-line-automation.md "mention").

## Automation

See [command-line-automation.md](../automation/command-line-automation.md "mention") and [variables.md](../../developers/scripting-and-expressions/variables.md "mention") for automation scenarios.

## Post Action Report

Gaea will save a post-action report as both human readable and machine readable files. You can use them in your automation workflow or use them to gather vital intelligence about your builds.

