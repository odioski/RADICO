# 🌟 RADICA
## Network Connectivity Troubleshooter v2.0

```
██████╗  █████╗ ██████╗ ██╗ ██████╗ █████╗ 
██╔══██╗██╔══██╗██╔══██╗██║██╔════╝██╔══██╗
██████╔╝███████║██║  ██║██║██║     ███████║
██╔══██╗██╔══██║██║  ██║██║██║     ██╔══██║
██║  ██║██║  ██║██████╗██║╚██████╗██║  ██║
╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝ ╚═╝ ╚═════╝╚═╝  ╚═╝
      Connectivity Troubleshooter v2.0
```


> **RADICA** - *A comprehensive, AI-powered network troubleshooting solution for Linux systems* Network Connectivity Troubleshooter v2.0

[![Linux](https://img.shields.io/badge/Platform-Linux-blue.svg)](https://github.com/odioski/RADICA)]
[![Version](https://img.shields.io/badge/Version-2.0-green.svg)](https://github.com/odioski/RADICA)]
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)]
[![AI Powered](https://img.shields.io/badge/AI-Powered-purple.svg)](https://github.com/odioski/RADICA)]

---

## 🚀 What is RADICA?

**RADICA** is a revolutionary network connectivity troubleshooter that combines traditional diagnostic tools with cutting-edge AI technology. Whether you're dealing with Ethernet issues, WiFi problems, or Bluetooth connectivity challenges, RADICA has you covered across all major Linux distributions.

### ✨ Key Features

- 🔧 **Multi-Platform Support**: Works seamlessly on Debian/Ubuntu, RedHat/CentOS/Fedora, Arch Linux, and openSUSE
- 🤖 **AI-Powered Diagnostics**: Integration with OpenAI GPT-4, Anthropic Claude, Perplexity AI, and local Ollama
- 🌐 **Comprehensive Coverage**: Ethernet, WiFi, and Bluetooth troubleshooting in one tool
- 📦 **Smart Dependencies**: Automatically handles package conflicts and missing repositories
- 🎨 **Customizable Interface**: Multiple color schemes and themes
- 📊 **Advanced Logging**: Comprehensive session logging with customizable file names
- ⚡ **Auto-Installation**: Checks and installs missing network utilities automatically

---

## 🏃‍♂️ Quick Start

### Basic Usage
```bash
# Download and run RADICA
chmod +x RADICA
./RADICA

# Enable AI features with dark color profile and logging
./RADICA --ai-enabled --color-profile dark --log-file network_debug.log

# Get direct AI help
./RADICA --ai-help openai "WiFi connects but no internet"
```

## Color Profiles

The script supports multiple color profiles for different preferences and terminal themes:

- **default**: Standard terminal colors
- **professional**: Muted professional colors  
- **high-contrast**: High contrast colors for accessibility
- **monochrome**: Grayscale colors
- **dark**: Optimized for dark themes

The script will also automatically detect and load color profiles from:
- `~/.config/RADICA/colors/`
- `~/.RADICA_colors`
- `~/.config/terminal/colors/`
- `~/.local/share/color-schemes/`
- `~/.kde/share/apps/konsole/`
- `~/.config/konsole/`

## Logging

The script offers comprehensive logging capabilities:

- **Interactive setup**: Choose whether to enable logging during startup
- **Custom log files**: Specify your own log file name or use default `RADICA.log`
- **Command line option**: Enable logging directly with `--log-file filename.log`
- **Clean log format**: Timestamps and color-code-free entries for easy parsing
- **Session tracking**: Complete record of troubleshooting steps and results

### Logging Examples

```bash
# Enable logging interactively (will prompt for log file name)
./RADICA

# Specify log file via command line
./RADICA --log-file my_network_debug.log

# Use default log file name
./RADICA --log-file RADICA.log
```

## Dependencies

### Debian/Ubuntu (apt)
```bash
sudo apt install iproute2 net-tools ethtool iputils-ping traceroute dnsutils \
wireless-tools iw rfkill wpasupplicant bluez curl jq
```

### RedHat/CentOS/Fedora (dnf/yum)
```bash
sudo dnf install iproute net-tools ethtool iputils traceroute bind-utils \
wireless-tools iw rfkill wpa_supplicant bluez curl jq
```

### Arch Linux (pacman)
```bash
sudo pacman -S iproute2 net-tools ethtool iputils traceroute bind \
wireless_tools iw rfkill wpa_supplicant bluez curl jq
```

### openSUSE (zypper)
```bash
sudo zypper install iproute2 net-tools ethtool iputils traceroute bind-utils \
wireless-tools iw rfkill wpa_supplicant bluez curl jq
```

## AI Setup (Optional)

```bash
# OpenAI
export OPENAI_API_KEY="your-api-key"

# Anthropic Claude
export ANTHROPIC_API_KEY="your-api-key"

# Perplexity AI
export PERPLEXITY_API_KEY="your-api-key"

# Local AI (Ollama)
curl -fsSL https://ollama.ai/install.sh | sh
ollama pull llama2
```

## Permissions

Some diagnostic commands require elevated privileges. The script will:
- **Automatically request sudo** when needed for package installation
- **Gracefully handle** commands that need root access
- **Suggest alternatives** when sudo isn't available

> 💡 **Tip**: For best results, consider running with `sudo ./RADICA` or ensure your user is in the `sudo` group.

## Usage

```bash
./RADICA [OPTIONS]

Options:
  --ai-enabled                Enable AI troubleshooting features
  --ai-help SERVICE QUERY     Get AI assistance
  --color-profile PROFILE     Set color profile
  --log-file FILENAME         Enable logging to specified file
  --help, -h                  Show help message

Color Profiles:
  default       Standard terminal colors
  professional  Muted professional colors
  high-contrast High contrast colors
  monochrome    Grayscale colors
  dark         Dark theme optimized

AI Services:
  openai       OpenAI GPT-4
  anthropic    Anthropic Claude  
  perplexity   Perplexity AI
  local        Local Ollama

Examples:
  ./RADICA --ai-enabled --color-profile dark
  ./RADICA --log-file debug_session.log
  ./RADICA --ai-help openai "network interface down"
```

---

## 🎯 Supported Platforms

| Distribution | Status | Package Manager |
|-------------|---------|-----------------|
| Ubuntu/Debian | ✅ Full Support | apt |
| RedHat/CentOS/Fedora | ✅ Full Support | yum/dnf |
| Arch Linux | ✅ Full Support | pacman |
| openSUSE | ✅ Full Support | zypper |
| Other Linux | 🔄 Basic Support | Manual |

---

## 🤖 AI Integration

RADICA supports multiple AI providers for enhanced troubleshooting:

- **OpenAI GPT-4**: Advanced problem analysis
- **Anthropic Claude**: Detailed technical explanations  
- **Perplexity AI**: Real-time web-based solutions
- **Local Ollama**: Privacy-focused offline AI

### AI Configuration
```bash
# Set your preferred AI provider
export RADICA_AI_PROVIDER="openai"
export OPENAI_API_KEY="your-api-key-here"

# Or use local Ollama
export RADICA_AI_PROVIDER="ollama"
```

---

## 📸 Screenshots

### Main Interface
![RADICA Main Interface](RADICA.png)

### Advanced Diagnostics
![RADICA Advanced Mode](RADICA-LOG-EXAMPLE-LOCAL-BASH.png)
Tiny example. Download [Radica Example Log.pdf](radica-example-log.pdf) to view the full current output.
---

## 📚 Documentation

- 📖 [User Manual](NFO.md)
- 🎨 [ASCII Art Guide](ASCII%20ART.NFO.md)
- 📊 [Development Notes](DEVELOPMENT_SESSION_SUMMARY.md)
- 🔍 [Session Reports](REPORTS/)

---

## 🤝 Contributing

We welcome contributions to RADICA! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Development Setup
```bash
git clone https://github.com/odioski/RADICO.git
cd RADICO

# Additional tools...

su

# Kate - Feature Rich Text Editor and IDE
apt satisfy kate

# shfmt - Like shellcheck works well w/Kate troubleshooting Shell Scripts (bash,sh,zsh,etc.)
apt install shfmt

# Bash LSP - Plugin for Kate, in conjuction with shfmt.
snap install bash-language-server --classic
```
Might want some AI...
Gemini and Copilot versions can be found at the [Snapcraft store](https://snapcraft.io).

```
snap install Copilot-desktop
snap install gemini-desktop

# Start developing!
```

---

## 📞 Support

- 🐛 **Issues**: [GitHub Issues](https://github.com/odioski/RADICA/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/odioski/RADICA/discussions)
- 📧 **Email**: link92@bookmotives.com

---

## License

MIT License - Feel free to modify and distribute.

---

<div align="center">

**⭐ Star this repository if RADICA helped you solve your network issues! ⭐**

Made with ❤️ by [odioski](https://github.com/odioski)

</div>

---

*Originally conceived by Mr. Omar Daniels*  
*Developed collaboratively with GitHub Copilot*  
*A practical approach to network troubleshooting with modern AI assistance*
