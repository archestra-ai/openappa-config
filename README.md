# OpenAPPA configuration

`appa.toml` is the source of truth for your OpenAPPA policy. Archestra seeds it with your current policy when it creates this repository. Edit it through a reviewed pull request; Archestra pulls the merged policy after validation.

The `Validate OpenAPPA policy` check parses the policy on every pull request. A self-contained policy is also replayed against the `.appa` files under `traces/` with the standalone `appa`; see the [validation guide](https://www.openappa.com/validation). A policy Archestra keeps in sync composes inside Archestra, with its batteries and host settings, so the standalone `appa` cannot replay it: the workflow says so, and Archestra's own pull request check validates every change instead. Make both checks required in your branch protection settings.

Archestra keeps the files beside the policy current. When a new Archestra version ships a newer workflow or README, the next sync opens a pull request that updates them; review and merge it. Never replace a deployment's `appa.toml` with the template example.
