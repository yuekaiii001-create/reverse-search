# reverse-search

> 别搜「去哪找 X」。先问：**谁手上有 X，而且正在为它发愁？**

一个 Claude Code 技能。把「帮我找 X」的请求反转成「谁手上已经有 X、而且正在为它发愁」，从而绕开中介、广告和同质化竞争。

> Reframe a "help me find X" request into "who already has X and is anxious about it".

## 它解决什么问题

你搜「我想买 X」，你站在**需求方**位置：你是请求者，供给方挑你，中间隔着中介、广告和同质化竞争。

这个技能把你换到**供给方**位置。核心问题只有一个：

> **谁手上有这个东西，而且现在正为它发愁？**

发愁的供给方会主动降低筛选门槛 —— 这是价值来源，也是风险来源。

适用场景：找房、租房、找工作、招人、找客户、找供应商、找货源、二手、库存清仓、找合作伙伴、找项目机会。

## 四个动作

1. **判断要不要启动** —— 这个领域里存在「手上有货、正在发愁」的人吗？不存在就别用这套，强行逆向会给出比直接搜索更差的建议
2. **替身推演** —— 整场对话只打断一次，卡在「谁在发愁」这一步。给候选让用户纠正，不空问
3. **落到具体入口** —— 搜索词 + 信息枢纽。判断枢纽只认一条：**发愁的人会不会在这里公开说出自己的困境？** 广告位不是枢纽，评论区才是
4. **设计接触 + 风险提醒** —— 真实交换的姿态。不是救世主（对方会抗拒），也不是收割者（对方会报复）。并且必须提醒：「急」的背后可能是机会，也可能藏着隐性问题，逆向搜索降低了寻找成本，但大幅提高了筛选成本

> 另有一套「五步法」（需求剥离 → 反转供给方 → 痛点推演 → 枢纽定位 → 接触设计）是 AI 内部
> 的完整推演流程，对应上面四个动作，见 [skills/reverse-search/references/method.md](skills/reverse-search/references/method.md)。

## 安装

### 方式一：作为插件安装（推荐）

```
/plugin marketplace add yuekaiii001-create/reverse-search
/plugin install reverse-search@reverse-search
```

### 方式二：手动拷贝

把这个仓库里的 `skills/reverse-search/` 整个目录拷到你的个人技能目录：

```powershell
# Windows
Copy-Item -Recurse .\skills\reverse-search "$HOME\.claude\skills\"
```

```bash
# macOS / Linux
cp -r ./skills/reverse-search ~/.claude/skills/
```

## 使用

装好后直接用自然语言提需求即可，技能会根据描述自动触发：

> 我想买点二手显卡
>
> 帮我在 XX 区找个能长期租的房子，不想走中介
>
> 我们团队缺个后端，招了三个月没招到

也可以显式调用：`/reverse-search`

## 目录结构

```
reverse-search/
├── .claude-plugin/
│   ├── plugin.json          # 插件清单
│   └── marketplace.json     # 让 /plugin marketplace add 可用
├── skills/
│   └── reverse-search/
│       ├── SKILL.md         # 技能入口
│       ├── references/      # 渐进式披露：按需加载
│       │   ├── activation.md    # 该不该启动、什么时候逆向失效
│       │   ├── questioning.md   # 怎么反问用户（最容易做错的一步）
│       │   ├── method.md        # 完整五步法
│       │   ├── queries.md       # 搜索词构造
│       │   ├── hubs.md          # 信息枢纽定位
│       │   ├── outreach.md      # 接触方案与红线
│       │   └── risks.md         # 尽调清单
│       └── assets/
│           └── output-template.md
└── README.md
```

## 开发

```bash
# 本地加载调试
claude --plugin-dir ./reverse-search

# 改完热重载
/reload-plugins

# 提交前校验清单和 frontmatter
claude plugin validate ./reverse-search
```

## 边界

这个技能明确不做：欺骗、骚扰、绕过平台规则、利用他人的困境。

`references/outreach.md` 里写了三条硬红线，其中一条值得单独说：

> 当对方的困境是「**没有别的选择**」，而不是「想快点成交」时，你的议价优势来自对方的绝望，不是来自你提供的价值。这不是逆向思维，这是趁火打劫。退出。

## License

见 [LICENSE](LICENSE)。
