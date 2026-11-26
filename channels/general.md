# 通用 GitHub 仓库推广

不限技术栈，适用于任何开源项目。核对日期 2026-11-26。

标 **VERIFIED** 的，是当天实际读到了规则原文或看到了近期活动；标 **UNVERIFIED** 的，是记忆或推断，投之前自己开页面确认。Reddit 和 V2EX 在这台机器上打不开（分别返回拦截页和拒绝连接），所以这两块基本是空的，别当成结论用。

## 能直接用的

| 渠道 | 门槛 | 方式 | 可信度 |
|---|---|---|---|
| **HelloGitHub** | 无 star 上限、无仓库年龄要求 | GitHub issue 表单 | VERIFIED |
| **Show HN** | 无 | 提交 story，标题以 `Show HN` 开头 | VERIFIED |
| **掘金** | 无，但禁止过度营销 | 发文章 | VERIFIED |
| **GitHub topics** | 无 | 仓库设置里加 | VERIFIED |
| **Product Hunt** | 无，不需要 hunter | 注册个人账号后提交产品页 | VERIFIED |

## 用不了的

| 渠道 | 为什么 |
|---|---|
| `sindresorhus/awesome` | 它索引的是「列表」，不是项目，类型不对 |
| `public-apis/public-apis` | 只收 API |
| `awesome-selfhosted` | 要求首个版本发布满 4 个月，且**明确禁止 AI/agent 代提 issue 或 PR、代写条目文案** |
| `vinta/awesome-python` | 要求仓库满 1 个月，且必须有现成的子分类可放 |
| Lobsters | 邀请制；新账号 70 天内**不能用 `show` 标签**，等于废了 |
| `the-book-of-secret-knowledge` | 2024-11 之后没动过 |

## 逐个说明

### HelloGitHub

中文渠道里最合适的一家。191k star，按月出刊，issue 表单里写明了「欢迎自荐和推荐开源项目」，**没有 star 门槛，也没有仓库年龄要求**。

提交入口：`521xueweihan/HelloGitHub` 的 issue 表单，两个模板：

- `submit-cn.yaml` —— 中文，标题前缀 `[开源推荐] `
- `submit-en.yaml` —— 英文

必填：仓库地址、分类下拉（含「人工智能」）、标题 ≤50 字、描述 32–256 字。只收 GitHub 上的项目。

### Show HN

唯一一个 1 star 的仓库也能在一天内触达数千开发者的地方。规则在 `news.ycombinator.com/showhn.html`：

- 标题必须以 `Show HN` 开头
- 必须是**能跑起来**的东西，且是**你自己的作品**
- 发帖人必须在帖子里回复讨论
- 不收 landing page、募捐、博客文章、newsletter
- 不要找人互赞；版本更新不算新内容

时间选北美东部工作日上午。

### 掘金

服务条款禁止的是「散布商业广告、过度营销信息及垃圾信息」，**没有禁止放仓库链接**。所以一篇正经的、讲怎么做的技术文，文末带仓库，不违规；一张口就是「求 star」才踩线。

判断标准是行文，不是链接本身。

### GitHub 原生

先把这几件做了，其他渠道的转化都会好一些：

- topics：小写、可用连字符、单个 ≤50 字符、最多 20 个
- README 顶部放 GIF——视觉类项目靠图卖
- 打开 Discussions，让早期用户有地方落脚

**GitHub Trending 没有任何官方说明。** 网上讲算法的都是猜的。可以把它当成「曝光之后的副产品」，不能当成一个可以投放的渠道。

### Product Hunt

规则上没门槛：个人账号就能提交，不需要 hunter。但它面向的是有落地页、有 launch 节奏的产品，一个主题插件在里面属于弱产品。零成本可以试，预期收益低。

### 少数派 Matrix

页面上写着「成功发布 3 篇符合基本规则的内容，可成为正式作者」，且有编辑审核。慢，但适合有内容可写的项目。

### Reddit

**这块没有核实。** Reddit 的所有入口（网页、JSON、old.reddit、几个镜像）从这台机器都被拦了。

流传的说法是：`r/SideProject`、`r/coolgithubprojects` 本身就是发项目的地方；`r/programming` 对自荐很不友好；`r/webdev` 把展示集中在 Showoff Saturday；`r/LocalLLaMA` 有每周自荐帖。

**投之前自己开页面看侧边栏和置顶帖。** 别照抄上面这几句。

### V2EX

`/go/create`（分享创造）节点存在，但本机连不上，规则和活跃度都没读到。

## 顺序建议

1. **GitHub 原生三件套**——免费、当天可做、其他渠道都依赖它
2. **HelloGitHub**——一个 issue，中文受众，无门槛
3. **Show HN**——需要我本人当天在帖子里回复，挑一个能坐下来的上午
4. **掘金**——写一篇真正有内容的，不是项目介绍
5. **Reddit**——自己确认规则之后手动发，一天不超过两个版
