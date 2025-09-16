# 🎯 AI Agent周报生成提示词系统

---

> @weekly_ai_prompt.md  执行这个任务，[日期范围]：2025年9月10日-9月16日
>
> @weekly_ai_prompt.md  再次检查这个文档，确保其中提供的所有网址和搜索词都已经访问获取过内容了。 deep thinking
>
> @weekly_ai_prompt.md  再一次检查这个文档，确保其中提供的所有网址和搜索词都已经访问获取过内容了，或者之前曾经失败过，都进行重新访问和搜集内容。 deep deep thinking
>
> 在周报的md文档中，我发现有很多信息没有给出链接，而有的链接是其他周报，而非最终的源头的链接，请deep thinking更正。
>
> 在搜集周报信息时，你是否有新发现资源链接和内容，可以用于更新 @weekly_ai_prompt.md ，让其更加强大和标准。
>
> @AI_Weekly_Report_2025-09-10_to_2025-09-16.md  查看这个文档，里面的很多描述都是分为了好几条，请根据链接指向的具体内容，或你已知的信息，改为一段完整的话来描述。

---

## 标识

[日期范围]：2025年9月10日-9月16日

## 第一阶段：信息收集提示词

```markdown
# AI周报信息收集Agent

你是一个专业的AI行业周报信息收集助手。请帮我收集本周（[日期范围]）的AI行业重要动态信息。

## 收集要求：
1. **时间范围**：严格限定在指定的一周内发生的事件
2. **信息分类**：按模型发布、行业动态、热门开源、深度阅读四个维度收集
3. **质量标准**：优先收集有影响力的事件，避免重复和过时信息

## 信息源清单：
请依次搜索以下信息源，每个源至少找3-5条相关信息：

### 【非常重要】权威信息源优先级

**第一优先级：官方直接发布源**
- 公司官方新闻页面、博客、GitHub官方发布
- 官方社交媒体账号（Twitter/X、LinkedIn）
- 官方技术文档和API更新

**第二优先级：一线科技媒体**
- TechCrunch、The Verge、Wired、Fortune
- VentureBeat、Ars Technica、MIT Technology Review
- 路透社、彭博社、华尔街日报科技版

**第三优先级：AI专业媒体**
- VentureBeat AI、MIT Technology Review AI
- MarkTechPost、TheAITrack、InfoQ AI版块
- Towards Data Science、Analytics India Magazine

**参考源（用于发现线索，但需验证原始来源）：**
1. https://ai-weekly.ai/
2. https://aiweekly.co/
3. https://lastweekin.ai/
4. https://www.superhuman.ai/

### 模型发布源（按验证优先级排序）：

**主要AI厂商官方源：**
- https://www.anthropic.com/news (Anthropic官方新闻)
- https://openai.com/news (OpenAI官方新闻) 
- https://blog.openai.com/ (OpenAI官方博客)
- https://blog.google/technology/ai/ (Google AI博客)
- https://developers.googleblog.com/ (Google开发者博客)
- https://ai.meta.com/blog/ (Meta AI官方博客)
- https://mistral.ai/news/ (Mistral AI新闻)
- https://x.ai/news (xAI官方新闻)
- https://www.deepseek.com/ (DeepSeek官网)
- https://qwenlm.github.io/blog/ (Qwen模型官方博客)

**GitHub官方渠道：**
- https://github.com/blog (GitHub官方博客)
- https://github.com/trending (趋势项目)
- 各公司官方GitHub组织页面

**技术平台官方源：**
- https://huggingface.co/models?sort=trending (HuggingFace热门模型)
- https://zed.dev/blog/ (Zed编辑器官方博客)
- https://blog.replit.com/ (Replit官方博客)
- https://cursor.sh/blog (Cursor编辑器博客)

**官方社交媒体（验证信息用）：**
- https://x.com/anthropic (Anthropic官方Twitter)
- https://x.com/openai (OpenAI官方Twitter) 
- https://x.com/GoogleAI (Google AI官方Twitter)
- https://x.com/MetaAI (Meta AI官方Twitter)
- https://x.com/xai (xAI官方Twitter)
- https://x.com/deepseek_ai (DeepSeek官方Twitter)
- https://x.com/Alibaba_Qwen (Qwen官方Twitter)
- Search: "AI model release [具体日期范围，如September 3-9 2024]" site:techcrunch.com
- Search: "LLM launch" site:venturebeat.com
- Search: "新模型发布" site:36kr.com
- Search: "AI模型" site:leiphone.com

**搜索技巧提示：**
- 使用具体日期范围替换[时间范围]，如"September 3-9 2024"或"2024年9月3日-9月9日"
- 如果某个网站无法访问，请尝试其archive.org版本或相关新闻报道
- 重点关注官方发布而非传言或预测

### 行业动态源（按权威性分级）：

**A级权威媒体（优先使用）：**
- https://www.reuters.com/technology/ (路透社科技版)
- https://www.bloomberg.com/technology (彭博科技)
- https://www.ft.com/technology (金融时报科技版)
- https://www.wsj.com/tech (华尔街日报科技版)
- https://techcrunch.com/category/artificial-intelligence/ (TechCrunch AI版块)
- https://www.theverge.com/ai-artificial-intelligence (The Verge AI版块)
- https://www.wired.com/tag/artificial-intelligence/ (Wired AI版块)
- https://fortune.com/section/artificial-intelligence/ (Fortune AI版块)

**B级专业媒体：**
- https://venturebeat.com/ai/ (VentureBeat AI版块)
- https://www.technologyreview.com/topic/artificial-intelligence/ (MIT Tech Review)
- https://www.theaitrack.com/ (AI行业追踪)
- https://www.marktechpost.com/ (AI技术新闻)
- https://www.infoq.com/ai-ml/ (InfoQ AI/ML版块)
- https://analyticsindiamag.com/ (Analytics India Magazine)

**C级参考源（发现线索用）：**
- https://www.rundown.ai/ (AI新闻聚合)
- https://news.ycombinator.com/ (Hacker News)
- https://www.reddit.com/r/MachineLearning/ (机器学习讨论)
- https://www.reddit.com/r/singularity/ (AI技术讨论)

**融资数据专业源：**
- https://www.crunchbase.com/ (Crunchbase融资数据)
- https://pitchbook.com/ (PitchBook融资追踪)
- https://36kr.com/newsflashes (36氪快讯)
- https://www.itjuzi.com/ (IT桔子融资数据)
- Search: "AI funding" OR "AI investment" [具体时间范围]
- Search: "AI policy" OR "AI regulation" [具体时间范围]
- Search: "AI company acquisition" [具体时间范围]
- Search: "AI startup" site:crunchbase.com [具体时间范围]
- Search: "人工智能" site:36kr.com [具体时间范围]
- Search: "AI融资" site:itjuzi.com [具体时间范围]

**搜索策略优化：**
- 对于融资新闻，重点关注超过500万美元的A轮及以上融资
- 政策新闻关注美国、中国、欧盟的AI监管动态
- 收购新闻关注估值超过1亿美元的交易
- 如果某些网站限制访问，可搜索相关新闻的二次报道

### 开源项目源：
- https://github.com/trending (查看本周趋势)
- https://github.com/trending/typescript?since=weekly
- https://github.com/trending/python?since=weekly
- https://github.com/trending/rust?since=weekly
- https://github.com/trending/javascript?since=weekly
- https://www.reddit.com/r/ClaudeCode/ (Claude Code相关项目)
- https://www.reddit.com/r/windsurf/ (Windsurf相关项目)
- https://www.reddit.com/r/Codeium/ (Codeium相关项目)
- https://www.reddit.com/r/DeepSeek/ (DeepSeek相关项目)
- 筛选条件：与AI、机器学习、Agent、LLM、编程助手相关的项目
- 重点关注：Star数增长>500的项目

### 深度阅读源：
- https://arxiv.org/list/cs.AI/recent (最新AI论文)
- https://arxiv.org/list/cs.CL/recent (计算语言学论文)
- https://arxiv.org/list/cs.LG/recent (机器学习论文)
- https://www.deeplearning.ai/the-batch/ (DeepLearning.AI周报)
- Search: "AI agent" OR "LLM" site:medium.com [时间范围]
- Search: "AI coding" OR "AI development" site:substack.com [时间范围]
- Search: "AI编程" OR "代码智能" site:juejin.cn [时间范围]
- Search: "LLM应用" site:zhihu.com [时间范围]
- https://zed.dev/blog/ (Zed编辑器博客)
- https://cursor.sh/blog (Cursor编辑器博客)
- https://blog.replit.com/ (Replit博客)

## 输出格式（增强版）：
对每条信息，请提供：
1. **标题**：简洁准确的中文标题
2. **时间**：具体发布日期（格式：YYYY年MM月DD日）
3. **来源等级**：标注信息源级别
   - ⭐⭐⭐ 官方直接发布（公司官网、官方博客、GitHub官方）
   - ⭐⭐ 一线权威媒体（Reuters、Bloomberg、TechCrunch等）
   - ⭐ 专业媒体或二手源（需要交叉验证）
4. **原始链接**：直接链接到信息最初发布的地方
5. **备用链接**：如有权威媒体报道，提供作为验证
6. **摘要**：2-3句话的核心内容
7. **重要性**：1-10分评级，并说明理由
   - 8-10分：重大模型发布、巨额融资（>1亿美元）、重要政策变化
   - 6-7分：知名公司产品更新、中等融资（1000万-1亿美元）
   - 4-5分：有趣的技术进展、小额融资、行业讨论
   - 1-3分：一般性新闻、重复信息
8. **验证状态**：已验证✅ / 待确认🔄 / 存疑❓
9. **分类**：模型发布/行业动态/开源项目/深度阅读/新兴工具

**输出示例格式：**
```
**标题**：Anthropic发布Claude 4.0，性能提升50%
**时间**：2024年9月6日
**来源等级**：⭐⭐⭐ 官方直接发布
**原始链接**：https://www.anthropic.com/news/claude-4-release
**备用链接**：https://techcrunch.com/2024/09/06/anthropic-claude-4-launch （TechCrunch报道）
**摘要**：Anthropic正式发布Claude 4.0，在推理能力和代码生成方面较前版本提升50%，支持更长上下文窗口。新增多模态能力和API访问。
**重要性**：9分（重大模型发布，技术突破显著）
**验证状态**：已验证✅
**分类**：模型发布
```

请开始收集，每找到一条信息就立即输出，不要等全部找完再汇总。
```

