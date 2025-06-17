# 🌐 RADICO - Network Connectivity Troubleshooter
# *This tool works...*


```
██████╗  █████╗ ██████╗ ██╗ ██████╗ █████╗ 
██╔══██╗██╔══██╗██╔══██╗██║██╔════╝██╔══██╗
██████╔╝███████║██║  ██║██║██║     ███████║
██╔══██╗██╔══██║██║  ██║██║██║     ██╔══██║
██║  ██║██║  ██║██████╔╝██║╚██████╗██║  ██║
╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝ ╚═╝ ╚═════╝╚═╝  ╚═╝
      Connectivity Troubleshooter v2.0
```

> *"radica solutions for radical network problems"*

## 📚 Table of Contents

1. [🎯 What is RADICO?](#-what-is-radico)
2. [🎨 Color Profiles](#-color-profiles)
3. [🤖 AI Services Integration](#-ai-services-integration)
4. [📊 Logging System](#-logging-system)
5. [🔧 Usage Examples & Function Reference](#-usage-examples--function-reference)
6. [🎯 Quick Reference](#-quick-reference)
7. [📚 Function Architecture](#-function-architecture)
8. [👨‍💻 Credits & Attribution](#-credits--attribution)

---

## 🎯 What is RADICO?

**RADICO** (radico Connectivity Troubleshooter) is a sophisticated Bash script designed to revolutionize network troubleshooting on Linux systems. Born from the brilliant mind of **Mr. Omar Daniels** and collaboratively enhanced with **GitHub Copilot**, RADICO transforms complex network diagnostics into an intuitive, AI-powered experience.

### 🌟 The Vision

Imagine having a network expert at your fingertips 24/7—someone who never gets tired, knows every Linux distribution, speaks the language of packets and protocols, and can instantly consult the world's leading AI minds for the most challenging problems. That's RADICO.

### ✨ What Makes RADICO Revolutionary?

- 🧠 **AI-First Approach**: Seamlessly integrates with OpenAI GPT-4, Anthropic Claude, Perplexity AI, and local Ollama
- 🎨 **Accessibility Champion**: Five stunning color profiles including high-contrast for visual accessibility
- 🔍 **Smart Detection**: Automatically identifies your OS, missing tools, and dependency conflicts
- 📝 **Complete Transparency**: Comprehensive session logging with clean, professional output
- 🌐 **Universal Compatibility**: Works across Debian, RedHat, Arch, SUSE, and more
- 🚀 **Zero Configuration**: Works out of the box, enhances with your preferences

### 🎯 The RADICO Difference

| Traditional Tools | RADICO Experience |
|-------------------|------------------|
| Manual tool installation | Automatic detection & installation |
| Static troubleshooting | AI-powered analysis & suggestions |
| Terminal color blindness | Beautiful, accessible color themes |
| Lost session data | Comprehensive logging system |
| One-size-fits-all | Customizable to your workflow |
| Isolated problem solving | Connected to global AI knowledge |

### 🚀 Introduction

**RADICO** stands at the intersection of traditional Linux networking tools and cutting-edge artificial intelligence. Whether you're a system administrator troubleshooting enterprise networks, a developer debugging connectivity issues, or a Linux enthusiast learning the ropes, RADICO adapts to your skill level and provides exactly the assistance you need.

### 🌟 Key Features

| Feature | Description |
|---------|-------------|
| **Smart Tool Detection** | Automatically checks for and installs missing network utilities |
| **AI-Powered Analysis** | Get expert troubleshooting advice from multiple AI services |
| **Color Profiles** | Choose from 5 built-in themes or load your own custom profiles |
| **Session Logging** | Complete audit trail of all diagnostic steps and results |
| **Dependency Resolution** | Intelligent package management with conflict resolution |
| **Cross-Platform** | Works across major Linux distributions |

---

## 🎨 Color Profiles

radico offers multiple visual themes to suit your environment and preferences:

### Built-in Profiles

| Profile | Best For | Description |
|---------|----------|-------------|
| `default` | General use | Standard terminal colors |
| `professional` | Business/presentations | Muted, professional color scheme |
| `high-contrast` | Accessibility | High contrast for visual impairments |
| `monochrome` | Minimal setups | Grayscale color scheme |
| `dark` | Dark themes | Optimized for dark terminal backgrounds |

### Custom Profile Locations

radico automatically scans these locations for user-defined color profiles:

```
~/.config/radico/colors/
~/.radico_colors
~/.config/terminal/colors/
~/.local/share/color-schemes/
~/.kde/share/apps/konsole/
~/.config/konsole/
```

---

## 🤖 AI Services Integration

### Supported AI Providers

#### 🧠 OpenAI GPT-4
- **Best for**: Comprehensive troubleshooting analysis
- **Setup**: `export OPENAI_API_KEY="your-api-key"`
- **Get Key**: [OpenAI Platform](https://platform.openai.com/api-keys)

#### 🎓 Anthropic Claude
- **Best for**: Technical deep-dive analysis
- **Setup**: `export ANTHROPIC_API_KEY="your-api-key"`
- **Get Key**: [Anthropic Console](https://console.anthropic.com/)

#### 🔍 Perplexity AI
- **Best for**: Real-time web search + AI analysis
- **Setup**: `export PERPLEXITY_API_KEY="your-api-key"`
- **Get Key**: [Perplexity Settings](https://www.perplexity.ai/settings/api)

#### 🏠 Local Ollama
- **Best for**: Privacy-focused, offline analysis
- **Setup**: 
  ```bash
  curl -fsSL https://ollama.ai/install.sh | sh
  ollama pull llama2
  ```

---

## 📊 Logging System

### Features
- ✅ **Enabled by Default**: Logging is active from the start for complete transparency
- ✅ **Interactive Configuration**: Choose your log file name or disable if needed
- ✅ **Custom Filenames**: Specify your own log file names or use default radico.LOG
- ✅ **Clean Format**: Timestamped entries without color codes
- ✅ **Complete Sessions**: Full audit trail of all operations
- ✅ **Command Line Control**: Override logging behavior via switches

### Default Behavior
RADICO enables logging by default to ensure you never lose important troubleshooting information. On startup, you'll see:

```
=== Logging Configuration ===
✓ Logging is enabled by default for RADICO
Current log file: radico.LOG

Options:
1) Keep current settings (radico.LOG)
2) Change log file name  
3) Disable logging for this session

Choose option (1-3, default: 1):
```

### Log File Structure
```
========================================
RADICO Connectivity Troubleshooter Log
Started: 2025-06-16 14:30:22
OS: Ubuntu 22.04
========================================
[2025-06-16 14:30:25] Checking required tools...
[2025-06-16 14:30:26] ✓ ip - installed
[2025-06-16 14:30:26] ✗ ethtool - missing
...
```

---

## 🔧 Usage Examples & Function Reference

### Basic Operations

#### **Function**: `show_banner()` + OS Detection
**Purpose**: Displays the radico banner and detects the operating system

```bash
# Basic usage - shows banner, detects OS, offers color selection
./radico
```
**Output**:
```
================================================
    Connectivity Troubleshooter v2.0
    Enhanced with AI-Powered Assistance
================================================
Detected OS: Ubuntu 22.04

=== Color Profile Selection ===
Available color profiles:
1) default
2) professional
3) high-contrast
4) monochrome  
5) dark
0) Skip color selection (use default)
```

---

#### **Function**: `set_color_profile()` + `setup_logging()`
**Purpose**: Set visual theme and enable session logging

```bash
# Professional look with custom logging
./radico --color-profile professional --log-file network_analysis.log
```
**What happens**:
1. Sets professional color scheme (muted colors)
2. Enables logging to `network_analysis.log`
3. Proceeds with diagnostics using professional colors

---

#### **Function**: `check_tools()` + `get_package_info()`
**Purpose**: Verify required network tools are installed

```bash
# Standard tool verification
./radico
```
**Behind the scenes**:
- Detects package manager (apt, yum, dnf, pacman, zypper)
- Checks for missing network utilities
- Offers to install missing packages
- Verifies package availability in repositories

---

### AI-Powered Troubleshooting

#### **Function**: `call_ai_api()` + `call_openai_api()`
**Purpose**: Get immediate AI assistance for specific network issues

```bash
# Direct AI consultation with OpenAI GPT-4
export OPENAI_API_KEY="sk-your-key-here"
./radico --ai-help openai "WiFi connects but no internet access"
```
**Response format**:
```
=== AI Troubleshooting Assistant v1.0 ===
Query: WiFi connects but no internet access
Service: openai

🤖 Querying OpenAI GPT-4...
[AI provides detailed troubleshooting steps]
```

---

#### **Function**: `call_anthropic_api()`
**Purpose**: Use Claude for technical deep-dive analysis

```bash
# Technical analysis with Anthropic Claude
export ANTHROPIC_API_KEY="your-key-here"
./radico --ai-help anthropic "Bluetooth device won't pair with Ubuntu"
```
**Use case**: Complex protocol analysis, detailed configuration guidance

---

#### **Function**: `call_perplexity_api()`
**Purpose**: Real-time web search combined with AI analysis

```bash
# Current information with web search
export PERPLEXITY_API_KEY="your-key-here"
./radico --ai-help perplexity "Network interface keeps dropping on kernel 6.5"
```
**Advantage**: Gets latest driver updates, kernel bug reports, current solutions

---

#### **Function**: `call_local_ai()`
**Purpose**: Private, offline AI assistance

```bash
# Privacy-focused local AI
./radico --ai-help local "Cannot resolve DNS names"
```
**Setup required**:
```bash
curl -fsSL https://ollama.ai/install.sh | sh
ollama pull llama2
```

---

### Advanced Usage Scenarios

#### **Function**: `prompt_ai_features()` + `run_comprehensive_diagnostics()`
**Purpose**: Full-featured troubleshooting session with AI integration

```bash
# Complete diagnostic session with AI and logging
./radico --ai-enabled --color-profile dark --log-file debug_session.log
```
**Flow**:
1. Sets dark theme for terminal compatibility
2. Enables AI assistance throughout session
3. Logs everything to `debug_session.log`
4. Runs comprehensive network diagnostics
5. Offers AI analysis of detected issues

---

#### **Function**: `choose_color_profile()` (Interactive)
**Purpose**: Accessibility-focused troubleshooting

```bash
# High contrast for visual accessibility
./radico --color-profile high-contrast --log-file accessibility_debug.log
```
**Benefits**: 
- Enhanced visibility for users with visual impairments
- Clear contrast between different message types
- Maintains full functionality with better readability

---

#### **Function**: `check_package_availability()` + `PKG_SATISFY`
**Purpose**: Handle complex dependency issues

```bash
# Let radico handle repository and dependency problems
./radico
# When packages are missing, radico will:
# 1. Check package availability
# 2. Resolve dependencies
# 3. Suggest repository fixes
# 4. Offer AI assistance for complex issues
```

---

### Specialized Diagnostic Functions

#### **Function**: `run_ethernet_diagnostics()`
**Purpose**: Comprehensive Ethernet troubleshooting

```bash
# Focused Ethernet diagnosis
./radico --ai-enabled
# Then select Ethernet diagnostics
```
**Checks performed**:
- Interface detection (`ip link show`)
- Link status (`ethtool`)
- IP configuration (`ip addr show`)
- Cable connectivity (`mii-tool`)

---

#### **Function**: `run_wifi_diagnostics()`
**Purpose**: WiFi-specific troubleshooting

```bash
# WiFi troubleshooting with AI assistance
./radico --ai-help openai "WiFi interface not detected"
```
**Diagnostics include**:
- Wireless interface detection
- rfkill status checking
- Signal strength analysis
- Connection status verification

---

#### **Function**: `run_bluetooth_diagnostics()`
**Purpose**: Bluetooth connectivity analysis

```bash
# Bluetooth issues with technical AI analysis
./radico --ai-help anthropic "Bluetooth controller not responding"
```
**Covers**:
- Bluetooth service status
- Controller configuration
- Device pairing issues
- Driver problems

---

## 🎯 Quick Reference Commands

### Most Common Usage Patterns

```bash
# Quick start (interactive)
./radico

# Silent operation with logging
./radico --log-file

# AI-powered session
./radico --ai-enabled --log-file ai_session.log

# Accessibility mode
./radico --color-profile high-contrast

# Professional presentation
./radico --color-profile professional --ai-enabled

# Developer mode (dark theme + detailed logging)
./radico --color-profile dark --log-file dev_debug.log

# Get immediate AI help
./radico --ai-help local "describe your issue here"
```

---

## 📚 Function Architecture

### Core System Functions
- `show_banner()` - Display application header
- `show_usage()` - Command line help system
- `command_exists()` - Check if tools are available

### Color & UI Functions  
- `load_user_color_profiles()` - Scan for custom themes
- `set_color_profile()` - Apply color scheme
- `choose_color_profile()` - Interactive theme selection

### Package Management
- `get_package_info()` - Detect package manager
- `check_tools()` - Verify required tools
- `check_package_availability()` - Dependency resolution

### AI Integration
- `call_ai_api()` - Main AI dispatcher
- `validate_ai_service()` - Service validation
- `check_ai_availability()` - AI readiness check

### Logging System
- `setup_logging()` - Interactive log configuration
- `log_message()` - Write timestamped entries
- `echo_log()` - Dual output (console + log)

### Diagnostic Engines
- `run_ethernet_diagnostics()` - Ethernet analysis
- `run_wifi_diagnostics()` - WiFi troubleshooting  
- `run_bluetooth_diagnostics()` - Bluetooth checks
- `run_comprehensive_diagnostics()` - Full system scan

---

## 👨‍💻 Credits & Attribution

**🎯 Concept Genesis:** Mr. Omar Daniels  
**🤖 Collaborative Development:** GitHub Copilot  
**📅 Created:** June 2025  
**🔄 Version:** 2.0 Enhanced Edition  
**🏷️ License:** Open Source  

### 🙏 Acknowledgments

Special thanks to the open source community, Linux networking pioneers, and the AI researchers whose innovations make tools like RADICO possible.

---

## 🌟 Final Words

**RADICO** isn't just another network troubleshooting script—it's a revolution in how we approach connectivity problems. From the moment you run `./radico`, you're not just executing commands; you're embarking on a guided journey through the layers of modern networking, powered by both time-tested Unix philosophy and cutting-edge artificial intelligence.

### 💫 The Philosophy

*"Every network problem has a solution. Every solution has a story. Every story teaches us something new."*

Whether you're dealing with a stubborn WiFi connection, mysterious packet loss, or complex enterprise networking challenges, RADICO is your companion in the digital troubleshooting journey.

---

**🚀 RADICO - Making network troubleshooting Radicoy simple, beautifully intelligent! 🚀**