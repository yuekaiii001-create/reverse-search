---
name: reverse-search
description: 把「帮我找 X」类请求反转为「谁手上有 X、而且正在为它发愁」，从需求方位置换到供给方位置，绕开中介、广告和同质化竞争。当用户说「帮我找 / 去哪找 / 怎么找 X / 我想买 / 我想要 / 我需要 」、且直接搜索会撞上中介、广告或激烈竞争时使用，覆盖找房租房、找工作、招人、找客户、找供应商货源、找合作伙伴、二手、转让、库存清仓、拍卖等场景；也用于用户已搜过一轮并反馈「全是中介」「全是广告」「都长得一样」。不用于普通事实检索、用户已给出具体链接、或供给方稀缺不愁卖的领域。Reframe a "help me find X" request into "who already has X and is anxious about it" — locate anxious supply-side actors, find where they publicly air the problem, and plan a transparent approach. Not for deception, harassment, platform-rule evasion, or exploiting people in distress.
metadata:
  short-description: 把「帮我找 X」反转成「谁手上有 X 且正在发愁」
---

# 逆向需求穿透

## 一句话

用户问「我去哪找 X」时，先别给搜索词。先回答：

> **谁手上有 X，而且正在为它发愁？**

## 这是什么

一个**对话滤镜**：改变 AI 面对「找资源」类请求时的默认反应。

- 不是搜索词生成器 —— 搜索词是副产品，不是目的
- 不是低价成交保证
- 不是让你去接触陌生人的工具

**核心机制**：从需求方位置换到供给方位置。

需求方位置下你是请求者，供给方挑你，中间隔着中介、广告和同质化竞争。
供给方位置下你是解决问题的人，对方有痛点，你有他需要的东西。

**位置换了，谈判位置就换了。** 发愁的供给方会主动降低筛选门槛 —— 这是价值来源，也是风险来源。

## 四个动作

### 1. 判断要不要启动

不是所有「找 X」都该走这套。判据只有一个：

> **这个领域里，存在「手上有货、正在发愁」的人吗？**

存在就启动。不存在就别启动，直接给常规答案 —— 强行逆向会给出比直接搜索更差的建议。

→ 详见 [references/activation.md](references/activation.md)

### 2. 替身推演，只打断一次

默认 AI 自己跑逆向，**不要盘问用户**。

整场对话只在**「谁在发愁」**这一步停下来问 —— 因为这一步的答案只有用户知道：他所在的城市、行业、圈子里实际情况是什么。AI 硬猜必错。

问的时候**给候选让用户纠正**，不要空问「那你觉得谁会发愁？」。

→ 详见 [references/questioning.md](references/questioning.md)

### 3. 落到具体入口

这里直接给结果，不再反问：搜索词、信息枢纽。

判断枢纽只认一条：**发愁的人会不会在这里公开说出自己的困境？** 广告位不是枢纽，评论区才是。

→ 详见 [references/queries.md](references/queries.md)、[references/hubs.md](references/hubs.md)

### 4. 给接触方案和风险

姿态是**真实交换** —— 不是救世主，也不是收割者。两者都会让对方抗拒，平等姿态的成交率更高。

输出结尾必须带风险提醒。

→ 详见 [references/outreach.md](references/outreach.md)、[references/risks.md](references/risks.md)

## 完整方法

五步法的完整展开（需求剥离 → 反转供给方 → 痛点推演 → 枢纽定位 → 接触设计）见 [references/method.md](references/method.md)。

## 输出结构

默认输出模板见 [assets/output-template.md](assets/output-template.md)。

## 参考文件索引

| 文件 | 什么时候读 |
|---|---|
| [references/activation.md](references/activation.md) | 判断该不该启动、逆向在什么情况下失效 |
| [references/questioning.md](references/questioning.md) | 决定怎么反问用户 —— **新思路核心，优先读** |
| [references/method.md](references/method.md) | 需要完整五步法时 |
| [references/queries.md](references/queries.md) | 构造搜索词时 |
| [references/hubs.md](references/hubs.md) | 定位信息枢纽时 |
| [references/outreach.md](references/outreach.md) | 设计接触话术时 |
| [references/risks.md](references/risks.md) | 输出尽调和风险提醒时 |
| [assets/output-template.md](assets/output-template.md) | 需要完整输出结构时 |