## 第二阶段：专项深挖提示词

```markdown
# 专项信息深挖指令

基于第一阶段收集的信息，请针对以下几个重点领域进行深度挖掘：

## 深挖指令A：重要模型发布验证
请详细调研以下可能的重要模型发布，确认是否在[日期范围]内发生：
1. Anthropic Claude系列是否有更新
2. OpenAI GPT系列是否有新版本
3. Google Gemini系列是否有发布
4. 阿里Qwen系列是否有新模型
5. DeepSeek是否有新版本
6. Meta Llama系列是否有更新
7. Mistral AI是否有新模型
8. xAI Grok系列是否有更新
9. 百度文心一言是否有新版本
10. 其他知名公司的模型发布

对每个确认的发布，请提供：详细技术参数、定价信息、与前版本对比、市场反应

补充验证渠道：
- 访问各公司官方Twitter/X账号
- 检查HuggingFace热门模型页面
- 搜索"model release"关键词在tech媒体

## 深挖指令B：GitHub热门AI项目筛选
请访问GitHub Trending页面，筛选出本周星数增长最快的AI相关项目：
筛选条件：
- 项目描述包含：AI、ML、Agent、LLM、GPT、Claude等关键词
- 本周新增星数 > 100
- 活跃度高（最近有提交）

对每个项目提供：
- 项目功能简介
- 技术栈和特色
- 与现有工具的差异化
- Star数和增长趋势

## 深挖指令C：投融资和政策动态
搜索本周AI领域的重要商业动态：
关键词组合搜索：
- "AI startup funding" + [时间范围]
- "AI company acquisition" + [时间范围]
- "AI policy" + "regulation" + [时间范围]
- "AI safety" + "government" + [时间范围]
- "artificial intelligence" + "investment" + [时间范围]
- "machine learning" + "funding" + [时间范围]
- "LLM" + "startup" + [时间范围]

重点关注：
- 超过1000万美元的融资事件
- 大公司的AI相关收购
- 政府AI政策变化
- 行业联盟或标准制定
- AI安全相关法规更新
- 开源AI项目的商业化动态

补充搜索渠道：
- Crunchbase AI公司数据库
- VentureBeat AI funding专栏
- TechCrunch AI section
- 36氪人工智能频道
- IT桔子融资数据

## 深挖指令D：新兴工具和产品动态
专门搜索本周发布或更新的AI工具和产品：
关键词搜索：
- "AI tool launch" + [时间范围]
- "AI IDE" + "release" + [时间范围] 
- "AI coding assistant" + "update" + [时间范围]
- "AI agent platform" + [时间范围]
- "LLM API" + "launch" + [时间范围]

重点关注类别：
- AI编程工具（IDE、插件、CLI工具）
- AI智能体平台
- 新的AI API服务
- AI内容生成工具
- AI开发框架和库

信息收集要点：
- 工具核心功能和特色
- 定价模式（免费/付费/订阅）
- 与竞品的差异化
- 用户反馈和采用情况
- 技术架构和集成能力
```

