<!-- Modified by plannotator-lite from Plannotator v0.29.0. -->
# plannotator-lite

面向中文 PRD 评审的本地工具。桌面评审页左侧保留目录，右侧批注栏按需展开，顶部提供批注、看差异、通过和发送反馈。打开本地 Markdown 文件的桌面评审页后，可以在地址栏加上 `view=prd` 启用这套布局。

## 从源码构建

需要 Bun。在仓库根目录运行以下命令。

```sh
bun install --frozen-lockfile --registry https://registry.npmjs.org
bun run build:review
bun run build:hook
bun build apps/hook/server/index.ts --compile --outfile ./plannotator-lite
```

运行 `./plannotator-lite annotate ./example.md --gate` 打开本地 Markdown 的评审页。其他评审命令及插件接入方式见 [上游 v0.29.0 文档](https://github.com/backnotprop/plannotator/blob/v0.29.0/README.md)。在此仓库构建的可执行文件为 `./plannotator-lite`。

## 来源与许可

本项目由 [bestkurisu](https://github.com/bestkurisu) 维护，改编自 backnotprop 与 Plannotator 贡献者的 [Plannotator v0.29.0](https://github.com/backnotprop/plannotator/tree/55e6bbd2b16580b23b5926b235a314a17591d12a)。这是个人维护的衍生项目，与上游项目独立。

Copyright 2025–2026 backnotprop

本项目按 [Apache License 2.0](LICENSE) 分发。原始上游代码的 [Apache-2.0](LICENSE-APACHE) 与 [MIT](LICENSE-MIT) 许可声明均保留。改动见 [NOTICE](NOTICE)，随源码保留的第三方材料及其条款见 [第三方声明](THIRD_PARTY_NOTICES.md)。
