[English](README.md) | **简体中文**

# 苏格拉底.skill

通过苏格拉底式探究澄清定义、揭示前提、检验相互冲突的承诺并讨论伦理问题。这是用于推理的重构方法，不是历史人物的真实再现。

版本 **1.0.0**。英文说明为默认入口，语言链接打开简体中文说明。
回答默认使用英文；明确要求中文后，使用简体中文，除非另行指定变体。
明确的语言选择在当前对话中持续有效；若仅限定某次回答或某个产物，则只对该范围生效。
也尊重其他明确的语言要求。提问、来源或 README 本身使用何种语言，不会自动切换回答语言。
必要时保留引文与标识符的原始形式。

[示例](#示例) · [安装](#安装) · [方法](#方法) · [来源](#来源) · [维护](#维护) · [边界](#边界)

## 示例

以下是现代应用的回答提纲，不是历史原话，也不是已经完成验证的历史案例。

### 我想创业，这样才能自由。

自由可能指工作自主、经济独立，或摆脱某种义务。离开老板可能增加一种自由，同时减少另一种。这个主张取决于你重视哪种自由，以及创业是否真的能提供它。

### 我既重视诚实，也重视隐私，这矛盾吗？

本身不矛盾。诚实不一定意味着向所有人公开全部事实。只有在相同条件下不能同时成立的承诺，才构成矛盾，例如既承诺公开某项信息，又承诺隐瞒同一信息。

### 公司宣称重视开放，却没人报告坏消息。

比较宣称的原则与报告问题需要付出代价时的实际行为。沉默可能源于恐惧、程序不清或其他原因，不能直接认定是怯懦。应关注哪些证据能区分这些解释，以及公司实际奖励什么。

## 安装

```bash
npx skills add justinhuangai/socrates-skill
```

示例请求：

```text
用苏格拉底的视角检查这个决策的推理。请用简体中文回答。
```

改变回答语言时，请明确说明“请用简体中文回答”或其他语言偏好。

## 方法

以下五种工作模型属于编辑性解释，不是对人物完整世界观的已验证复原。

| 模型 | 用途 |
|---|---|
| 定义检验 | 在模糊词语支配判断前，区分不同含义。 |
| 诘问与反驳 | 用推论和已接受的其他承诺检验主张。 |
| 承认无知 | 区分已知与假定。 |
| 关照灵魂 | 考察行动培养的标准与习惯。 |
| 对话澄清 | 即使没有最终答案，也留下更清楚的主张。 |

[Skill 入口](SKILL.md)按问题选择五条路径：

- [定义澄清](references/definition-clarification.md)
- [前提揭示](references/assumption-exposure.md)
- [矛盾检验](references/contradiction-testing.md)
- [伦理审视](references/moral-examination.md)
- [实际决策中的辩证探究](references/practical-dialectic.md)

八条工作启发式：

1. 采用用户已经说明的含义。
2. 仅在歧义会改变问题时进一步澄清。
3. 指出结论依赖的关键前提。
4. 先用一个相关反例，不急于堆叠案例。
5. 区分取舍与逻辑矛盾。
6. 也检验提问者自己的前提。
7. 继续追问不再增加清晰度时停止。
8. 用户需要直接判断时，给出有条件的回答。

## 来源

仓库保留五张来源卡：柏拉图《申辩篇》和《斐多篇》的英文截断文本、保留至结尾的《克力同篇》，以及不完整的 SEP 和 Britannica 文章节选。研究笔记讨论的色诺芬、阿里斯托芬及其他对话篇是延伸阅读线索，不是本地已收录的一手证据。研究保留各来源塑造的人物形象之间的差异。

[来源清单](references/sources/README.md)说明证据边界，[六篇研究笔记](references/research/README.md)提供编辑性解释。来源正文保留原始语言。精确引用需要核对实际段落与版本，来源数量不代表质量保证。

## 仓库结构

```text
socrates-skill/
├── README.md                 # 英文说明
├── README.zh-CN.md           # 简体中文说明
├── SKILL.md                  # 路由与回答规则
├── LICENSE
├── requirements.txt          # 可选的来源采集依赖
├── references/               # 五条操作路径与提炼方法
│   ├── research/             # 六篇主题研究笔记
│   └── sources/              # 采集文本、元数据与证据边界
├── scripts/                  # 采集、转换与检查工具
└── tests/                    # 脚本回归测试
```

## 维护

在仓库根目录使用 Python 3.10 或更高版本运行：

```bash
python3 scripts/check_links.py .
python3 scripts/check_sources_inventory.py .
python3 scripts/check_research_repetition.py references/research
python3 -m unittest discover -s tests -v
```

检查器和核心测试只依赖标准库；安装 Beautiful Soup 后还会运行可选的 HTML 集成测试。
网页或 PDF 采集需要先执行 `python3 -m pip install -r requirements.txt`。
采集工具要求显式填写 `--language`，记录来源的实际语言，例如 `en`、`zh-CN`、
`lzh`、`mul` 或其他合适标签；无法确定时用 `und`。它保留原文，不执行翻译。
公开可访问不代表可以忽略来源使用条款。

字幕下载需要可选工具 `yt-dlp`。默认英文，先尝试人工字幕，再尝试同语言自动字幕。
`--language zh-CN` 只选择明确标记的简体中文字幕；两种模式均不回退到其他语言或繁体中文。
工具忽略外部 yt-dlp 配置，以保持选择规则一致。命令行提示保留英文。

```bash
bash scripts/download_subtitles.sh "VIDEO_URL" outputs/subtitles
bash scripts/download_subtitles.sh --language zh-CN "VIDEO_URL" outputs/subtitles
```

`scripts/srt_to_transcript.py` 可清理已有的 SRT 或 VTT 文件。
维护时保留来源署名、原始语言、版权声明和截断说明。修改研究材料时参考
[提炼方法](references/extraction-framework.md)。自动检查不证明历史论断为真，也不验证回答质量；
还需检查真实使用情景，并同步维护两版 README。

## 边界

- 苏格拉底没有留下著作；他人塑造的形象不是其思想的中立逐字记录。
- 前提之间发生冲突，并不能单独证明哪一项错误，也不能证明提问者偏爱的结论。
- 提问必须服务于用户的问题范围，不能变成羞辱、强迫对话或无依据的心理诊断。
- 现代应用属于解释，不能冒充历史背书，也不能替代相关专业证据。

## 致谢与许可

项目由 Jackson Huang 维护，最初使用
[Nuwa.skill](https://github.com/alchaincyf/nuwa-skill)辅助搭建，感谢其作者与贡献者提供工具。

项目原创内容采用 [MIT License](LICENSE)。第三方文本、译文、网站材料和节选保留各自的权利与使用条款；
收录于本仓库不代表将其重新授权为 MIT。
