# rime_schemas

## 分发模式

Repo -> 输入法作者自己的仓库，我们不添加/修改。

:arrow_down:

Bundles -> 集中仓库对各个 repo 的描述文件，很多输入法都有好集中 schemas 集合起来叫 bundle，存放这里。

:arrow_down:

Schemas(Recipe) -> 用户的客户端从这里拿到 bundle，由客户端解析，然后按照描述从目标仓库下载到本地。解 bundle 后变成 schemas 就可以随便安装了。


```
    +--------------------------------+
    | Bundle                         |
    |                                |
    | +--------------------------+   |
    | | Repo info                |   |
    | |                          |   |
    | | id:                      |   |
    | | url:                     |   |
    | |                          |   |
    | +--------------------------+   |
    | +--------------------------+   |
    | | Recipe                   |   |
    | | +----------------------+ |   |
    | | | id: luna_pinying     | |   |
    | | | type:                | |   |
    | | | files: Schema files  | |   |
    | | +----------------------+ |   |
    | | +----------------------+ |   |
    | | | id: luna_pinying_trad| |   |
    | | | type:                | |   |
    | | | files: Schema files  | |   |
    | | +----------------------+ |   |
    | |                          |   |
    | +--------------------------+   |
    +--------------------------------+
```

## 计划

当前格式并不固定，格式会随着一个个功能做完逐渐添加。当前的草案：
https://github.com/rimebrew/rimebrew/blob/main/bundle_spec.yaml 

逐项合并功能: https://github.com/rime/plum/issues/4

制作一些类似于 [rime-easy-en](https://github.com/BlindingDark/rime-easy-en) 之类的混合体，来演示一下创建预设组合方案的方法。

---

目前已由脚本自动生成这个仓库 https://github.com/biopolyhedron/rime_schemata

Next:https://github.com/laubonghaudoi/Chinese_Rime
---

参考：
https://github.com/Homebrew/homebrew-core
