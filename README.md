# agent-skills

个人 AI 编程助手（Antigravity / Claude Code / Codex）通用工程规范技能集合。

## 包含技能

| 技能 | 路径 | 用途 |
| --- | --- | --- |
| `go-dev` | [`skills/go-dev/SKILL.md`](skills/go-dev/SKILL.md) | Go 代码风格、包/文件/结构体/接口/并发与停机规范、中文 `@brief` 注释、核心 Benchmark 与 `gofmt`/`vet`/`-race` 验证门禁 |
| `unit-test` | [`skills/unit-test/SKILL.md`](skills/unit-test/SKILL.md) | 单元测试、集成测试与黑盒 E2E 对抗性工程规范（覆盖率双标准、反假绿与删修复必红自检、六维对抗清单） |

## 使用方式

将 `skills/` 下的目录复制到对应工具的全局技能目录即可：

- **Antigravity**：`~/.gemini/config/skills/`
- **Claude Code**：`~/.claude/skills/`
- **Codex**：`~/.codex/skills/`

示例（macOS / Linux / WSL）：

```bash
mkdir -p ~/.gemini/config/skills
cp -a skills/go-dev skills/unit-test ~/.gemini/config/skills/
```

示例（Windows PowerShell）：

```powershell
New-Item -ItemType Directory -Force "$HOME\.gemini\config\skills" | Out-Null
Copy-Item -Recurse -Force .\skills\go-dev, .\skills\unit-test "$HOME\.gemini\config\skills\"
```
