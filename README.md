# snowflake-rs (mirror)

Full mirror of [spiceai/snowflake-rs](https://github.com/spiceai/snowflake-rs), which is itself a fork of [andrusha/snowflake-rs](https://github.com/andrusha/snowflake-rs).

This mirror exists to insulate [runtimedb](https://github.com/hotdata-dev/runtimedb) builds from upstream availability. All branches and tags are synced daily via GitHub Actions.

## Acknowledgements

- [Andrew Korzhuev](https://github.com/andrusha) — original author of snowflake-rs
- [Spice.ai](https://github.com/spiceai) — maintainers of the actively-developed fork with Arrow compatibility patches

## How it works

- The `hotdata` branch (default) contains only this README and the sync workflow.
- All other branches are mirrored verbatim from `spiceai/snowflake-rs`.
- A daily workflow checks whether Spice.ai has updated their pinned rev in [spiceai/spiceai](https://github.com/spiceai/spiceai) and files a PR against runtimedb if so.

## Setup

The sync workflow requires a `RUNTIMEDB_PAT` repository secret — a fine-grained GitHub PAT with:
- **Repository access**: `hotdata-dev/runtimedb`
- **Permissions**: `Contents: Read and write`, `Pull requests: Read and write`
