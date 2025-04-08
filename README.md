# Awesome Cursor MCP

一个用于增强[Cursor编辑器](https://cursor.sh/)功能的模型上下文协议(Model Context Protocol)配置集合。

## 📖 简介

这个仓库包含了预配置的MCP服务器配置，可以扩展Cursor编辑器的AI能力，使其能够与浏览器交互、执行顺序思考，以及使用Playwright进行自动化测试。

## 🛠️ 包含的MCP服务

该配置包含以下MCP服务：

### 1. Browser Tools MCP

允许AI助手与浏览器进行交互，可以：
- 获取控制台日志和错误
- 捕获网络日志和错误
- 截取屏幕截图
- 执行可访问性、性能和SEO审计

### 2. Sequential Thinking

增强AI的思考过程，使其能够：
- 分解复杂问题
- 进行多步骤分析
- 生成和验证假设
- 通过思考链得出更准确的结论

### 3. Playwright MCP Server

使AI能够通过Playwright自动化浏览器操作，例如：
- 导航到网页
- 获取页面内容
- 与页面元素交互（点击、拖放等）
- 模拟用户操作

## 🚀 使用方法

1. 在Cursor编辑器中，将此`mcp.json`文件复制到你的项目根目录。
2. 启动Cursor编辑器，确保AI功能已启用。
3. 开始使用增强后的AI功能进行开发。

## 🔧 配置文件详解

```json
{
    "mcpServers": {
        "browser-tools-mcp": {
            "command": "npx",
            "args": [
                "-y",
                "@agentdeskai/browser-tools-mcp"
            ]
        },
        "sequential-thinking": {
            "command": "npx",
            "args": [
                "-y",
                "@modelcontextprotocol/server-sequential-thinking"
            ]
        },
        "playwright-mcp-server": {
            "command": "cmd",
            "args": [
                "/c",
                "npx",
                "-y",
                "@smithery/cli@latest",
                "run",
                "@showfive/playwright-mcp-server",
                "--key",
                "5ed3768e-aba6-4c41-8ecb-6b31ceed935f"
            ]
        }
    }
}
```

## 📋 前提条件

- 安装了Cursor编辑器
- Node.js环境（用于运行NPM包）
- 如使用Playwright功能，需要安装相关浏览器驱动

## 🤝 贡献

欢迎提交问题和拉取请求，共同改进这个MCP配置集合。

## 📜 许可证

MIT 