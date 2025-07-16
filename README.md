# 🎉Claude Code 安装使用教程【最新】
[English](README_en.md) | [中文](README.md)

>Claude Code 是一个强大的 AI 编程助手，让您可以直接在终端中与 AI 协作编程。本教程将指导您完成安装和配置过程。
## 📋 系统要求

- Node.js 版本 ≥ 18.0
- 支持的操作系统：macOS、Linux、Windows (WSL)

## 🚀 快速开始
### 1. 安装 Node.js

> 💡 **提示**：如果您已经安装了 Node.js 18.0 或更高版本，可以跳过此步骤。

#### Ubuntu / Debian 用户

```bash
# 安装 Node.js LTS 版本
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo bash -
sudo apt-get install -y nodejs

# 验证安装
node --version
```

#### macOS 用户

```bash
# 安装 Xcode 命令行工具
sudo xcode-select --install

# 安装 Homebrew（如果尚未安装）
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 通过 Homebrew 安装 Node.js
brew install node

# 验证安装
node --version
```

### 2. 安装 Claude Code

使用 npm 全局安装 Claude Code：

```bash
npm install -g @anthropic-ai/claude-code

# 验证安装
claude --version
```

### 3. 配置并开始使用

#### 获取必要的配置信息
前往`https://api.jisuai.top` 注册并登录，前往 控制台 -> API令牌 页面复制令牌备用。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/194152b1d42b4edb847aaad216e49657.png)

您需要准备两个重要的配置项：

| 配置项 | 说明 | 获取方式 |
|--------|------|----------|
| **ANTHROPIC_AUTH_TOKEN** | API 认证令牌 | 注册后在 `API令牌` 页面点击 `添加令牌` 获得（以 `sk-` 开头） |
| **ANTHROPIC_BASE_URL** | API 服务地址 | 使用 `https://api.jisuai.top`（与主站地址相同） |

> 📝 **创建令牌时的建议设置**：
> - 名称：随意命名
> - 额度：设为无限额度
> - 其他选项：保持默认设置

#### 启动 Claude Code

在您的项目目录下运行：

```bash
# 进入项目目录
cd your-project-folder

# 设置环境变量
export ANTHROPIC_AUTH_TOKEN=sk-...  # 替换为您的实际令牌
export ANTHROPIC_BASE_URL=https://api.jisuai.top

# 启动 Claude Code
claude
```

#### 初次运行配置

启动后，您将看到以下配置步骤：

1. **选择主题** → 选择您喜欢的主题 + 按 Enter
2. **安全须知** → 确认安全须知 + 按 Enter
3. **Terminal 配置** → 使用默认配置 + 按 Enter
4. **工作目录信任** → 信任当前目录 + 按 Enter

✨ **恭喜！** 现在您可以开始与您的 AI 编程搭档一起写代码了！

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6b56ac6aa92b4f15a12e3f4fe03f15aa.png)

## ❓ 常见问题解答

### Q: 遇到 "Invalid API Key · Please run /login" 错误？

**A:** 这表明 Claude Code 未检测到环境变量。请检查：
- 是否正确设置了 `ANTHROPIC_AUTH_TOKEN` 和 `ANTHROPIC_BASE_URL`
- 环境变量值是否正确（令牌以 `sk-` 开头）
- 如果使用了永久配置，是否重启了终端

### Q: 为什么显示 "offline" 状态？

**A:** Claude Code 通过连接 Google 来判断网络状态。显示 "offline" 不影响正常使用，只是表明无法连接到 Google。

### Q: 为什么浏览网页的 Fetch 会失败？

**A:** Claude Code 在访问网页前需要调用 Claude 服务进行安全检查。您需要：
- 保持稳定的国际互联网连接
- 必要时使用全局代理

### Q: 请求总是显示 "fetch failed"？

**A:** 可能是网络环境导致的问题。解决方案：
1. 尝试使用代理工具


### Q: API 报错如何处理？

**A:** 可能是转发代理不稳定导致的，建议：
- 退出 Claude Code（Ctrl+C）
- 重新运行 `claude` 命令
- 如果问题持续，请稍后再试

### Q: 网页登录错误？

**A:** 尝试清除本站的 Cookie，然后重新登录。

## 📌 注意事项

- 本站直接接入官方 Claude Code 转发服务
- 仅支持 Claude Code 的 API 流量，不支持其他 API 调用
- 请妥善保管您的 API 令牌，避免泄露

## 🔗 相关链接

- [Claude Code 官方文档](https://docs.anthropic.com)
- [Node.js 官方网站](https://nodejs.org)

---

💡 **提示**：如遇到其他问题，请查看官方文档或联系技术支持。
