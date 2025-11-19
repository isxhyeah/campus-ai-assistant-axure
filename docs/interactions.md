# 交互设计（PC 端）

布局：
- 顶栏（Logo/搜索/主题切换/用户菜单）
- 左侧栏（模块导航与快捷操作）
- 主内容区（卡片与列表）

智能助手（03_Assistant_Chat）
- 组件：动态面板 dpChatArea、Repeater rpChat(role/text/time)、dpThinking、输入框 iptMsg、发送按钮、rpHints
- 发送流程：
  1) 校验输入 -> 空则 Toast
  2) rpChat.addRow(user 气泡)
  3) 显示 dpThinking，gLoading=1
  4) IntentDetect：关键词/FAQ 命中
  5) Wait 600~1200ms（思考中）
  6) 渲染 AI 回复与操作按钮（查看详情/去预约/打开地图）
  7) 隐藏 dpThinking，gLoading=0，清空输入
- 候选建议：输入改变时 rpHints 过滤 faqs 的 tags/question 字段，点击建议直接填充并发送

多轮上下文：gLastIntent；跨页传参：全局变量或页面变量
