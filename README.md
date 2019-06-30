# abstract-key-server (aks)

Abstract key server (aks) is a minimal PGP key server to support communities. aks is a kind of
read-only OpenPGP key server which is updated by some core administrators of a community. Those
core administrators can add other trusted aks server to provide lookup of other keys via their server.

This is a work-in-progress to solve specific problems in security and information sharing communities.

## Goals

- Minimal parsing of PGP packets (to reduce complexity and software dependencies)
- New keys are added via a specific vetted process (or at the discretion of the aks operator)
- AKS can connect to other trusted list to query unknown keys and there is no reconciliation protocol (by design)
- Standard HKP interface with `add` method disabled
- Simple interface to filter out known malicious or rogue PGP keys
- Fast and reliable

# Requirements

- [ardb](https://github.com/yinqiwen/ardb) as storage back-end
- Python 3.6

