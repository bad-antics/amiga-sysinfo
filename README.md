```
╔═══════════════════════════════════════════════════════════════════════════════╗
║                                                                               ║
║     █████╗ ███╗   ███╗██╗ ██████╗  █████╗       ███████╗██╗   ██╗███████╗    ║
║    ██╔══██╗████╗ ████║██║██╔════╝ ██╔══██╗      ██╔════╝╚██╗ ██╔╝██╔════╝    ║
║    ███████║██╔████╔██║██║██║  ███╗███████║█████╗███████╗ ╚████╔╝ ███████╗    ║
║    ██╔══██║██║╚██╔╝██║██║██║   ██║██╔══██║╚════╝╚════██║  ╚██╔╝  ╚════██║    ║
║    ██║  ██║██║ ╚═╝ ██║██║╚██████╔╝██║  ██║      ███████║   ██║   ███████║    ║
║    ╚═╝  ╚═╝╚═╝     ╚═╝╚═╝ ╚═════╝ ╚═╝  ╚═╝      ╚══════╝   ╚═╝   ╚══════╝    ║
║                                                                               ║
║    AMIGA-SYSINFO V1.0 | System Intelligence Utility | ARexx Script           ║
║    github.com/bad-antics | NullSec Retro Series                               ║
╚═══════════════════════════════════════════════════════════════════════════════╝
```

## Overview

AMIGA-SYSINFO is an ARexx script for Commodore Amiga systems that gathers comprehensive system information. Perfect for hardware inventory, troubleshooting, and security auditing of Amiga installations.

## Features

- **OS Version Detection**: Kickstart and Workbench versions
- **Memory Analysis**: Chip/Fast RAM breakdown via AVAIL
- **Device Enumeration**: All mounted volumes and devices
- **Expansion Board Detection**: Zorro II/III autoconfig cards
- **Custom Chip Identification**: OCS/ECS/AGA chipset detection
- **Library Inventory**: Scans for critical system libraries
- **Assign Listing**: Shows all system logical assignments
- **Network Detection**: Checks for TCP/IP stack presence

## Requirements

- AmigaOS 1.3 or higher
- ARexx (included with OS 2.0+, optional for 1.3)

## Usage

### From CLI
```
rx amiga-sysinfo.arexx
```

### From Workbench
Double-click `amiga-sysinfo.arexx` (if ARexx is properly installed)

### With Arguments
```
rx amiga-sysinfo.arexx QUICK    ; Quick scan only
rx amiga-sysinfo.arexx FULL     ; Full detailed scan
rx amiga-sysinfo.arexx >report.txt  ; Save to file
```

## Output Sections

1. **AmigaOS Version Detection** - System and Kickstart versions
2. **Memory Map** - Available RAM via AVAIL command
3. **Mounted Devices** - INFO command output
4. **Expansion Boards** - ShowConfig or manual detection
5. **Custom Chip Detection** - Agnus/Denise identification
6. **Library Scan** - Critical .library files
7. **Assigned Devices** - Logical assignments
8. **Network Interfaces** - TCP/IP stack detection

## Compatibility

| Model | Supported |
|-------|-----------|
| A1000 | ✓ |
| A500/A500+ | ✓ |
| A600 | ✓ |
| A1200 | ✓ |
| A2000 | ✓ |
| A3000 | ✓ |
| A4000 | ✓ |
| CD32 | ✓ (with keyboard) |

## Chipset Detection

The script identifies:
- **OCS**: Original Chip Set (A1000, A500, A2000)
- **ECS**: Enhanced Chip Set (A500+, A600, A3000)
- **AGA**: Advanced Graphics Architecture (A1200, A4000, CD32)

## Network Stacks Detected

- AmiTCP
- Miami/MiamiDX
- Roadshow
- Genesis

## Installation

```
Copy amiga-sysinfo.arexx TO REXX:
; or
Copy amiga-sysinfo.arexx TO C:
```

## Sample Output

```
══════════════════════════════════════════════
 AMIGAOS VERSION DETECTION
══════════════════════════════════════════════
  System: Kickstart 40.68, Workbench 40.42

══════════════════════════════════════════════
 MEMORY MAP
══════════════════════════════════════════════
  Type   Available    In-Use    Maximum
  chip     1789184    258000    2097152
  fast     8126464    112384   16777216
  total    9915648    370384   18874368
```

## Part of the NullSec Retro Series

Single-script security and system tools for vintage computing platforms.

## License

MIT License - See LICENSE file
