# 🎉 Claude Code Installation Guide [Latest]
[English](README_en.md) | [中文](README.md)

Claude Code is a powerful AI programming assistant that enables direct collaboration with AI in your terminal. This guide will walk you through the installation and configuration process.

## 📋 System Requirements

- Node.js version ≥ 18.0
- Supported Operating Systems: macOS, Linux, Windows (WSL)

## 🚀 Quick Start

### 1. Install Node.js

> 💡 **Tip**: Skip this step if you already have Node.js 18.0 or higher installed.

#### Ubuntu / Debian Users

```bash
# Install Node.js LTS version
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo bash -
sudo apt-get install -y nodejs

# Verify installation
node --version
```

#### macOS Users

```bash
# Install Xcode Command Line Tools
sudo xcode-select --install

# Install Homebrew (if not already installed)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Node.js via Homebrew
brew install node

# Verify installation
node --version
```

### 2. Install Claude Code

Install Claude Code globally using npm:

```bash
npm install -g @anthropic-ai/claude-code

# Verify installation
claude --version
```

### 3. Configuration and Usage

#### Get Required Configuration Information
Go to `https://api.jisuai.top`, register and log in. Navigate to Console -> API Tokens page to copy your token.

You'll need two important configuration items:

| Config Item | Description | How to Get |
|-------------|-------------|------------|
| **ANTHROPIC_AUTH_TOKEN** | API authentication token | After registration, get it from the 'API Tokens' page by clicking 'Add Token' (starts with `sk-`) |
| **ANTHROPIC_BASE_URL** | API service address | Use `https://api.jisuai.top` (same as the main site address) |

> 📝 **Recommended Token Creation Settings**:
> - Name: Any name you prefer
> - Quota: Set to unlimited
> - Other options: Keep default settings

#### Launch Claude Code

In your project directory, run:

```bash
# Navigate to your project folder
cd your-project-folder

# Set environment variables
export ANTHROPIC_AUTH_TOKEN=sk-...  # Replace with your actual token
export ANTHROPIC_BASE_URL=https://api.jisuai.top

# Start Claude Code
claude
```

#### First-Time Setup

Upon launch, you'll see the following configuration steps:

1. **Choose Theme** → Select your preferred theme + Press Enter
2. **Security Notice** → Confirm security notice + Press Enter
3. **Terminal Configuration** → Use default configuration + Press Enter
4. **Workspace Trust** → Trust current directory + Press Enter

✨ **Congratulations!** You can now start coding with your AI programming partner!

## ❓ FAQ

### Q: Getting "Invalid API Key · Please run /login" error?

**A:** This indicates Claude Code hasn't detected the environment variables. Check:
- If `ANTHROPIC_AUTH_TOKEN` and `ANTHROPIC_BASE_URL` are set correctly
- If environment variable values are correct (token starts with `sk-`)
- If using permanent configuration, restart your terminal

### Q: Why does it show "offline" status?

**A:** Claude Code uses Google connectivity to determine network status. The "offline" status doesn't affect normal usage; it just indicates inability to connect to Google.

### Q: Why do webpage Fetches fail?

**A:** Claude Code requires security checks via Claude service before accessing webpages. You need to:
- Maintain stable international internet connection
- Use global proxy if necessary

### Q: Requests always show "fetch failed"?

**A:** This might be due to network environment issues. Solutions:
1. Try using a proxy tool

### Q: How to handle API errors?

**A:** This might be caused by proxy instability. Recommended actions:
- Exit Claude Code (Ctrl+C)
- Restart with `claude` command
- If issues persist, try again later

### Q: Web login errors?

**A:** Try clearing the site's cookies and logging in again.

## 📌 Important Notes

- This site directly connects to the official Claude Code forwarding service
- Only supports Claude Code API traffic, not other API calls
- Keep your API token secure and prevent leaks

## 🔗 Related Links

- [Claude Code Official Documentation](https://docs.anthropic.com)
- [Node.js Official Website](https://nodejs.org)

---

💡 **Tip**: For other issues, please refer to the official documentation or contact technical support. 
