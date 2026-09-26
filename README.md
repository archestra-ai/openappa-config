# OpenAPPA configuration

`appa.toml` is the source of truth for your OpenAPPA policy. Archestra seeds it with your current policy when it creates this repository. Edit it through a reviewed pull request; Archestra pulls the merged policy after validation.

The `Validate OpenAPPA policy` check parses the policy on every pull request. Add `.appa` files under `traces/` to test allowed and refused tool sequences with `appa replay`. See the [validation guide](https://www.openappa.com/validation). Make this check required in your branch protection settings.

A template update affects newly created repositories. Existing repositories keep their own policy and workflow until you review and merge a proposed update. In particular, never replace a deployment's `appa.toml` with the template example.
