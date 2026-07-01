# Steam Machine Hardware Reference

Early hardware documentation collected from a retail Steam Machine using standard Linux tools.

> [!NOTE]
> This repository documents hardware information from one retail Steam Machine.
>
> No reverse engineering, firmware extraction, or hardware modification was performed.
>
> All information was collected using publicly available Linux utilities.

---

# Overview

This repository contains hardware information collected from a retail Steam Machine shortly after launch.

The purpose of this project is to preserve verifiable hardware information for the community, including developers, Linux users, reviewers, and anyone interested in Valve hardware.

If some of this information has already been published elsewhere, that is completely fine.

This repository does **not** claim to be the first source of any information.

The goal is simply to collect verified reference material from a retail unit in one place.

---

# Hardware Summary

| Component | Information |
|-----------|-------------|
| Operating System | SteamOS 3.8.12 Stable |
| Build | 20260629.1 |
| Kernel | Linux 6.16.12-valve24.1 |
| CPU | AMD Custom CPU 1772 |
| CPU Configuration | 6 Cores / 12 Threads |
| Maximum Boost Clock | ~4.86 GHz |
| GPU | AMD Radeon Graphics (Navi 33) |
| Graphics Stack | Mesa 25.3.0 |
| Vulkan | Vulkan 1.4.321 |
| Installed Memory | 1 × 16 GB DDR5-5600 (SK Hynix) |
| Memory Slots | 2 SO-DIMM |
| Maximum Supported Memory | 64 GB |
| Storage | Micron 2500 512 GB NVMe SSD |
| Motherboard | Valve Fremont (Version 9) |
| BIOS | Valve F7F0106 |

---

# Interesting Findings

- Upgradeable SO-DIMM memory (not soldered)
- Two physical DDR5 SO-DIMM slots
- Ships with one 16 GB module installed
- Maximum supported memory: 64 GB
- Valve-developed BIOS
- Valve Fremont motherboard
- Latest Mesa graphics stack included with SteamOS
- Vulkan 1.4.321 available out of the box

---

# Repository Structure

```
terminal/
    Raw terminal outputs collected from the retail machine

photos/
    Photos of the hardware (future)

docs/
    Reports and documentation (future)
```

---

# Raw Command Outputs

Complete terminal outputs are available in the `terminal/` directory.

Collected commands include:

- `cat /etc/os-release`
- `lscpu`
- `sudo dmidecode -t memory`
- `lspci`
- `lsblk`
- `sudo dmidecode -t bios`
- `sudo dmidecode -t baseboard`
- `glxinfo`
- `vulkaninfo`

Machine-specific serial numbers have been removed where appropriate.

---

# Methodology

Everything in this repository was collected using standard Linux commands available to every Steam Machine owner.

No reverse engineering.

No firmware dumping.

No BIOS modification.

No engineering sample hardware.

Only publicly available tools were used.

---

# Credits

## Hardware

Retail Steam Machine provided and tested by **ATRoUko**.

## Documentation

Command selection, documentation structure, data interpretation, and repository writing were assisted by **ChatGPT**.

---

# Contributing

If you own a retail Steam Machine and discover hardware differences, firmware updates, or additional technical information, feel free to open an Issue or Pull Request.

Community contributions are always welcome.

Please remove any serial numbers or other personally identifiable information before submitting logs.

---

## License

This project is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0).

See the LICENSE file for details.
