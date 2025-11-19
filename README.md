# Campus AI Assistant - Axure RP 10 Prototype

基于人工智能的校园智能助手系统 - PC Web 原型（Axure RP 10 / Apple HIG / 深色模式支持）

## 项目概述

本仓库提供完整的 Axure RP 10 原型文件、设计规范、数据集和文档，用于快速构建"校园智能助手"PC Web 原型。设计遵循苹果 Human Interface Guidelines（清晰、内敛、深度），支持深浅色主题切换。

## 快速开始

1. 克隆仓库：
   ```bash
   git clone https://github.com/isxhyeah/campus-ai-assistant-axure.git
   cd campus-ai-assistant-axure
   ```

2. 使用 Axure RP 10 打开原型文件：
   - 打开 `prototype/CampusAIAssistant.rp`
   - 预览从 `02_Home_Dashboard` 或 `03_Assistant_Chat` 开始
   - 在右上角切换浅色/深色主题

## 目录结构

```
.
├── README.md                    # 项目总览（本文件）
├── .gitattributes              # Git LFS 配置（*.rp 文件）
├── .gitignore                  # Git 忽略规则
├── assets/                     # 品牌资源
│   ├── logo.svg               # 吉林大学校徽
│   └── README.md              # 资源说明
├── copy/                       # UI 文案
│   └── strings_zh.json        # 中文界面文案
├── data/                       # Repeater 数据源（CSV）
│   ├── faqs.csv               # 常见问题与意图
│   ├── courses.csv            # 课程表数据
│   ├── notices.csv            # 通知公告
│   ├── rooms.csv              # 预约房间
│   ├── canteen.csv            # 食堂菜品
│   ├── map_pois.csv           # 地图兴趣点
│   └── conversations_seed.csv # 对话种子数据
├── docs/                       # 完整文档
│   ├── README.md              # 文档总览
│   ├── IA.md                  # 信息架构
│   ├── interactions.md        # 交互设计
│   ├── styles.md              # 样式规范与 Tokens
│   ├── dark-mode.md           # 深色模式实现
│   ├── axure-build-steps.md   # Axure 构建步骤
│   ├── flows.md               # 交互流程图
│   └── qa/
│       └── test-scenarios.md  # 测试场景
└── prototype/                  # Axure 原型文件
    ├── CampusAIAssistant.rp   # 主原型文件（Git LFS）
    └── README.md              # 原型说明

```

## 核心特性

### 🎨 Apple HIG 设计风格
- **清晰（Clarity）**：清晰的视觉层次和可读性
- **内敛（Deference）**：界面不喧宾夺主，突出内容
- **深度（Depth）**：通过层次和动效增强理解

### 🌓 深色模式支持
- 完整的浅色/深色主题切换
- 遵循 Apple HIG 色彩规范
- 全局变量 `gTheme` 控制主题

### 🤖 AI 智能助手
- 自然语言理解与意图检测
- 思考中动画效果
- 候选建议实时过滤
- 多轮对话上下文管理
- 跨页面操作引导

### 📱 完整功能模块
1. **登录** - 用户认证
2. **首页仪表盘** - 今日安排、快捷操作
3. **智能助手** - AI 对话交互
4. **课程** - 课表查询与管理
5. **通知中心** - 校务公告
6. **预约** - 教室/自习室预约
7. **食堂** - 菜品浏览与筛选
8. **地图** - 校园导航
9. **报修** - 设施报修与反馈
10. **个人中心** - 设置与个性化

## 技术规范

### 设计规范
- **画布宽度**：1440px（桌面端）
- **布局**：顶栏（64px）+ 左侧栏（240px）+ 主内容区
- **字体栈**：SF Pro Text/Display, PingFang SC, 苹果系统字体
- **间距系统**：8px 基准网格
- **圆角**：卡片 12px，气泡 16px

### 色彩系统
详见 `docs/styles.md`，包含完整的 Light/Dark 模式色彩 Tokens。

### 数据导入
所有 Repeater 数据存储在 `data/*.csv`，可直接导入 Axure：
- 支持中文内容
- UTF-8 编码
- 符合 Axure Repeater 格式

## 使用指南

### 构建原型
详细步骤见 `docs/axure-build-steps.md`：
1. 创建 Masters（复用组件）
2. 设置全局变量
3. 创建页面（01-10）
4. 导入 CSV 数据
5. 实现深色模式切换
6. 配置交互逻辑

### 测试场景
按照 `docs/qa/test-scenarios.md` 验证：
- ✅ 自然语言课表查询
- ✅ 自习室智能预约
- ✅ 通知汇总与筛选
- ✅ 食堂个性化推荐
- ✅ 地图路线规划
- ✅ 报修工单流程
- ✅ 候选建议匹配
- ✅ 角色切换（教师模式）
- ✅ 兜底响应机制

## 文档导航

- **[完整文档](docs/README.md)** - 文档索引
- **[信息架构](docs/IA.md)** - 页面结构与导航
- **[交互设计](docs/interactions.md)** - 交互流程与逻辑
- **[样式规范](docs/styles.md)** - 设计 Tokens 与组件样式
- **[深色模式](docs/dark-mode.md)** - 主题切换实现
- **[构建步骤](docs/axure-build-steps.md)** - Axure 操作指南
- **[流程图](docs/flows.md)** - 意图识别流程
- **[测试场景](docs/qa/test-scenarios.md)** - 验收标准

## Git LFS

Axure `.rp` 文件使用 Git LFS 存储，避免二进制文件膨胀仓库：

```bash
# 安装 Git LFS（如未安装）
git lfs install

# 验证 LFS 配置
git lfs ls-files
```

## 贡献指南

欢迎贡献！请确保：
1. 使用 Axure RP 10（而非更早版本）
2. 遵循 Apple HIG 设计原则
3. 保持深色模式兼容性
4. 更新相关文档

## 许可证

本项目仅用于教育和演示目的。

## 联系方式

- 仓库：https://github.com/isxhyeah/campus-ai-assistant-axure
- 问题反馈：[Issues](https://github.com/isxhyeah/campus-ai-assistant-axure/issues)