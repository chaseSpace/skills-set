# skills-set

一个可持续扩展的 Agent Skills 集合。每项 Skill 都是独立目录，可按需安装到支持 `SKILL.md` 约定的编码 Agent。

## 安装

按需安装一个 Skill。以下示例只检出并安装 `react-bits`；将 `SKILL_NAME` 替换为可用 Skills 表中的名称即可：

```bash
SKILL_NAME="react-bits"
SKILLS_DIR="/path/to/your-agent-skills"

git clone --depth 1 --filter=blob:none --sparse \
  https://github.com/chaseSpace/skills-set.git /tmp/skills-set
git -C /tmp/skills-set sparse-checkout set "$SKILL_NAME"
mkdir -p "$SKILLS_DIR"
cp -R "/tmp/skills-set/$SKILL_NAME" "$SKILLS_DIR/"
```

请保留该 Skill 的完整目录（包括 `SKILL.md`、`references/` 和其他同级文件）。具体 skills 发现目录、刷新和调用方式以所用 Agent 的文档为准。

## 可用 Skills

| Skill | 说明 |
| --- | --- |
| [`react-bits`](react-bits/) | 为 React 项目选择、安装和集成 React Bits 组件。 |

每项 Skill 的适用范围、前置条件和使用细节均在该目录的 `SKILL.md` 中说明。

## 外站 Skill 推荐

- [svg-diagram](https://github.com/bybit-exchange/svg-diagram) — 为 Agent 提供统一的手写 SVG 图表规范，可生成架构图、流程图、时序图、数据流图和生命周期图；内置零依赖 lint 工具，帮助校验图表输出。

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
