# tempo-rock

[![Open a PR to OCI Factory](https://github.com/canonical/tempo-rock/actions/workflows/rock-release-oci-factory.yaml/badge.svg)](https://github.com/canonical/tempo-rock/actions/workflows/rock-release-oci-factory.yaml)
[![Publish to GHCR:dev](https://github.com/canonical/tempo-rock/actions/workflows/rock-release-dev.yaml/badge.svg)](https://github.com/canonical/tempo-rock/actions/workflows/rock-release-dev.yaml)
[![Update Rock](https://github.com/canonical/tempo-rock/actions/workflows/rock-update.yaml/badge.svg)](https://github.com/canonical/tempo-rock/actions/workflows/rock-update.yaml)

[Rocks](https://canonical-rockcraft.readthedocs-hosted.com/en/latest/) for [tempo](https://grafana.com/oss/tempo/).  
This repository holds all the necessary files to build rocks for the upstream versions we support. The tempo rock is used by the [tempo-k8s-operator](https://github.com/canonical/tempo-k8s-operator) charm.

The rocks on this repository are built with [OCI Factory](https://github.com/canonical/oci-factory/), which also takes care of periodically rebuilding the images.

Automation takes care of:
* validating PRs, by simply trying to build the rock;
* pulling upstream releases, creating a PR with the necessary files to be manually reviewed;
* releasing to GHCR at [ghcr.io/canonical/tempo:dev](https://ghcr.io/canonical/tempo:dev), when merging to main, for development purposes.