## 第三阶段：信息整理和格式化提示词

```markdown
# 周报生成和格式化指令

现在请将收集到的所有信息整理成一份完整的AI周报。

## 整理要求：
1. **去重合并**：相同事件的多个来源要合并成一条
2. **重要性排序**：每个类别内按重要性降序排列
3. **时间验证**：确保所有事件都在指定时间范围内
4. **链接验证**：确保所有链接可访问

## 输出格式模板：

```markdown
# AI周报 [日期范围]

## 🔧 新兴工具

**[工具名称]：[一句话描述]**
[发布时间/更新时间]，[开发主体][详细描述，包括核心功能、技术特色、定价模式等]。[对行业或开发者的影响评述]。
相关链接：[官方链接]

## 🤖 模型发布

**[模型名称]：[一句话描述]**
[发布时间]，[发布主体][详细描述，包括技术参数、特色功能、定价等]。[对行业影响的评述]。
相关链接：[官方链接]

## 📰 行业动态

**[事件标题]**
[发布时间]，[详细描述，包括金额、背景、意义等]。[对行业影响的评述]。
相关链接：[新闻链接]

## 🛠️ 热门开源

https://github.com/[用户名]/[项目名]
[项目功能描述，技术特色，与同类项目的差异化优势]。本周新增Star数：[具体数字]。

