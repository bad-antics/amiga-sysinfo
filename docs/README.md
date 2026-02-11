# Amiga SysInfo Documentation

## Overview

Amiga SysInfo is a system information and monitoring tool with an interface inspired by the classic Amiga Workbench. It displays detailed system information in a nostalgic Amiga-style terminal UI.

## Features

- **System Overview** — CPU, memory, disk, network stats
- **Process Monitor** — Running processes with resource usage
- **Network Info** — Interface details, connections, routing
- **Hardware Detection** — Detailed hardware inventory
- **Amiga Workbench UI** — Classic blue/orange/white color scheme

## Panels

| Panel | Information |
|-------|------------|
| Chip RAM | Physical memory usage |
| Fast RAM | Virtual memory stats |
| Kickstart | OS/kernel version |
| Custom Chips | Hardware details |
| Disk Drives | Storage devices |
| Serial Ports | Network interfaces |

## Installation

```bash
cargo install amiga-sysinfo
# or
git clone https://github.com/bad-antics/amiga-sysinfo
cd amiga-sysinfo && cargo build --release
```

The Workbench-style UI uses `tui-rs` for terminal rendering with authentic Amiga color palettes.
