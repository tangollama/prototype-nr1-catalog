# Prototype Catalog Repo of repos

@tangollama's PoC for a conceptual architecture of the NR1 Catalog.

## Concept

Eeach item in the catalog is a `git` repository that weaved into this repository using `git submodules`, GitHub Pull Requests for submission and review, and a CI solution for handling the final build and promotion to the global account for a given submodule project.

## Prototype Execution

Request access to the repo using [this prototype form](https://docs.google.com/forms/d/e/1FAIpQLSePmDvY4wtNJkftKu1BH8qtvgQJxqcMGnOp_ANe_A_RvU8GGQ/viewform).

1. Fork this repo
2. Add a `git` submodule
3. Submit a PR
4. Accept the PR
5. PR triggers a CI script
   1. Checkout repo
   2. Checkout submodule
   3. Lint code
   4. Generate third_party_notices
   5. Align the delivered submodule with global account `uuid` (create and/or lookup)
   6. Build submodule
   7. Publish/deploy to global account