## 📚 深度阅读

[文章标题]：
[文章链接]

质量检查清单：

**必需检查项：**
- [ ] 每个类别至少有3条内容
- [ ] 所有日期都在指定范围内（严格控制时间窗口）
- [ ] 链接格式正确且可访问
- [ ] 内容无重复（同一事件多个来源需合并）
- [ ] 中文表达专业且流畅
- [ ] 技术描述准确（避免夸大或误解）

**去重判断标准：**
- 同一公司同一产品的发布算作重复
- 同一融资事件的多个报道算作重复
- 同一论文的多个解读算作重复
- 不同语言的同一内容算作重复

**重要性评分参考：**
- 模型发布：GPT-5级别=10分，Claude-4级别=9分，小版本更新=6分
- 融资事件：>10亿美元=10分，1-10亿美元=8分，1000万-1亿美元=6分
- 开源项目：Star>10K且功能创新=8分，Star>1K实用工具=6分
- 政策法规：国家级重要法规=9分，行业标准=7分，公司政策=5分

特殊处理指令：

1. **如果信息不足**：
   - 明确指出哪些类别信息不足
   - 建议补充搜索的具体关键词
   - 提供备选信息源
   - 标注"信息收集不完整，建议人工补充"

2. **如果有争议信息**：
   - 标注"待确认"并详细说明争议点
   - 提供多个来源的不同表述
   - 建议进一步验证的方法
   - 注明可能的误解或传言

