# novel-polish-skill

网文文笔润色技能 —— 情感保真，人感优先。不流水化、不生硬，像人的润色。

适用于所有支持 SKILL.md 规范的 AI 编程助手（WorkBuddy / Trae IDE 等）。

---

## ✨ 核心哲学

不是"改得多就是好"，而是**每一处修改都过两关**：

1. **情感保真** ——原文的情绪还在吗？有没有变淡、变味、变调？
2. **人感自然** ——改完读起来像人在认真说话吗？还是像机器在优化文本？

两关都过，才改。一关不过，就撤回。

---

## 工作流

```
第一步：通读，找情绪核
       ↓
第二步：润色测评（给用户看）
       ↓
第三步：判断干预深度（微调/顺稿/润色）
       ↓
第四步：逐句动手（两问循环）
       ↓
第五步：朗读验证 + 自查清单 → 输出
```

### 关键规范

| 规范 | 说明 |
|------|------|
| **不改的底线** | 带情绪的短句、角色的个性对话、作者的情绪节奏、功能性过渡、有瑕疵但有人感的句子 |
| **神态描写专项** | 全段直接神态/肢体描写 ≤1处，善用环境烘托、他人侧写、对话弦音、行动结果 |
| **三档干预深度** | 微调(≤5%) / 顺稿(5-15%) / 润色(15-30%)，由原文质量决定 |
| **润色后自查** | 情绪变味？误改底线？神态超限？风格一致？修改率超标？全部通过才输出 |
| **多轮交互** | 支持局部重改、降档升档、版本回退、指定方向、不满意定位5种路径 |

---

## 文件结构

```
novel-polish/
├── SKILL.md                        # 核心技能文件（工作流 + 规范 + 交互）
├── README.md                       # 本文件
├── .gitignore
└── references/
    ├── polish-logic.md             # 判断脚手架（情绪/人感/直接描写/句式/放过）
    └── author-styles.md            # 热门作家风格速查（A细腻/B热血/C代入）
```

---

## 安装

### 方式一：下载 ZIP（推荐）

从 GitHub 仓库下载 ZIP 压缩包：

```
https://github.com/ahao0625/novel-polish-skill
```

点击页面右上角绿色 **Code** 按钮 → **Download ZIP**，然后解压到对应目录：

#### WorkBuddy

```bash
unzip novel-polish-skill.zip -d ~/.workbuddy/skills/
# 完成后，在 WorkBuddy 中说"帮我润色这段"即可触发
```

#### Trae IDE（项目级）

```bash
unzip novel-polish-skill.zip -d /你的项目根目录/.trae/skills/
# 完成后，在 Trae 中说"帮我润色这段"即可触发
```

### 方式二：git clone

```bash
git clone https://github.com/ahao0625/novel-polish-skill.git ~/.workbuddy/skills/novel-polish
```

---

## 与 novel-audit 联动

本技能与 `novel-audit`（网文审计）技能互补：

| 审计发现 | 传入本技能后 |
|---------|-------------|
| AI痕迹重（套路句式多） | 口语化改造 + 打破对称结构 |
| 对话同质化（分不出谁在说话） | 对话差异化 + 口语化 |
| 节奏问题（拖沓/仓促） | 节奏调整 |

---

## 风格预设

用户可预置写作风格偏好，后续自动载入：

```
【风格预设卡】
题材偏好：[都市/玄幻/历史/悬疑/通用]
节奏偏好：[快/中/慢/自动识别]
默认干预级别：[微调/顺稿/润色]
```

在 WorkBuddy 中说"帮我记住，我写都市爽文，节奏快"即可建立。

---

## ☕ 支持一下

如果这个技能对你有帮助，欢迎：

- ⭐ 给项目点个 **Star**
- ☕ 赞助一杯咖啡，鼓励持续维护

<table>
  <tr>
    <td align="center"><b>微信</b></td>
    <td align="center"><b>支付宝</b></td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/ahao0625/novel-polish-skill/main/assets/wechat-qr.png" width="200" alt="微信赞赏码"></td>
    <td><img src="https://raw.githubusercontent.com/ahao0625/novel-polish-skill/main/assets/alipay-qr.png" width="200" alt="支付宝收款码"></td>
  </tr>
</table>

---

## License

MIT
