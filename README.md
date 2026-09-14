# skills-set

一组可复用的 Agent Skills。每个 Skill 都是一个独立目录，包含必需的 `SKILL.md` 与按需加载的参考资料；可用于任何支持该目录式 Skill 约定的编码 Agent。

## Skills

### React Bits

`react-bits/` 用于在已有 React 项目中选择、安装并集成 [React Bits](https://reactbits.dev) 的组件、动效和背景。

- 先检测项目的 TypeScript / JavaScript、Tailwind / CSS、SSR / Next.js 和 shadcn 配置。
- 根据项目选用 `TS-TW`、`TS-CSS`、`JS-TW` 或 `JS-CSS` 实现变体。
- 需求不明确时先澄清项目、页面位置、效果、交互与约束；只有确认一个真实组件名（如 `AcidSquares`）后才会安装或引入代码。
- 采用渐进式资料加载：文字动效、通用动效、UI 组件、背景和 React Bits Pro 分别独立。
- 包含 SSR 客户端边界、依赖、无障碍、减少动态效果和性能方面的集成约束。

## 通用安装

克隆仓库后，将**整个** Skill 目录复制到你的 Agent 所配置的 skills 目录。必须保留 `SKILL.md`、`references/` 以及其他同级文件，不能只复制入口文件。

```bash
git clone git@github.com:chaseSpace/skills-set.git /tmp/skills-set
mkdir -p /path/to/your-agent-skills
cp -R /tmp/skills-set/react-bits /path/to/your-agent-skills/
```

不同 Agent 的 skills 发现目录、刷新方式与显式调用语法不同。请将 `/path/to/your-agent-skills` 替换为该 Agent 文档规定的位置，并在配置后按该 Agent 的方式刷新或重启。

### Codex 示例

Codex 将项目技能放在 `.agents/skills`。若希望仅对当前代码仓库生效：

```bash
git clone git@github.com:chaseSpace/skills-set.git /tmp/skills-set
mkdir -p .agents/skills
cp -R /tmp/skills-set/react-bits .agents/skills/
```

若希望对本机所有项目生效：

```bash
git clone git@github.com:chaseSpace/skills-set.git /tmp/skills-set
mkdir -p "$HOME/.agents/skills"
cp -R /tmp/skills-set/react-bits "$HOME/.agents/skills/"
```

Codex 通常会自动发现新技能；若未显示，请重启 Codex。

## 更新

重新拉取仓库后，覆盖 Agent skills 目录中的同名 Skill 即可。保留整个目录，以免丢失渐进式参考资料：

```bash
git -C /tmp/skills-set pull --ff-only
cp -R /tmp/skills-set/react-bits /path/to/your-agent-skills/
```

## 使用

通用 Agent 应读取 `react-bits/SKILL.md`，并只在需要时读取链接到的对应 `references/` 文件。该 Skill 要求先确认项目、页面位置、效果和完整组件名；在此之前不会提供或引入 Bits 代码。

在支持显式调用的 Agent 中，可使用其自身的调用格式。例如 Codex：

```text
$react-bits 为 Next.js + TypeScript + Tailwind 页面添加一个轻量的产品背景
```

也可以直接描述需求，例如“用 React Bits 给这个数据指标做文字进入动画”。Skill 会先澄清细节、选择匹配项目的实现变体，并在用户确认一个实际组件后读取相关类别的组件目录。

## 目录结构

```text
react-bits/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── project-routing.md
    ├── requirements-intake.md
    ├── installation.md
    ├── text-animations.md
    ├── animations.md
    ├── components.md
    ├── backgrounds.md
    └── react-bits-pro.md
```

React Bits Pro 是单独的、许可控制的注册表；Skill 只会在需求确实属于页面区块、应用界面、模板或 Agent Kit 时引导至 Pro，不会把它与免费的 React Bits 组件混用。
