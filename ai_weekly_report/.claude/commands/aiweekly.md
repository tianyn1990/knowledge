---
argument-hint: [开始日期] [结束日期]
description: 生成AI周报，使用并行Task Agent自动化搜索和整合
model: inherit
allowed-tools: Task, WebFetch, WebSearch, Write, Bash, Read
---

你是AI周报生成的主控制器，负责自动化调度4个专业SubAgent并行工作。

## 📅 输入参数处理
- **开始日期**: $1
- **结束日期**: $2

## 🔧 前置准备

**第一步：创建输出目录**
使用Bash工具创建reports目录（如不存在）：
```bash
mkdir -p reports
```

**第二步：日期格式转换**
将中文日期格式转换为标准格式，用于文件命名：
- 输入格式示例: "2025年9月17日"
- 输出格式示例: "2025-09-17"

## ⚠️ 重要执行说明

**每个SubAgent必须严格按照自己的配置文件执行，不能简化流程！**

## 🔄 并行执行流程

**关键：使用单个消息并行启动所有4个Task，确保真正的并行执行**

现在同时启动4个专业搜索Agent（在同一个Tool调用中）：

### Task 1: model-release-expert
你是model-release-expert。

⚠️ 重要：首先使用Read工具读取你的配置文件：
.claude/agents/model_release_expert.md

然后严格按照配置文件中的详细执行步骤，搜索$1到$2期间的AI模型发布动态。

配置文件要求你：
1. 依次访问所有指定的官方网站(OpenAI、Anthropic、Google DeepMind、Meta AI等)
2. 检查所有RSS源和API源
3. 验证社交媒体账号确认
4. 对每个发现的模型进行多源验证
5. 严格按照配置文件的输出格式要求

请执行完整的搜索流程，不要简化任何步骤。配置文件中列出了25+个具体网址，必须逐一检查。

### Task 2: industry-news-expert
你是industry-news-expert。

⚠️ 重要：首先使用Read工具读取你的配置文件：
.claude/agents/industry_news_expert.md

然后严格按照配置文件中的详细执行步骤，搜索$1到$2期间的AI行业动态和融资事件。

配置文件要求你：
1. 依次访问所有权威媒体源(Reuters、Bloomberg、华尔街日报等)
2. 检查专业AI媒体和融资数据源
3. 搜索政策监管动态
4. 多源验证重要事件
5. 严格按照配置文件的输出格式要求

请执行完整的搜索流程，配置文件中列出了30+个具体信息源，必须系统性检查。

### Task 3: opensource-expert
你是opensource-expert。

⚠️ 重要：首先使用Read工具读取你的配置文件：
.claude/agents/opensource_expert.md

然后严格按照配置文件中的详细执行步骤，搜索本周GitHub上的热门AI开源项目。

配置文件要求你：
1. 系统扫描6个GitHub Trending页面(总体、Python、TypeScript、JavaScript、Rust、Go)
2. 验证AI相关性和质量筛选
3. 收集完整的项目统计数据
4. 严格按照配置文件的输出格式要求

请执行完整的搜索流程，必须访问所有指定的Trending页面并进行质量筛选。

### Task 4: deep-reading-expert
你是deep-reading-expert。

⚠️ 重要：首先使用Read工具读取你的配置文件：
.claude/agents/deep_reading_expert.md

然后严格按照配置文件中的详细执行步骤，搜索$1到$2期间的优质AI技术文章和论文。

配置文件要求你：
1. 系统扫描学术前沿(arXiv各分类、顶级会议)
2. 访问大厂技术博客和RSS源
3. 检查专业技术媒体
4. 评估内容价值和权威性
5. 严格按照配置文件的输出格式要求

请执行完整的搜索流程，配置文件中列出了20+个具体学术和技术源，必须系统性检查。

## 📝 结果整合与验证

等待所有4个Task完成后，执行最终整合和验证：

### 🔍 结果验证步骤
**对每个SubAgent的结果进行质量检查：**

1. **完整性验证**：
   - 检查是否所有SubAgent都返回了结果
   - 验证结果格式是否符合要求
   - 确认内容数量达到最低标准

