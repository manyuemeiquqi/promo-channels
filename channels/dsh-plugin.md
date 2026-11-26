# DeepSeek Harness 插件生态

适用于给 DSH（DeepSeek Harness）做的插件。体量数字取自 2026-11-26。

## 前置条件

多数列表共用同一组要求，先确认这些再动手，否则会被 CI 直接拒：

- `package.json` 里声明 **`dsh.bundle`**（`bundle.patch` 指向 `cordis.patch.yml`）。只声明 `dsh.client` 不算可安装，这是最常见的被拒原因。
- 仓库带 **`dsh-plugin`** GitHub topic。
- 仓库填了 **description**。空描述的仓库不收。
- 仓库创建满 **1 天**。
- 有真实代码，不是占位或纯 README。

## 列表总览

| 仓库 | Star | 体量 | 方式 | 门槛 |
|---|---|---|---|---|
| `awesome-dsh-plugin/awesome-dsh-plugin` | 25.6k | 最大 | PR 加一个 YAML | 无 |
| `0xsline/awesome-deepseek-harness` | 1.4k | 大 | PR 改两个 README | 无 |
| `LivXue/dsh-plugin-shop` | 667 | 市场 | 多为自动抓取 | 未知 |
| `Zhiyuan-Fan/Awesome-DeepSeek-Harness-Plugins` | 572 | 大 | PR 改表格 | 按 star 排序，新项目沉底 |
| `dshplugin/dsh-plugin-hub` | 565 | 市场 | 多为自动抓取 | 未知 |
| `bruc3van/awesome-dsh-plugin-pro` | 533 | 大 | PR 加一行到 SHOWCASE.md | **要求 star > 10** |
| `Dominic789654/awesome-deepseek-harness` | 442 | 大 | PR 改两个 README | 需 `#dsh` topic |
| `polang233/dsh-plugin-index` | 338 | 市场 | 多为自动抓取 | 未知 |
| `bradeGithub/DSH-Plugins-Marketplace` | 211 | 市场 | 按 topic 抓取 | 未知 |
| `beancookie/awesome-dsh-plugin` | 198 | 中 | PR 改两个 README | 分类内按 owner 字母序 |
| `Alex-Yanggg/awesome-DSH-plugin` | 104 | 中 | PR | 未验证 |
| `kejixiaoliang/awesome-dsh-plugins` | 85 | 中 | PR / issue | 未验证 |
| `AdamPlatin123/dsh-plugin-radar` | 1.5k | 自动 | 靠 k8s 实测，不收投稿 | 不可控 |
| `awesome-dsh-plugin.com` | — | 1.3 万条 | 自动生成索引 | 不可控 |

## 逐个说明

### awesome-dsh-plugin/awesome-dsh-plugin（25.6k）

体量最大，格式最规范，CI 全自动校验。**先投这家。**

一个文件就是全部投稿：`data/plugins/<owner>__<repo>.yml`

```yaml
url: https://github.com/owner/repo
name: owner/repo
category: ui
description:
  en: 'One-line description ending with a period.'
  zh: 一句话描述，以句号结尾。
```

- `category` 取值：`agi` `ui` `usage` `theme` `model` `identity` `session` `memory` `tools` `wsl` `browser` `vision` `voice` `docs` `skill` `workflow` `git` `notify` `dev` `security` `remote` `market` `fun`
- `description.en` 必填、单行、**含 `: ` 必须加引号**
- 描述会被当成对插件功能的声明，并跟代码核对。**夸大是唯一会让人主动打回的原因。**
- 两个 README 由脚本生成，不要手工改。
- 改自己的条目就只改自己的文件。

### 0xsline/awesome-deepseek-harness（1.4k）

人工精选。在 `README.md` 和 `README.zh-CN.md` 的对应分类下各加一行：

```
- [owner/repo](https://github.com/owner/repo) - One-line description.
```

要求"no fluff"：不带徽章、条目里不放截图、不写长段落。

### beancookie/awesome-dsh-plugin（198）

同样改 `README.md` 和 `README.en.md`，格式：

```
- [owner/repo](https://github.com/owner/repo) — 一句话描述。   # 中文用全角破折号
- [owner/repo](https://github.com/owner/repo) - One-line.      # 英文用连字符
```

分类内按 owner 字母序排列，CI 会校验顺序；`scripts/build-site.mjs` 也会重排。位置放错不算大问题，但顺序对了省事。

### Dominic789654/awesome-deepseek-harness（442）

改 `README.md` 和 `README.zh-CN.md`，中英用 ` —— ` 分隔。额外要求仓库带 **`#dsh`** topic。

只允许纯新增，不能改邻近行——把条目插进别人的行里会把对方描述截断，这是他们点名的最常见错误。

### bruc3van/awesome-dsh-plugin-pro（533）

有一个"作者自荐"专区，不经编辑部审核，PR 加到 `SHOWCASE.md`。

**但要求仓库 star > 10**，CI 自动核验。新项目进不去，只能先在别处把 star 攒起来。

### Zhiyuan-Fan/Awesome-DeepSeek-Harness-Plugins（572）

README 是表格，按 star 降序排。能进，但会沉在分类末尾，主要价值是那一条外链。

## 自动抓取类

`dshplugin/dsh-plugin-hub`、`LivXue/dsh-plugin-shop`、`polang233/dsh-plugin-index`、`bradeGithub/DSH-Plugins-Marketplace` 这几家多数按 `topic:dsh-plugin` 自动收。

**结论：不可依赖。** 实测仓库加了 topic 和 description 之后，`awesome-dsh-plugin.com` 的 1.3 万条索引里依然查不到。该主动提的还是得提。
