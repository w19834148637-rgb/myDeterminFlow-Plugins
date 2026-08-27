# Humanizer-zh for DeterminFlow

将 [Humanizer-zh](https://github.com/op7418/Humanizer-zh) 的 `SKILL.md` 以 DeterminFlow Plugin Bundle 形式提供，使其可以通过 DeterminFlow / 笔枢的插件仓库直接安装。

## 目录结构

```text
.
├── extension.toml
├── plugin-repository.toml
├── README.md
└── resources/
    └── skill-bundles/
        └── humanizer-zh/
            └── SKILL.md
```

## 在 DeterminFlow / 笔枢中安装

添加插件仓库时填写：

- Git URL：本仓库的 GitHub 地址
- Ref：`main`（或指定的 commit / release tag）
- Subdirectory：留空（插件位于仓库根目录）

仓库包含 `plugin-repository.toml`，因此支持插件仓库目录发现；实际安装仍以根目录 `extension.toml` 为准。

## 来源

Humanizer-zh：<https://github.com/op7418/Humanizer-zh>

本适配仓库只负责将其 `SKILL.md` 包装为 DeterminFlow `skill_bundles` 资源，不修改技能正文。