2. **质量验证**：
   - 模型发布：至少2-4个重要发布
   - 行业动态：至少3-5个重要事件
   - 开源项目：至少8-10个优质项目
   - 深度阅读：至少5-8篇高价值内容

3. **数据验证**：
   - 所有链接可访问性检查
   - 日期范围准确性验证
   - 去重处理，避免重复内容

### 🚨 错误处理机制
**如果某个SubAgent执行失败或结果不达标：**

- **模型发布专家失败**：使用WebSearch补充搜索"AI model release"
- **行业动态专家失败**：使用WebSearch补充搜索"AI funding news"
- **开源项目专家失败**：直接访问GitHub Trending页面补充
- **深度阅读专家失败**：搜索arXiv和主要技术博客补充

### 📊 数据整合要求
1. **去重**：相同事件的多个来源合并
2. **排序**：每个类别内按重要性降序
3. **验证**：确保所有链接可访问，日期在范围内
4. **格式**：使用标准markdown格式

## 📄 文件输出系统

### 🔧 文件准备步骤

**第一步：执行前置准备**
```bash
# 创建reports目录（如不存在）
mkdir -p reports
```

**第二步：日期格式标准化**
将输入的中文日期转换为ISO格式：
- 输入示例: "2025年9月17日", "2025年9月23日"
- 转换为: "2025-09-17", "2025-09-23"
- 文件名格式: `ai_weekly_2025-09-17_to_2025-09-23.md`

### 📝 双重输出机制

**1. 控制台输出（用户立即查看）**
显示完整的AI周报内容供用户立即查看和审阅

**2. 文件保存（持久化存储）**
使用Write工具将完整周报保存到文件系统：

**文件位置**: `reports/ai_weekly_[开始日期]_to_[结束日期].md`

**文件内容模板**：
```markdown
# AI周报 $1 - $2

> 生成时间: [当前时间戳]
> 文件位置: reports/ai_weekly_[日期范围].md
> 数据来源: 4个专业SubAgent并行搜索

## 🤖 模型发布
[Task 1结果：model-release-expert的搜索结果，按重要性排序]

## 📰 行业动态
[Task 2结果：industry-news-expert的搜索结果，按影响力排序]

## 🚀 开源项目
[Task 3结果：opensource-expert的搜索结果，保持编号格式]

## 📚 深度阅读
[Task 4结果：deep-reading-expert的搜索结果，按技术价值排序]

---

## 📊 生成统计
- **总耗时**: [X]分钟
- **质量评分**: [X.X]/10
- **数据覆盖**: 全球主要AI公司和研究机构
- **信息验证**: 所有链接均已验证有效性
- **SubAgent执行情况**:
  - 模型发布专家: ✅ [X]个模型发布
  - 行业动态专家: ✅ [X]个重要事件
  - 开源项目专家: ✅ [X]个优质项目
  - 深度阅读专家: ✅ [X]篇高价值内容

## 📈 本周AI趋势总结
[基于收集数据的趋势分析和洞察]
```

### ⚡ 执行时间管理

**总体时间控制**:
- 最大执行时间: 45分钟
- 各SubAgent超时设置: 12分钟
- 结果整合时间: 5分钟
- 文件生成时间: 2分钟

**超时处理**:
- 如果某个SubAgent超时，自动触发错误处理机制
- 使用WebSearch进行补充搜索
- 确保最终周报完整性

## 🚀 执行开始

**立即开始执行AI周报生成流程！**

### 步骤1: 前置准备
首先使用Bash工具创建必要目录：

### 步骤2: 并行启动SubAgent
使用Task工具在**同一个消息中**并行启动所有4个专业Agent：

1. **model-release-expert** (subagent_type: general-purpose)
2. **industry-news-expert** (subagent_type: general-purpose)
3. **opensource-expert** (subagent_type: general-purpose)
4. **deep-reading-expert** (subagent_type: general-purpose)

### 步骤3: 结果整合
等待所有Task完成后，整合结果并生成最终周报。

### 步骤4: 文件保存
将完整周报保存到reports目录，并向用户展示结果。

**重要提醒**：严格按照每个SubAgent配置文件的详细执行步骤，不要简化任何流程！