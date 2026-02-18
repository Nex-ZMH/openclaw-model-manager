<p align="center">
  <img src="https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-switcher/main/logo.jpg" width="220" alt="OpenClaw Model Switcher Logo">
</p>

<h1 align="center">OpenClaw Model Switcher 🦀</h1>

<p align="center">
  <b>Zero friction. Zero config. 100% Interactive.</b>
</p>

<p align="center">
  ⚡ Launch. Select. Play. The elegant model manager for OpenClaw.
</p>

<p align="center">
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square" alt="License: MIT">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/PowerShell-5.1+-blue.svg?style=flat-square&logo=powershell" alt="PowerShell">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Platform-Windows-green.svg?style=flat-square&logo=windows" alt="Platform">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Status-Stable-brightgreen.svg?style=flat-square" alt="Status">
  </a>
</p>

<p align="center">
  <a href="#english">English</a> ·
  <a href="#中文">简体中文</a> ·
  <a href="#getting-started">Getting Started</a> ·
  <a href="#features">Features</a> ·
  <a href="#installation">Installation</a> ·
  <a href="#contributing">Contributing</a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-switcher/main/ScreenShot.png" width="800" alt="Demo Screenshot">
</p>

---

## English

### Getting Started

**OpenClaw Model Switcher** — An elegant, interactive model switcher that transforms your OpenClaw experience. Featuring a polished terminal UI, it automatically detects available models from `openclaw.json` and empowers you to seamlessly switch configurations at launch — no manual file editing required.

### Features

- 🎮 **Interactive Selection** — Navigate effortlessly with arrow keys, mark with Space, confirm with Enter
- ⚡ **Zero-Config Automation** — Auto-detects models and synchronizes with `openclaw.json` in real-time
- 🖥️ **Beautiful TUI** — Clean, intuitive terminal interface for a premium CLI experience
- 🔧 **Scripting Ready** — Full command-line argument support for power users and automation
- 🌐 **Cross-Platform** — Windows ready, Linux & macOS coming soon

### Installation

```powershell
# Clone the repository
git clone https://github.com/Nex-ZMH/openclaw-model-switcher.git

# Navigate to directory
cd openclaw-model-switcher

# Run installer
.\install.ps1
```
Restart your terminal after installation.

## Usage

### Interactive Mode

```bash
openclaw gateway
```

This will display an interactive menu:

```
  +-------------------------------------------------------+
  |               OpenClaw Gateway                        |
  +-------------------------------------------------------+
  | [*] ollama/qwen3:8b                                   |
  | [ ] qwen-portal/coder-model *                         |
  | [ ] qwen-bailian/kimi-k2.5 (kimi)                     |
  | [ ] qwen-bailian/glm-4.7 (glm47)                      |
  |                                                       |
  |   [Skip] Start OpenClaw directly                      |
  +-------------------------------------------------------+

  Up/Down: Navigate   Space: Mark   Enter: Confirm   Q: Quit
```

### Keyboard Controls

| Key | Action |
|-----|--------|
| ↑/↓ | Navigate through models |
| Space | Mark/Unmark model |
| Enter | Confirm selection and start |
| Q | Quit without starting |

### Command Line Options

```bash
openclaw gateway                  # Interactive selection
openclaw gateway --skip           # Skip selection, start directly
openclaw gateway --noselect       # Same as --skip
openclaw gateway --model <id>     # Directly select model
openclaw gateway --list           # List available models
openclaw gateway --help           # Show help
```

### Examples

```bash
# Select model interactively
openclaw gateway

# Start with a specific model
openclaw gateway --model qwen-bailian/kimi-k2.5

# List all configured models
openclaw gateway --list

# Start without changing model
openclaw gateway --skip
```

## Uninstallation

```powershell
.\uninstall.ps1
```

Or:

```powershell
irm https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-switcher/main/uninstall.ps1 | iex
```

## Requirements

- [OpenClaw](https://github.com/sst/openclaw) installed globally via npm
- PowerShell 5.1+ (Windows)
- Node.js

## How It Works

The switcher reads model configurations from `~/.openclaw/openclaw.json` and modifies the `agents.defaults.model.primary` field when you select a model.

## Roadmap

- [ ] Linux support (bash script)
- [ ] macOS support
- [ ] Model search/filter
- [ ] Recent models history

## Author

[Nex-ZMH](https://github.com/Nex-ZMH)

## License

[MIT](LICENSE)
