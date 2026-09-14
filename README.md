# skills-set

一个可持续扩展的 Agent Skills 集合。每项 Skill 都是独立目录，可按需安装到支持 `SKILL.md` 约定的编码 Agent。

## 安装

克隆仓库后，将所需的**完整 Skill 目录**复制到 Agent 配置的 skills 目录：

```bash
git clone git@github.com:chaseSpace/skills-set.git /tmp/skills-set
mkdir -p /path/to/your-agent-skills
cp -R /tmp/skills-set/<skill-name> /path/to/your-agent-skills/
```

请保留 `SKILL.md`、`references/` 和其他同级文件；具体发现目录、刷新和调用方式以所用 Agent 的文档为准。

## 可用 Skills

| Skill | 说明 |
| --- | --- |
| [`react-bits`](react-bits/) | 为 React 项目选择、安装和集成 React Bits 组件。 |

每项 Skill 的适用范围、前置条件和使用细节均在该目录的 `SKILL.md` 中说明。

## 目录约定

```text
<skill-name>/
├── SKILL.md       # 必需：触发条件与工作流
├── references/    # 可选：按需读取的详细资料
├── scripts/       # 可选：可执行辅助工具
└── assets/        # 可选：模板与输出资源
```

## 添加 Skill

新 Skill 请使用小写短横线命名，并至少提供包含 `name` 和 `description` 前置元数据的 `SKILL.md`。将领域资料放在 `references/`，让入口文件保持精简并支持渐进式加载。
