---
title: "gpustat: a rust-version of gpustat."
date: 2021-08-28T15:00:30.183Z
extra:
  link: https://crates.io/crates/gpustat
  image: /media/rust-logo-blk.svg
description: 📊 A simple command-line utility for querying and monitoring GPU status
taxonomies:
  tags:
    - Rust
    - GPU
    - Nvidia
---
### gpustat

[![Crates.io](https://img.shields.io/crates/v/gpustat.svg)](https://crates.io/crates/gpustat)
[![license](https://img.shields.io/github/license/alongwy/gpustat.svg?maxAge=86400)](LICENSE)

A rust version of [gpustat](https://github.com/wookayin/gpustat).

Just *less* than nvidia-smi?

#### Usage

`$ gpustat`

Options:

* `--color`            : Force colored output (even when stdout is not a tty)
* `--no-color`         : Suppress colored output
* `-u`, `--show-user`  : Display username of the process owner
* `-c`, `--show-cmd`   : Display the process name
* `-f`, `--show-full-cmd`   : Display full command and cpu stats of running process
* `-p`, `--show-pid`   : Display PID of the process
* `-F`, `--show-fan`   : Display GPU fan speed
* `-e`, `--show-codec` : Display encoder and/or decoder utilization
* `-a`, `--show-all`   : Display all gpu properties above


#### Quick Installation

Install from Cargo:

```
cargo install gpustat
```

#### Default display

> [0] | A100-PCIE-40GB | 65'C | 75 % | 33409 / 40536 MB | along(33407M)

- `[0]`: GPUindex (starts from 0) as PCI_BUS_ID
- `A100-PCIE-40GB`: GPU name
- `65'C`: Temperature
- `75 %`: Utilization
- `33409 / 40536 MB`: GPU Memory Usage
- `along(33407M)`: Username of the running processes owner on GPU (and their memory usage)


#### License

[GPL v2 License](LICENSE)