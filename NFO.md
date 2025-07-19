# 🌐 RADICA - Network Connectivity Troubleshooter
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

1. [🎯 What is RADICA?](#-what-is-RADICA)
2. [🎨 Color Profiles](#-color-profiles)
3. [📊 Logging System](#-logging-system)
4. [🔧 Usage Examples & Function Reference](#-usage-examples--function-reference)
5. [🎯 Quick Reference](#-quick-reference)
6. [📚 Function Architecture](#-function-architecture)
7. [👨‍💻 Credits & Attribution](#-credits--attribution)

---

## 🎯 What is RADICA?

**RADICA** (RADICA Connectivity Troubleshooter) is a sophisticated Bash script designed to revolutionize network troubleshooting on Linux systems. Born from the brilliant mind of **Mr. Omar Daniels**, RADICA transforms complex network diagnostics into an intuitive experience.

### 🌟 The Vision

Imagine having a network expert at your fingertips 24/7—someone who never gets tired, knows every Linux distribution, and speaks the language of packets and protocols. That's RADICA.

### ✨ What Makes RADICA Revolutionary?

- 🎨 **Accessibility Champion**: Five stunning color profiles including high-contrast for visual accessibility
- 🔍 **Smart Detection**: Automatically identifies your OS, missing tools, and dependency conflicts
- 📝 **Complete Transparency**: Comprehensive session logging with clean, professional output
- 🌐 **Universal Compatibility**: Works across Debian, RedHat, Arch, SUSE, and more
- 🚀 **Zero Configuration**: Works out of the box, enhances with your preferences

### 🎯 The RADICA Difference

| Traditional Tools | RADICA Experience |
|-------------------|------------------|
| Manual tool installation | Automatic detection & installation |
| Static troubleshooting | Expert analysis & suggestions |
| Terminal color blindness | Beautiful, accessible color themes |
| Lost session data | Comprehensive logging system |
| One-size-fits-all | Customizable to your workflow |
| Isolated problem solving | Connected to global knowledge |

### 🚀 Introduction

**RADICA** stands at the intersection of traditional Linux networking tools and cutting-edge technology. Whether you're a system administrator troubleshooting enterprise networks, a developer debugging connectivity issues, or a Linux enthusiast learning the ropes, RADICA adapts to your skill level and provides exactly the assistance you need.

### 🌟 Key Features

| Feature | Description |
|---------|-------------|
| **Smart Tool Detection** | Automatically checks for and installs missing network utilities |
| **Expert Analysis** | Get professional troubleshooting advice |
| **Color Profiles** | Choose from 5 built-in themes or load your own custom profiles |
| **Session Logging** | Complete audit trail of all diagnostic steps and results |
| **Dependency Resolution** | Intelligent package management with conflict resolution |
| **Cross-Platform** | Works across major Linux distributions |

---

## 🎨 Color Profiles

RADICA offers multiple visual themes to suit your environment and preferences:

### Built-in Profiles

| Profile | Best For | Description |
|---------|----------|-------------|
| `default` | General use | Standard terminal colors |
| `professional` | Business/presentations | Muted, professional color scheme |
| `high-contrast` | Accessibility | High contrast for visual impairments |
| `monochrome` | Minimal setups | Grayscale color scheme |
| `dark` | Dark themes | Optimized for dark terminal backgrounds |

### Custom Profile Locations

RADICA automatically scans these locations for user-defined color profiles:

```
~/.config/RADICA/colors/
~/.RADICA_colors
~/.config/terminal/colors/
~/.local/share/color-schemes/
~/.kde/share/apps/konsole/
~/.config/konsole/
```

---

## 📊 Logging System

### Features
- ✅ **Enabled by Default**: Logging is active from the start for complete transparency
- ✅ **Interactive Configuration**: Choose your log file name or disable if needed
- ✅ **Custom Filenames**: Specify your own log file names or use default RADICA.LOG
- ✅ **Clean Format**: Timestamped entries without color codes
- ✅ **Complete Sessions**: Full audit trail of all operations
- ✅ **Command Line Control**: Override logging behavior via switches

### Default Behavior
RADICA enables logging by default to ensure you never lose important troubleshooting information. On startup, you'll see:

```
=== Logging Configuration ===
✓ Logging is enabled by default for RADICA
Current log file: RADICA.LOG

Options:
1) Keep current settings (RADICA.LOG)
2) Change log file name  
3) Disable logging for this session

Choose option (1-3, default: 1):
```

### Log File Structure
```
========================================
RADICA Connectivity Troubleshooter Log
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
**Purpose**: Displays the RADICA banner and detects the operating system

```bash
# Basic usage - shows banner, detects OS, offers color selection
./radica
```
**Output**:
```
================================================
    Connectivity Troubleshooter v2.0
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
./radica --color-profile professional --log-file network_analysis.log
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
./radica
```
**Behind the scenes**:
- Detects package manager (apt, yum, dnf, pacman, zypper)
- Checks for missing network utilities
- Offers to install missing packages
- Verifies package availability in repositories

---

### Advanced Usage Scenarios

#### **Function**: `run_comprehensive_diagnostics()`
**Purpose**: Full-featured troubleshooting session

**Flow**:
1. Sets dark theme for terminal compatibility
2. Logs everything to `debug_session.log`
3. Runs comprehensive network diagnostics

---

#### **Function**: `choose_color_profile()` (Interactive)
**Purpose**: Accessibility-focused troubleshooting

```bash
# High contrast for visual accessibility
./radica --color-profile high-contrast --log-file accessibility_debug.log
```
**Benefits**: 
- Enhanced visibility for users with visual impairments
- Clear contrast between different message types
- Maintains full functionality with better readability

---

#### **Function**: `check_package_availability()` + `PKG_SATISFY`
**Purpose**: Handle complex dependency issues

```bash
# Let RADICA handle repository and dependency problems
./radica
# When packages are missing, RADICA will:
# 1. Check package availability
# 2. Resolve dependencies
# 3. Suggest repository fixes
```

---

### Specialized Diagnostic Functions

#### **Function**: `run_ethernet_diagnostics()`
**Purpose**: Comprehensive Ethernet troubleshooting

```bash
# Focused Ethernet diagnosis
./radica --ai-enabled
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

**Diagnostics include**:
- Wireless interface detection
- rfkill status checking
- Signal strength analysis
- Connection status verification

---

#### **Function**: `run_bluetooth_diagnostics()`
**Purpose**: Bluetooth connectivity analysis

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
./radica

# Silent operation with logging
./radica --log-file

# AI-powered session
./radica --ai-enabled --log-file ai_session.log

# Accessibility mode
./radica --color-profile high-contrast

# Professional presentation
./radica --color-profile professional --ai-enabled

# Developer mode (dark theme + detailed logging)
./radica --color-profile dark --log-file dev_debug.log

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

Special thanks to the open source community and Linux networking pioneers whose innovations make tools like RADICA possible.

---

## 🌟 Final Words

**RADICA** isn't just another network troubleshooting script—it's a revolution in how we approach connectivity problems. From the moment you run `./radica`, you're not just executing commands; you're embarking on a guided journey through the layers of modern networking, powered by both time-tested Unix philosophy and cutting-edge artificial intelligence.

### 💫 The Philosophy

*"Every network problem has a solution. Every solution has a story. Every story teaches us something new."*

Whether you're dealing with a stubborn WiFi connection, mysterious packet loss, or complex enterprise networking challenges, RADICA is your companion in the digital troubleshooting journey.

---

**🚀 RADICA - Making network troubleshooting RADICAy simple, beautifully intelligent! 🚀**