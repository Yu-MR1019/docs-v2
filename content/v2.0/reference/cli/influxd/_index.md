---
title: influxd - InfluxDB daemon
description: The influxd daemon starts and runs all the processes necessary for InfluxDB to function.
v2.0/tags: [influxd, cli]
menu:
  v2_0_ref:
    name: influxd
    parent: Command line tools
weight: 102
---

The `influxd` daemon starts and runs all the processes necessary for InfluxDB to function.

## Usage

```
influxd [flags]
influxd [command]
```

## Commands

| Command                                          | Description                                       |
|:-------                                          |:-----------                                       |
| [generate](/v2.0/reference/cli/influxd/generate) | Generate time series data sets using TOML schema. |
| [inspect](/v2.0/reference/cli/influxd/inspect)   | Inspect on-disk database data.                    |
| [run](/v2.0/reference/cli/influxd/run)           | Start the influxd server _**(default)**_          |

## Flags

| Flag                   | Description                                                                            | Input type |
| :--------------------- | :------------------------------------------------------------------------------------- | :--------: |
| `--assets-path`        | Override default assets by serving from a specific directory (developer mode)          | string     |
| `--bolt-path`          | Path to boltdb database (default `~/.influxdbv2/influxd.bolt`)                         | string     |
| `--e2e-testing`        | Add /debug/flush endpoint to clear stores; used for end-to-end tests (default `false`) | boolean    |
| `--engine-path`        | Path to persistent engine files (default `~/.influxdbv2/engine`)                       | string     |
| `-h`, `--help`         | Help for `influxd`                                                                     |            |
| `--http-bind-address`  | Bind address for the REST HTTP API (default `:9999`)                                   | string     |
| `--log-level`          | Supported log levels are debug, info, and error (default `info`)                       | string     |
| `--protos-path`        | Path to protos on the filesystem (default `~/.influxdbv2/protos`)                      | string     |
| `--reporting-disabled` | Disable sending telemetry data to https://telemetry.influxdata.com                     |            |
| `--secret-store`       | Data store for secrets (bolt or vault) (default `bolt`)                                | string     |
| `--store`              | Data store for REST resources (bolt or memory) (default `bolt`)                        | string     |
| `--tracing-type`       | Supported tracing types (log or jaeger)                                                | string     |