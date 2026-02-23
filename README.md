<p align="center">
  <img src="https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-manager/main/logo.jpg" width="660" alt="OpenClaw Model Manager Logo">
</p>
</p>
<h1 align="center">OpenClaw Model Manager 🦞</h1>

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
Built by Nex-ZMH,an energy industry AI explorer from a remote mountain village of China in February 2026.

<p align="center">
  🌐 Languages:
  <a href="#english">English</a> ·
  <a href="#中文">简体中文</a> ·
<p align="center">
 ⚡️Quick Routes: 
  <a href="#getting-started">Getting Started</a> ·
  <a href="#features">Features</a> ·
  <a href="#installation">Installation</a> ·
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-manager/main/ScreenShot.png" width="500" alt="Demo Screenshot">
</p>

---
2026.2.23 updated，this project tool can also be used for model selection with Claude code.
<p align="center">
  <img src="https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-manager/main/ScreenShot-claude.png" width="500" alt="Demo Screenshot">
</p>

---
## English

### Getting Started

**OpenClaw Model Manager** — An elegant, interactive model manager that transforms your OpenClaw experience. Featuring a polished terminal UI, it automatically detects available models from `openclaw.json` and empowers you to seamlessly switch configurations at launch — no manual file editing required.

### Features

- 🎮 **Interactive Selection** — Navigate effortlessly with arrow keys, mark with Space, confirm with Enter
- ⚡ **Zero-Config Automation** — Auto-detects models and synchronizes with `openclaw.json` in real-time
- 🖥️ **Beautiful TUI** — Clean, intuitive terminal interface for a premium CLI experience
- 🔧 **Scripting Ready** — Full command-line argument support for power users and automation
- 🌐 **Cross-Platform** — Windows ready, Linux & macOS coming soon

### Installation

```powershell
# Clone the repository
git clone https://github.com/Nex-ZMH/openclaw-model-manager.git

# Navigate to directory
cd openclaw-model-manager

# Run installer
.\install.ps1
```
Restart your terminal after installation.

### Usage

#### Interactive Mode

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

#### Keyboard Controls

| Key | Action |
|-----|--------|
| ↑/↓ | Navigate through models |
| Space | Mark/Unmark model |
| Enter | Confirm selection and start |
| Q | Quit without starting |

#### Command Line Options

```bash
openclaw gateway                  # Interactive selection
openclaw gateway --skip           # Skip selection, start directly
openclaw gateway --noselect       # Same as --skip
openclaw gateway --model <id>     # Directly select model
openclaw gateway --list           # List available models
openclaw gateway --help           # Show help
```

#### Examples

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

### Uninstallation

```powershell
.\uninstall.ps1
```

Or:

```powershell
irm https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-manager/main/uninstall.ps1 | iex
```

### Requirements

- [OpenClaw](https://github.com/sst/openclaw) installed globally via npm
- PowerShell 5.1+ (Windows)
- Node.js

### How It Works

The manager reads model configurations from `~/.openclaw/openclaw.json` and modifies the `agents.defaults.model.primary` field when you select a model.

### Roadmap

- [ ] Linux support (bash script)
- [ ] macOS support
- [ ] Model search/filter
- [ ] Recent models history

## Author

[Nex-ZMH](https://github.com/Nex-ZMH)

## License

[MIT](LICENSE)

---

## 中文

### 简介

**OpenClaw Model Manager** — 一款优雅的交互式模型切换工具，为您的 OpenClaw 使用体验带来全新升级。它拥有精致的终端界面，能够自动从 openclaw.json 中检测可用模型，让您在启动时轻松切换配置，无需手动编辑文件。

### 功能特性

- 🎮 **交互式选择** — 使用方向键轻松导航，空格键标记，回车键确认
- ⚡ **零配置自动化切换** — 自动检测 `openclaw.json` 并实时同步模型配置
- 🖥️ **精美 TUI ** — 清洁直观的终端界面，提供优质的命令行体验
- 🔧 **脚本友好** — 完整的命令行参数支持，满足高级用户和自动化需求
- 🌐 **跨平台支持** — 已支持 Windows，Linux 和 macOS 版本即将推出

### 安装方法
建议将该工具安装在.openclaw目录下，方便直接调用。

```powershell
# 克隆仓库
git clone https://github.com/Nex-ZMH/openclaw-model-manager.git

# 进入目录
cd openclaw-model-manager

# 运行安装脚本
.\install.ps1
```
重启终端即可生效。

### 使用方法

#### 交互式模式

```bash
openclaw gateway
```

显示交互式菜单：

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

#### 键盘控制键

| 按键 | 功能 |
|-----|--------|
| ↑/↓ | 上下导航选择模型 |
| Space | 标记/取消标记模型 |
| Enter | 确认选择并启动 |
| Q | 退出不启动 |

#### 命令行参数

```bash
openclaw gateway                  # 交互式选择
openclaw gateway --skip           # 跳过选择，直接启动
openclaw gateway --noselect       # 同同 --skip
openclaw gateway --model <id>     # 直接指定模型并启动
openclaw gateway --list           # 列出可用模型
openclaw gateway --help           # 显示帮助
```

#### 示例

```bash
# 交互式选择模型
openclaw gateway

# 指定模型启动
openclaw gateway --model qwen-bailian/kimi-k2.5

# 列出所有已配置的模型
openclaw gateway --list

# 不更改模型直接启动
openclaw gateway --skip
```

### 卸载

```powershell
.\uninstall.ps1
```

或：

```powershell
irm https://raw.githubusercontent.com/Nex-ZMH/openclaw-model-manager/main/uninstall.ps1 | iex
```

### 系统要求

- [OpenClaw](https://github.com/sst/openclaw) installed globally via npm
- PowerShell 5.1+ (Windows)
- Node.js

### 工作原理

从 `~/.openclaw/openclaw.json` 读取模型配置，当你选择模型时修改 `agents.defaults.model.primary` 字段。

### 开发计划

- [ ] Linux 支持（bash 脚本）
- [ ] macOS 支持
- [ ] 搜索/过滤模型
- [ ] 最近模型历史记录

## 作者

[Nex-ZMH](https://github.com/Nex-ZMH)

## 许可

[MIT](LICENSE)



