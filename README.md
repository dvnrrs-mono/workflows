# Shared Workflows for Mono Gateway Projects

This repository contains GitHub workflows which are designed to be [reused][reusing-workflows] by,
or [triggered by][repository-dispatch], one or more Mono Gateway repositories.

## build-bootloaders

The [build-bootloaders][build-bootloaders] workflow builds a set of bootloaders for the Mono
Gateway board. Sources are pulled from the [rcw][rcw], [atf][atf] and [u-boot][u-boot]
repositories. The firmware is compiled using the [firmware-builder][firmware-builder] Docker
image. Each workflow run publishes the compiled bootloader images [in an artifact][artifacts]
associated with the workflow run.

[artifacts]: https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/storing-and-sharing-data-from-a-workflow
[atf]: https://github.com/dvnrrs-mono/atf
[build-bootloaders]: ./.github/workflows/build-bootloaders.yml
[firmware-builder]: https://github.com/dvnrrs-mono/firmware-builder
[rcw]: https://github.com/dvnrrs-mono/rcw
[repository-dispatch]: https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows#repository_dispatch
[reusing-workflows]: https://docs.github.com/en/actions/sharing-automations/reusing-workflows
[u-boot]: https://github.com/dvnrrs-mono/u-boot
