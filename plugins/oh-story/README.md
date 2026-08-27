# OH Story for DeterminFlow

将 [oh-story-claudecode](https://github.com/zenstory-ai/oh-story-claudecode) 的 Skills 作为 DeterminFlow `skill_bundles` Plugin 提供。

## 包含内容

本适配保留上游 `skills/` 下的 13 个独立 Skill，并完整保留每个 Skill 的 `references/`、必要的 `scripts/`、`assets/` 等内部资源：

- `story`
- `story-setup`
- `story-import`
- `story-long-write`
- `story-long-analyze`
- `story-long-scan`
- `story-short-write`
- `story-short-analyze`
- `story-short-scan`
- `story-deslop`
- `story-review`
- `story-cover`
- `browser-cdp`

## 与上游项目的边界

本目录只做 DeterminFlow Plugin Package 封装，不把上游的 `.claude-plugin`、`.agents`、`.zcode-plugin`、测试套件和仓库级开发配置复制进来。

`story-setup`、`browser-cdp` 以及榜单扫描/封面等能力可能依赖宿主环境（例如 Claude Code/OpenCode/Codex、Chrome/CDP、Node.js、外部 API 或联网能力）。安装 Plugin 不等于自动提供这些外部运行时。

## 目录结构

```text
oh-story/
├── extension.toml
├── README.md
└── resources/
    └── skill-bundles/
        └── oh-story/
            ├── story/
            ├── story-setup/
            ├── story-import/
            ├── story-long-write/
            ├── story-long-analyze/
            ├── story-long-scan/
            ├── story-short-write/
            ├── story-short-analyze/
            ├── story-short-scan/
            ├── story-deslop/
            ├── story-review/
            ├── story-cover/
            └── browser-cdp/
```

## 来源

上游项目：
https://github.com/zenstory-ai/oh-story-claudecode

本适配仓库尽量不修改上游 Skill 正文，以便后续同步上游更新。
