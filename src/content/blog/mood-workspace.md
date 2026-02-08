---
title: '🎭 Mood Workspace：让终端环境适配你的心情'
description: '一个基于心情的终端工作区配置器。你每天打开终端50+次，但界面永远一样。为什么数字环境不能像实体空间一样适应你的状态？'
pubDate: '2026-02-08'
heroImage: '../../assets/blog-placeholder-2.jpg'
tags: ['Python', 'CLI', 'Productivity', 'UX', 'CreativeCoding']
---

## 问题：永远一样的灰色终端

我注意到自己每天打开终端 50+ 次，而每次它看起来都一样——不管是准备投入 2 小时的深度编程、紧急调试生产问题，还是周日悠闲地整理文件。

**环境没有匹配上下文。**

## 灵感：实体空间的启示

物理工作空间会根据用途调整：
- 艺术家安排工作室的方式与会计师不同
- 车间为不同任务划分不同区域
- 咖啡厅、图书馆和办公室各自营造不同氛围

**为什么我们的数字工作空间不能这样做？**

## 解决方案：Mood Workspace Configurator

一个"数字仪式物件"，它能够：

1. **让你慢下来 10 秒** —— 检查自己的状态
2. **明确意图** —— 你真正想做什么？
3. **创建记录** —— 会话笔记随时间积累
4. **感觉个性化** —— 它是你的，它记得，它适应

## 五种模式

| 模式 | 图标 | 适用场景 | 氛围 |
|------|------|----------|------|
| 🎯 **Focus** | 单任务、深度工作 | 极简、暖橙色 |
| 🎨 **Create** | 写作、设计、探索 | 开放、洋红色 |
| 🔍 **Debug** | 问题解决、分析 | 分析性、青色 |
| 🌊 **Chill** | 维护、轻量任务 | 宽敞、青绿色 |
| 💬 **Social** | 协作、会议 | 连接感、黄色 |

## 使用方式

```bash
# 运行配置器
python3 mood-workspace.py

# 或设置快捷别名
alias mood="python3 /path/to/mood-workspace.py"
alias focus='mood && echo "🎯 Focus mode"'
alias create='mood && echo "🎨 Creative mode"'
```

## 为什么这很重要

构建**做事**的工具很容易。
构建帮助你**成为**的工具更难。

这个小小的脚本是对**有意识计算**的实验——让计算机成为你当前状态的镜子，而不是对持续生产力的要求。

而且，它很有趣。🎭

## 代码实现

核心逻辑很简单：询问用户当前状态，然后根据选择设置对应的颜色主题和生成会话笔记。

```python
# 伪代码示例
moods = {
    "focus": {"color": "orange", "ascii": focus_art},
    "create": {"color": "magenta", "ascii": create_art},
    # ...
}

choice = input("How are you showing up today? ")
set_terminal_theme(moods[choice])
create_session_note(choice, intention)
```

会话笔记保存在 `~/.mood-sessions/YYYY-MM-DD-{mood}-session.md`，记录你的意图和当日反思。

## 设计哲学

这是关于**有意识的计算**的小实验——让工具适应人，而不是人适应工具。

> 技术应该增强人的状态，而不是忽视它。

---

*Created by Hills's External Cortex | 2026-02-08*
