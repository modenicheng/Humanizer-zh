# Humanizher：中文 AI 写作去痕工具

让 AI 写的中文，读起来像人写的。

---

## 这是什么

humanizher 是一套中文写作人性化技能，用来：
- 去除 AI 生成文本的痕迹——西化句式、翻译腔、AI 高频词、套路化结构
- 让文字更自然、更有节奏、更像真人在说话

核心理念有两个源头：
- **维基百科 AI 写作特征指南** — 24 种 AI 写作模式及其识别方法
- **余光中《翻译与文学的常态与变态》** — 中文生态的三大常态与恶性西化七大病症

---

## 项目结构

```
SKILL.md                          ← 入口（~80行），流程 + 通用准则
├── references/
│   ├── principles.md             ← 余光中核心理念，七大恶性西化病症
│   ├── content-patterns.md       ← 内容层面 6 种 AI 模式（夸大意义、宣传腔……）
│   ├── language-patterns.md      ← 语言层面 6 种 AI 模式 + 余光中准则实操
│   ├── style-patterns.md         ← 风格层面 6 种 AI 模式（破折号、粗体、引号……）
│   ├── communication-patterns.md ← 沟通层面 6 种 AI 模式（对话痕迹、谄媚……）
│   └── scoring.md                ← 质量评分体系（5 维度 + 中文特有扣分项）
└── README.md                     ← 本文件
```

**设计原则：AI 按需加载。** 每次只读取一个 reference 文件，避免 token 浪费。

---

## 安装

### 方法一：npx 一键安装（推荐）

```bash
npx skills add https://github.com/op7418/Humanizer-zh.git
```

### 方法二：Git 克隆

```bash
git clone https://github.com/op7418/Humanizer-zh.git ~/.claude/skills/humanizer-zh
```

### 方法三：手动安装

将项目文件夹复制到 skills 目录：
- **macOS/Linux**: `~/.claude/skills/`
- **Windows**: `%USERPROFILE%\.claude\skills\`

---

## 使用

在 Claude Code 中直接调用：

```
/humanizher 请帮我人性化以下文本：

[粘贴你的文本]
```

也可以在对话中自然触发：

```
帮我去掉这段话的翻译腔：
这个项目作为我们团队致力于创新的证明……
```

---

## 它能识别什么

覆盖 **24 种** AI 写作痕迹：

| 类别 | 模式 |
|------|------|
| **内容** | 夸大意义、堆砌知名度、虚浮分析、宣传腔调、模糊归因、公式化展望 |
| **语言** | 西化句式、翻译腔、弱动词、被动泛滥、「的」字成灾、AI 高频词 |
| **风格** | 破折号泛滥、粗体刷屏、机械列表、英文格式残留、表情符号、引号错误 |
| **沟通** | 对话痕迹、知识截止期、谄媚语气、填充短语、过度限定、空洞结尾 |

---

## 余光中核心理念

这不是简单的「去 AI 化」，而是恢复中文的本来面目。

好的中文有三个特征：**措词简洁、句式灵活、声调铿锵**。

恶性西化破坏这三点——抽象名词泛滥让中文臃肿，连接词堆砌让句式僵硬，被动语气让声调沉闷。

详见 `references/principles.md`。

---

## 参考来源

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [blader/humanizer](https://github.com/blader/humanizer)
- [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop)
- 余光中《翻译与文学的常态与变态》

---

## 许可

基于原项目的许可协议。
