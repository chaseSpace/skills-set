# skills-set

一组可复用的 Codex Skills。每个 Skill 都是一个独立目录，包含必需的 `SKILL.md` 与按需加载的参考资料。

## Skills

### React Bits

`react-bits/` 用于在已有 React 项目中选择、安装并集成 [React Bits](https://reactbits.dev) 的组件、动效和背景。

- 先检测项目的 TypeScript / JavaScript、Tailwind / CSS、SSR / Next.js 和 shadcn 配置。
- 根据项目选用 `TS-TW`、`TS-CSS`、`JS-TW` 或 `JS-CSS` 实现变体。
- 需求不明确时先澄清项目、页面位置、效果、交互与约束；只有确认一个真实组件名（如 `AcidSquares`）后才会安装或引入代码。
- 采用渐进式资料加载：文字动效、通用动效、UI 组件、背景和 React Bits Pro 分别独立。
- 包含 SSR 客户端边界、依赖、无障碍、减少动态效果和性能方面的集成约束。

## 安装到 Codex

### 当前仓库可用

将 Skill 放入目标项目的 `.agents/skills`：

```bash
git clone git@github.com:chaseSpace/skills-set.git /tmp/skills-set
mkdir -p .agents/skills
cp -R /tmp/skills-set/react-bits .agents/skills/
```

Codex 会在当前工作目录至仓库根目录间查找 `.agents/skills`。该方式适合把 Skill 与项目一起版本管理。

### 本机全局可用

将 Skill 放入用户目录：

```bash
git clone git@github.com:chaseSpace/skills-set.git /tmp/skills-set
mkdir -p "$HOME/.agents/skills"
cp -R /tmp/skills-set/react-bits "$HOME/.agents/skills/"
```

Codex 通常会自动发现新技能；若界面未显示，请重启 Codex。

## 使用

可显式调用：

```text
$react-bits 为 Next.js + TypeScript + Tailwind 页面添加一个轻量的产品背景
```

也可以直接描述需求，例如“用 React Bits 给这个数据指标做文字进入动画”。Skill 会先选择匹配项目的实现变体，再只读取相关类别的组件目录。

## 目录结构

```text
react-bits/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── project-routing.md
    ├── installation.md
    ├── text-animations.md
    ├── animations.md
    ├── components.md
    ├── backgrounds.md
    └── react-bits-pro.md
```

React Bits Pro 是单独的、许可控制的注册表；Skill 只会在需求确实属于页面区块、应用界面、模板或 Agent Kit 时引导至 Pro，不会把它与免费的 React Bits 组件混用。
