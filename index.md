---
layout: home
title: AI 每日资讯
---

每天一条 AI 早报，一个文件存一天。

**往期：** 2026-11-04（本期） · [2026-11-03](digests/2026-11-03.html) · [2026-11-02](digests/2026-11-02.html) · [2026-11-01](digests/2026-11-01.html) · [2026-10-31](digests/2026-10-31.html) · [2026-10-30](digests/2026-10-30.html) · [2026-10-29](digests/2026-10-29.html) · [2026-10-28](digests/2026-10-28.html) · [2026-10-27](digests/2026-10-27.html) · [2026-10-26](digests/2026-10-26.html) · [2026-10-25](digests/2026-10-25.html) · [2026-10-24](digests/2026-10-24.html) · [2026-10-23](digests/2026-10-23.html) · [2026-10-22](digests/2026-10-22.html) · [2026-10-21](digests/2026-10-21.html) · [2026-10-20](digests/2026-10-20.html) · [2026-10-19](digests/2026-10-19.html) · [2026-10-18](digests/2026-10-18.html) · [2026-10-17](digests/2026-10-17.html) · [2026-10-16](digests/2026-10-16.html) · [2026-10-15](digests/2026-10-15.html) · [2026-10-14](digests/2026-10-14.html)

---

# AI 早报 2026-11-04

## 一、AI 资讯

**1. OpenAI 称 ChatGPT 搜索量已达 Google 的约 20%，但这是它自己的口径**

OpenAI 消费产品负责人 Adam Fry 在 11 月 3 日的发布会上称，ChatGPT 中触发联网搜索的查询量约为 Google 查询量的五分之一；同场还称 ChatGPT 周活已从两个月前的 10 亿升至 12 亿。

为什么值得知道：20% 是 OpenAI 自报、未公开测算方法和 Google 一侧的数据来源，独立估计要低得多（seoClarity 约 7.5%、Ahrefs 约 12%），且统计的是查询量不是流量份额——别把它当成“搜索格局已变天”，但它确实说明 AI 对话正在分流一部分“先问再搜”的需求。

