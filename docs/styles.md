# 样式与 Tokens（Apple HIG + 深色模式）

字体与排版
- 字体栈：-apple-system, BlinkMacSystemFont, "SF Pro Text", "SF Pro Display", "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans CJK SC", "PingFang SC", sans-serif
- H1 28/32 Semibold，H2 22/28 Semibold，正文 16/24 Regular，辅助 14/20

色彩 Tokens（Light/Dark）
- bg.primary: #FFFFFF / #0B0B0D
- bg.secondary: #F5F6F7 / #141416
- surface: #FFFFFF / #16171A
- card: #FFFFFF / #1B1C20
- text.primary: #111827 / #ECEEF1
- text.secondary: #6B7280 / #A1A7AF
- divider: #E5E7EB / #2A2C33
- accent: #0A84FF / #0A84FF
- success: #34C759 / #30D158
- warning: #FF9F0A / #FFD60A
- danger: #FF3B30 / #FF453A

间距：8px 基准；卡片圆角 12；气泡圆角 16；阴影低调

组件：
- 顶栏高度 64，左侧放置 assets/logo.png
- 侧栏宽 240，悬停对比 +6~8%
- 按钮：主按钮 accent，次按钮描边 divider
- 气泡：用户右侧（accent 背浅色字），AI 左侧（surface 背主文本）

动效：
- 三点思考：250ms/状态轮播
- 面板切换：150~250ms ease-in-out
