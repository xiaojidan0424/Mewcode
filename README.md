# MewCode

MewCode 是一个使用 Python 开发的终端 AI 编程助手。它提供交互式 TUI，支持调用大模型、读写代码、执行命令、管理上下文，以及通过 MCP、Skill 和多 Agent 扩展能力。

## 主要功能

- 支持 Anthropic、OpenAI 及 OpenAI 兼容接口
- 内置文件操作、代码搜索和命令执行工具
- 支持 MCP、Skill、Hook 和项目记忆
- 支持子 Agent、团队协作与 Git Worktree
- 提供交互模式、单次命令模式和远程模式

## 安装

需要 Python 3.11 或更高版本。

```bash
git clone https://github.com/xiaojidan0424/Mewcode.git
cd Mewcode
pip install -e .
```

也可以使用 [uv](https://docs.astral.sh/uv/)：

```bash
uv sync
```

## 配置

创建 `.mewcode/config.yaml`：

```yaml
providers:
  - name: openai
    protocol: openai
    base_url: https://api.openai.com/v1
    api_key: "your-api-key-here"
    model: gpt-4o

permission_mode: default
```

请勿将包含真实 API Key 的配置文件提交到 GitHub。

## 使用

```bash
# 启动交互式终端界面
mewcode

# 执行单次任务
mewcode -p "介绍一下这个项目"

# 启动远程模式
mewcode --remote
```

使用 uv 时，在命令前添加 `uv run`，例如：

```bash
uv run mewcode
```

## 测试

```bash
pytest
```
