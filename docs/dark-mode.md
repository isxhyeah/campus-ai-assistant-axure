# 深色模式实现（Axure）

- 全局变量 gTheme = "light"|"dark"
- 顶栏"主题切换"按钮 OnClick：切 gTheme 并触发 ApplyTheme
- ApplyTheme：按 Tokens 替换 surface/text/divider/card/button/气泡
- 用户气泡：Dark 模式中文本 #F5F8FF，背景 #0A84FF；AI 气泡：card 背景