来源：[The Verge 报道（11 月 3 日，转引）](https://9to5google.com/2026/11/03/chatgpt-has-hit-roughly-20-of-google-search-volume-openai-says/)、[Big Technology 报道的口径提醒](https://stevendigital.com/alerts/openai-says-chatgpt-search-20-percent-of-google/)

**2. Cursor 官方渠道里混进带后门的 Claude Code 扩展，最多 5000 人中招，卸载也清不掉**

10 月 29 日约 2:27 至 13:35（太平洋时间），Cursor 自家扩展市场分发了被篡改的 anthropic.claude-code 2.1.312 / 2.1.313，会往 ~/.ssh/authorized_keys 里写署名 svc-telemetry 的攻击者密钥并留持久化脚本；干净版是 2.1.314，但升级到干净版也不会自动清除已写入的密钥和脚本。

为什么值得知道：这是直接冲着开发者工作站来的供应链攻击，机器上常有仓库、云凭证——今天就能自查：`grep svc-telemetry ~/.ssh/authorized_keys`，中招按 Cursor 公告清密钥、清持久化任务、轮换凭证，别只卸载扩展了事。

来源：[The Hacker News（10 月 30 日）](https://thehackernews.com/2026/10/official-claude-code-vs-code-extension.html?m=1&hl=ja_JP)、[5 分钟自查清单](https://blog.authon.dev/claude-code-extension-backdoor-cursor-5-minute-check)

**3. Anthropic 修订招股书：Q3 收入 170 亿美元，却又亏回去，算力承诺高达 8954 亿美元**

11 月 2 日提交的 S-1/A 补上三季度：收入 169.56 亿美元，同比增 1127%、环比增约 47%（增速较 Q2 的 144% 放缓）；经营亏损 5.67 亿美元，主因是 50 亿美元高价短期算力采购和 20 亿美元捐赠匹配非现金支出；采购与租赁承诺合计约 8954 亿美元，其中约 698 亿美元在一年内到期，Broadcom 约 1610 亿、Google 约 1210 亿、SpaceX AI 部门最高 1205 亿、亚马逊 1100 亿美元。

为什么值得知道：这是第一家前沿模型公司完整摊开的账本——收入翻倍增长也 covering 不住算力账，短期算力溢价直接吃掉利润；对所有人都是一个信号：模型降价的另一面，是厂商在为算力锁仓付出天价。

来源：[PPC Land 对 S-1/A 的拆解（11 月 2 日）](https://ppc.land/anthropic-swings-to-567m-q3-operating-loss-on-5bn-of-short-term-compute/)、[Dealroom 报道（11 月 2 日）](https://dealroom.co/news/168953-anthropics-amended-s-1-17b-in-q3-revenue-a-slide-back-to-an-operating-lo/)

**4. SemiAnalysis 发布 GDPx：最强 agent 也只完成 12% 的真实专业任务**

11 月 2 日发布的 GDPx 用 206 个长任务、11 个专业领域（芯片设计、金融、法律、生物等）考 agent，单任务限时 8 小时、二进制通过/失败评分。Claude Opus 5.5 以 12.0% 居首（每任务 51.41 美元）、Gemini 4 Carbon 10.9% 第二（每任务仅 16.29 美元，性价比最高）、GPT-6 Astra 9.6% 第三；金融、法律领域几乎所有模型都是 0 分。

为什么值得知道：这不是又一个刷分榜——它把“答对 90% 但交付物错了”判为失败，所以分数低恰恰说明 agent 离“替你干完一份专业工作”还远；同时 Carbon 用不到三分之一的成本追到 1.1 个百分点以内，选型时成本/成功率比单看排名更重要。

来源：[SemiAnalysis GDPx 发布解读](https://www.unite.ai/semianalysis-launches-gdpx-benchmark-spanning-11-agentic-domains/)、[榜单与成本明细](https://vortx.ch/gdpx-benchmark-ai-agents-score-12-cost-428-per-win/)

**5. OpenAI 悬赏翻倍再翻倍：严重漏洞最高 17.2 万美元，还推了日常任务基准 LifeVal**

OpenAI 11 月 2 日宣布：核心产品（ChatGPT、Codex、API 平台）严重漏洞奖金升至 3 万美元，特别重大的发现基础奖 10 万美元、叠加质量/忠诚/活动奖励最高约 17.2 万美元，近 30 天内已获奖的报告可补差价；同时与 Cathedral Systems 合作搞内部安全冲刺，用自家模型攻自家系统。同日发布的 LifeVal 则用 3995 人调研提炼的日常任务（找托育、做预算、办政务）测模型，GPT-6 Astra 在 16 项任务中的 10 项拿满分。

为什么值得知道：悬赏涨到这个量级，说明厂商自己也承认 AI 正在放大攻防两边的能力；LifeVal 更值得普通用户留意——它测的不是考试题，而是你每天真的会交给 AI 的杂事。

来源：[The Decoder（11 月 3 日）](https://the-decoder.com/bug-hunters-can-now-earn-up-to-172000-from-openai-as-company-ramps-up-security/)、[Cybernews（11 月 3 日）](https://cybernews.com/ai-news/openai-increases-bug-bounty-rewards/)

**6. 英伟达被曝要求云客户“去中国化”：新合同里非中国客户占比不得低于 51%**

《金融时报》11 月 3 日引述 5 名知情人士称，英伟达近几个月口头要求数据中心和云客户：新合同中至少 51% 的服务卖给非中国公司，只影响未来合同、不追溯现有租约；英伟达未证实也未否认。同期价格信号：B300 机架国际价约 60 万美元，10 月在中国市场曾报出约 254 万美元。

为什么值得知道：这等于芯片商在当“私人出口管制员”——海外租卡训练这条路正在收窄，国内团队依赖海外云算力的成本和不确定性都会上升；但注意这是匿名信源、口头传达，51% 的统计口径（收入/算力/客户数）尚未明确，别当成已落地的政策条文。

来源：[Tech Xplore 转引 AFP/FT（11 月 3 日）](https://techxplore.com/news/2026-11-nvidia-center-clients-china-exposure.html)、[Dealroom 报道（11 月 3 日）](https://dealroom.co/news/other-1ogu1el-nvidia-orders-data-centre-clients-to-reduce-china-exposure/)

## 二、技术分享·好实践

**1. 同一个 bug，Claude Code 37 秒、DeepSeek 新 agent 73 秒——但后者是自己“听到”任务的**

Towards AI 11 月 3 日的实测：DeepSeek 开源研究原型 dsh-superagent 监听 GitHub issue、被 @ 到后自己开工，和 Claude Code 交出完全相同的 4 行修复；Claude 更快还多发现一个 bug，DeepSeek 花费约 0.2 美元且全程不用人守着。

为什么有效：钩子不在“谁更快”，而在对比结构——同一仓库、同一 bug、同一修复结果，速度/成本/自主性三维一次讲清，读者不用信作者结论，自己就能算账。

可以直接借的一招：做工具对比时固定“同一任务 + 同一验收标准”，只换一个变量，结论的可信度立刻翻倍。

链接：https://pub.towardsai.net/i-raced-deepseeks-new-agent-against-claude-code-37-seconds-vs-73-02d9ce10c4e9

**2. GDPx 为什么敢把满分 agent 打到 12%：因为它按“交付物对不对”判分**

dev.to 11 月 3 日的解读把 GDPx 的方法论讲透：8 小时真活、二进制评分、90% 完成也算失败，并点出金融/法律 0 分、安全分类器拖累部分模型分数等四个 caveat。

为什么有效：结构是“先给反直觉结论，再拆评分规则，最后主动列出自己的不可信之处”——作者先替读者质疑，读者反而更愿意信前面的结论。

可以直接借的一招：发任何榜单/测评帖时，结尾主动写 3–4 条“这个结论哪里可能不成立”，比只贴分数更像内行。

链接：https://dev.to/danielsamfdo/12-of-the-economy-the-benchmark-that-grades-ai-agents-like-employees-5f8g

**3. Cursor 后门事件最值得抄的不是新闻，是那篇“5 分钟自查”**

authon.dev 的帖子把一次供应链攻击压成一张检查单：哪两个版本、哪个密钥名、哪条 grep 命令、卸载为什么没用、清完还要轮换什么。

为什么有效：证据形式极具体——文件名、密钥标签、命令都可直接复制验证，读者读完就能动手，而不是只感到害怕。

可以直接借的一招：讲安全/翻车类话题时，结尾必须给一条“复制粘贴就能跑的验证命令”，这是收藏率最高的段落形态。

链接：https://blog.authon.dev/claude-code-extension-backdoor-cursor-5-minute-check

**4. AI 视频到底多少钱一秒？这篇把各家“信用点”全换算成了秒**

DreamDrive 11 月的跨平台成本指南把 Google Flow、Runway、Luma、Kling、Pika 的信用点体系统一换算成“一段 10 秒成片实际多少钱”，并点出分辨率是最贵的杠杆（Luma 上 1080p 比 360p 贵 20 倍）。

为什么有效：钩子直击真实痛点——套餐价看不懂，换算成“一条片子多少钱”立刻能决策；证据是各家官网价目页，不是二手传言。

可以直接借的一招：写价格/成本帖时，别贴套餐表，贴“完成一次真实任务的总价”，再加一个“最贵的变量是什么”。

链接：https://www.dreamdrive.ai/learn/cross-platform/ai-video-cost-which-platform-for-what/
