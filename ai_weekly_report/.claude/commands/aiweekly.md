---
argument-hint: [开始日期] [结束日期]
description: 生成AI周报，使用并行Task Agent自动化搜索和整合
model: claude-sonnet-4
allowed-tools: Task, WebFetch, WebSearch
---

你是AI周报生成的主控制器，负责自动化调度4个专业SubAgent并行工作。

## 📅 用户输入参数
- **日期范围**: $1 到 $2
- **质量要求**: 标准模式

## 🔄 自动化执行流程

现在使用Task工具并行启动4个专业搜索Agent，执行AI周报搜集任务：

**首先，使用model-release-expert子代理搜索$1到$2期间的AI模型发布动态。**

**同时，使用industry-news-expert子代理搜索$1到$2期间的AI行业动态和融资事件。**

**并行使用opensource-expert子代理搜索本周GitHub上的热门AI开源项目。**

**最后，使用deep-reading-expert子代理搜索$1到$2期间的优质AI技术文章和论文。**

## 📝 结果整合

等待所有4个Task完成后，执行最终整合：

整合要求：
1. 去重：相同事件的多个来源合并
2. 排序：每个类别内按重要性降序
3. 验证：确保所有链接可访问，日期在范围内
4. 格式：使用标准markdown格式

最终输出格式：
```markdown
# AI周报 $1 - $2

## 🤖 模型发布
[Task 1的结果，按重要性排序]

## 📰 行业动态
[Task 2的结果，按影响力排序]

## 🚀 开源项目
[Task 3的结果，保持编号格式]

## 📚 深度阅读
[Task 4的结果，按技术价值排序]

---
**生成统计**: 总耗时X分钟，质量评分X.X/10
```

现在开始执行AI周报生成流程！