3. **如果链接失效**：
   - 尝试搜索替代链接（如Internet Archive、官方备用链接）
   - 标注"链接待确认"
   - 提供事件的描述性信息而非依赖链接
   - 搜索相关新闻的二次报道

4. **如果遇到访问限制**：
   - 尝试使用Web Archive或缓存版本
   - 寻找该信息的其他权威来源
   - 标注访问限制情况
   - 提供概要信息而非完整内容

**应急信息源（当主要源失效时使用）：**
- Google News搜索相关关键词
- Bing News搜索  
- 百度资讯搜索（中文信息）
- 知乎热榜相关话题
- 微博热搜相关内容

## 链接验证与质量控制流程

### 链接验证标准：
1. **优先级检查**：官方源 > 权威媒体 > 专业媒体 > 聚合源
2. **原始性验证**：确保链接指向信息的最初发布地
3. **时效性检查**：验证链接当前可访问且内容匹配
4. **交叉验证**：重要信息必须有多个独立源确认

### GitHub项目链接要求：
- 必须提供具体仓库链接，非简单描述
- 格式：https://github.com/用户名/项目名
- 附带Star数、语言、许可证信息
- 验证项目活跃度（最近提交时间）

请开始整理并生成最终周报。
```

## 📋 使用流程建议

### 最佳实践：

1. 分批执行：不要一次性运行所有提示词，建议分3次执行
2. 时间控制：每阶段给Agent充足时间（20-30分钟）
3. 结果保存：及时保存每阶段的结果，避免丢失
4. 人工审核：每阶段结束后进行人工检查和调整

### 适用工具推荐：

- Claude Code：非常适合，有强大的web search能力
- Perplexity Pro：优秀的搜索和整理能力
- ChatGPT Plus：配合Browsing功能效果很好
- Cursor：如果你在编程环境中使用

### 预期效果：

- 时间节省：从13小时减少到3-4小时
- 覆盖全面：AI搜索比人工更全面
- 质量保证：结构化提示词确保输出质量
- 可重复性：每周都可以复用相同流程

### 进阶优化：

如果效果好，可以进一步优化：
- 建立专门的信息源监控清单
- 设计更精细的重要性评分标准
- 添加趋势分析和预测功能

## 🔍 高级搜索技巧补充

### 针对不同AI Agent工具的优化建议：

**Claude Code / Perplexity Pro：**
- 使用自然语言描述搜索意图，如"找到本周发布的新AI模型"
- 利用多轮对话深入挖掘，如"这个模型与前版本有什么区别？"
- 要求提供多个来源验证重要信息

**ChatGPT Plus (Browsing)：**
- 使用具体的布尔搜索操作符：AND、OR、NOT
- 指定时间范围："after:2024-09-03 before:2024-09-09"
- 使用site:限定特定网站搜索

**通用搜索策略：**
- 关键词组合：使用"AI model" + "release" + "September 2024"
- 排除干扰词：使用-"rumor" -"speculation"排除传言
- 多语言搜索：同时搜索中英文关键词获得更全面结果

### 时间敏感搜索关键词库：

**英文时间表达：**
- "this week", "past 7 days", "September 3-9 2024"
- "announced today", "launched yesterday", "released this morning"
- "breaking news", "just released", "new announcement"

**中文时间表达：**
- "本周", "过去7天", "9月3日-9月9日"
- "今日发布", "昨日上线", "最新发布"
- "刚刚宣布", "重磅消息", "最新动态"

### 备用搜索策略：

1. **当官方网站无响应时：**
   - 搜索"公司名 + 官方公告 + 时间"
   - 查找科技媒体的二次报道
   - 使用Wayback Machine查看历史版本

2. **当信息稀缺时：**
   - 扩大搜索范围至相关关键词
   - 搜索行业专家的社交媒体评论
   - 查找学术论文和技术博客

3. **验证信息真实性：**
   - 交叉验证多个独立来源
   - 检查官方社交媒体账号确认
   - 查看是否有官方辟谣或澄清

```
