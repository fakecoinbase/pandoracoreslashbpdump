# Bitcoin Transaction Services

Project was transformed into 
[Bitcoin Transaction Services](https://github.com/lnp-bp/txserv).

This repository is maintained for historical reasons; to run it please install
* Cargo 
* PostgreSQL on localhost, with user `postgres` and password `example`
* issue the following commands

```shell script
cargo install diesel_cli
diesel setup
diesel migration run
cargo run --package bpdump --bin bpdump block <path to bitcoin blockchain>
```

If no *path to bitcoin blockchain* is provided, `/var/lib/bitcoin/blocks` used
by default.

The program populates database with indexed transaction information.
