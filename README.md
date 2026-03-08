# HyWorld

![Status](https://img.shields.io/badge/status-early%20development-orange)
![Java](https://img.shields.io/badge/java-25-blue)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)
![UI](https://img.shields.io/badge/ui-JavaFX-4b8bbe)

**HyWorld** is a desktop-first management tool for **Hytale dedicated server runtimes and instances**.

It is built to make it easier to:
- import official Hytale server runtimes
- manage multiple thin instances from one shared runtime
- start, stop, and monitor instances from an embedded console
- handle authentication flows inside a cleaner admin workflow
- grow into a modern server control center for local and remote administration

> HyWorld is currently in **early development** and is focused on building a strong core before public release.

---

## Overview

HyWorld is designed around a simple idea:

- **Shared runtimes** hold the heavy official server files
- **Thin instances** hold only per-server data like configs, logs, mods, and world data
- The app manages those instances through a **desktop UI** with an embedded console and live status panels

This keeps disk usage lower, makes updates cleaner, and gives server admins a better workflow than juggling folders and batch files manually.

---

## Current Direction

HyWorld is currently being built as a **desktop-first control center** for Hytale servers, with future room for a web/remote layer later.

Current focus:
- shared runtime import
- thin instance management
- embedded server process control
- embedded instance console
- auth helper workflow
- live dashboard status
- cleaner admin UX

---

## Core Architecture

HyWorld currently uses a **shared runtime + thin instance** model.

```text
HyWorld/
  runtimes/
    <version>/
      Server/
      Assets.zip
      runtime.json

  instances/
    <instance-id>/
      config/
      logs/
      mods/
      universe/
      backups/
      instance.json
```

### Shared Runtime
A runtime contains the official files downloaded from the Hytale dedicated server package, such as:
- `Server/`
- `Assets.zip`
- `runtime.json`

### Thin Instance
An instance contains only the data unique to that server:
- configs
- logs
- mods
- universe/world data
- backups
- instance metadata

This allows multiple instances to use the same runtime without duplicating large files.

---

## Features

## Runtime Management
- Import official Hytale runtime folders
- Import official Hytale runtime zip files
- Create versioned runtime entries
- Open runtime folders directly from the UI

## Instance Management
- Create thin instances from a selected runtime
- Generate instance metadata automatically
- Open instance folders directly from the UI
- Regenerate instance launchers when needed

## Server Control
- Start selected instances from inside HyWorld
- Stop running instances from inside HyWorld
- Manage the server as an embedded process instead of relying on an external console window
- Send commands directly to the running instance

## Embedded Console
- View instance output inside the application
- Use an in-app command box
- Review app activity and launch activity
- Ongoing cleanup for ANSI/control-code rendering

## Authentication Workflow
- Support Hytale auth commands through the embedded console
- Surface auth helper information in the UI
- Support encrypted auth persistence once configured in the instance

## Dashboard
- Runtime count
- Instance count
- Running / stopped counts
- Selected instance overview
- PID / uptime / runtime version / auth state
- Recent activity panel
- Early live metrics support

---

## Planned Features

HyWorld is intended to grow into a more complete Hytale server admin tool.

Planned areas include:
- richer dashboard metrics
- cleaner instance health/status views
- config editing tools
- mod management tools
- better log browsing and search
- improved help/setup flows
- remote management support
- a future web interface layered on top of the same core model

---

## UI Goals

HyWorld is aiming for:
- a **clean dark desktop UI**
- a **modern server-control layout**
- a workflow that feels closer to a real control panel than a collection of scripts
- better quality-of-life for admins who run Hytale servers locally on Windows

The current UI is functional and improving, but visual polish is still in progress.

---

## Workflow

Typical intended workflow:

1. Download the official Hytale dedicated server package
2. Import the runtime into HyWorld
3. Create one or more thin instances
4. Start and manage those instances from the embedded console
5. Handle auth and persistence from inside the same workflow

---

## Technology

HyWorld is currently built with:
- **Java 25**
- **JavaFX**
- **JSON-based runtime and instance metadata**
- **embedded process management**
- **desktop-first UI architecture**

---

## Status

HyWorld is currently in **active development**.

The project has already proven:
- runtime import
- thin instance creation
- embedded console startup
- instance auth flow
- stop / restart flow
- dashboard foundation

The current work is focused on refining the core experience so HyWorld can become a solid public release.

---

## Installation

At the moment, HyWorld is intended to be run from source/build artifacts during development.

Planned future distribution options may include:
- packaged desktop releases
- easier first-run setup
- improved runtime import flow
- optional remote management support

---

## Contributing

Contributions are best saved until the core structure stabilizes a bit more.

The areas that will matter most are:
- UI/UX polish
- dashboard improvements
- metrics and monitoring
- config/mod tooling
- log handling
- cross-platform runtime/admin workflows

---

## Author

Created by **TriFactor**.

---

## License

License is still to be decided.
