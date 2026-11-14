# GitHub Topics 分类清单

一份用于给仓库打标签的 GitHub Topics 清单，按「模型底座 → 能力层 → 数据与工程 → 行业场景」四段组织：01–05 为模型与能力层，06–07 为多模态能力，08–09 为数据与工程，10 为行业场景。

> 维护规则见 [排序与维护规范](#排序与维护规范)，完整变更见 [变更映射表](#变更映射表)。

## 目录

- [01 模型与训练](#01-模型与训练-models--training)
- [02 数据集](#02-数据集-datasets)
- [03 检索增强与知识工程](#03-检索增强与知识工程-rag--knowledge)
- [04 Agent 与编排](#04-agent-与编排-agents--orchestration)
- [05 MCP 与工具链](#05-mcp-与工具链-mcp--tooling)
- [06 视觉与多模态生成](#06-视觉与多模态生成-vision--multimodal)
- [07 语音与跨模态转换](#07-语音与跨模态转换-speech--conversion)
- [08 数据、可视化与时空](#08-数据可视化与时空-data-visualization--spatiotemporal)
- [09 开发与系统](#09-开发与系统-development--systems)
- [10 垂直领域与场景](#10-垂直领域与场景-domains--use-cases)
- [排序与维护规范](#排序与维护规范)
- [变更映射表](#变更映射表)
- [待确认项](#待确认项)

---

## 01 模型与训练 Models & Training

基础模型、训练方法、评测与模型管理。

```
ai-framework
benchmark
evaluation
fine-tuning
llm
model
model-management
reinforcement-learning
research-models
sft
time-series-model
```

## 02 数据集 Datasets

数据集本体及其管理，含领域数据集。

```
data-set
dataset-management
medical-dataset
```

## 03 检索增强与知识工程 RAG & Knowledge

检索、语义匹配、知识图谱与结构化查询。

```
context-aware
embedding
information-integration
knowledge-graph
nlp
rag
semantic-retrieval
text-to-sql
web-search
```

## 04 Agent 与编排 Agents & Orchestration

通用智能体框架、编排、记忆与提示工程。

```
agent
ai-operating-system
browser-automation
build-agent
chatbot
chatbot-framework
claude-code
computer-use
development-agent
memory-management
memory-plugin
multi-agent
prompt-engineering
prompt-optimizer
skill
terminal-agent
train-agent
web-agent
windows-agent
workflow
```

## 05 MCP 与工具链 MCP & Tooling

MCP Server、命令行工具、爬虫与远程控制。

```
cli
database-mcp
git-mcp
mcp
memory-mcp
n8n-mcp
remote-control
spider
tool
web-mcp
windows-mcp
```

## 06 视觉与多模态生成 Vision & Multimodal

计算机视觉、图像/视频处理与生成。

```
3d-reconstruction
computer-vision
diffusion-model
digital-human
image-generation
image-processing
microscope
multimodal
object-detection
ocr
radar
video-generation
```

## 07 语音与跨模态转换 Speech & Conversion

```
image-to-speech
machine-translation
speech-to-text
text-to-speech
video-to-text
video-to-voice
voice-cloning
voice-to-voice
```

## 08 数据、可视化与时空 Data, Visualization & Spatiotemporal

数据治理、可视化、数据库软件与时空/图数据分析。

```
data-extraction
data-governance
data-science
data-scientist
data-visualization
database
document-parsing
gcn
gis
object-storage
spatiotemporal-data-analysis
spatiotemporal-forecasting
time-series-forecasting
vector-database
visualization
```

## 09 开发与系统 Development & Systems

应用开发、平台、网络、安全与行业信息系统。

```
application-development
code-generation
github-app-store
lims
network
security
virtualization
web-development
```

## 10 垂直领域与场景 Domains & Use Cases

按行业/场景归类的标签，含该领域专属 Agent。

### 10.1 金融 Finance

```
finance
prediction-market
quantitative-trading
trading-agent
```

### 10.2 医疗健康 Healthcare

```
medical
medical-evaluation-framework
medical-llm
medical-research-agent
```

### 10.3 生物 Biology

```
bioinformatics
biology
genomics
protein-structure-prediction
```

### 10.4 科研 Research

```
deep-research
paper-writing
paper-writing-agent
research-agent
research-development-agent
```

### 10.5 自动驾驶与机器人 Autonomy & Robotics

```
autopilot
robot
```

### 10.6 职场与效率 Work & Productivity

```
bid
find-job
office
product-manager
working
```

### 10.7 学习 Learning

```
awesome-list
language-learning
study-material
```

### 10.8 情报与舆情 Intelligence & OSINT

开源情报、新闻聚合与舆情情感分析。

```
news-monitoring
osint
sentiment-analysis
```

---

## 排序与维护规范

1. **一级分类固定编号 01–10**，按认知链路排列：模型底座(01) → 数据集(02) → 检索能力(03) → Agent 能力(04) → 工具链(05) → 视觉与多模态生成(06) → 语音与跨模态转换(07) → 数据可视化与时空(08) → 开发与系统(09) → 行业应用(10)。不按字母序，也不按添加时间。
2. **组内一律按字母序（A→Z）**，数字开头的 slug（如 `3d-reconstruction`）排在组首。便于查找、code review 和脚本 diff。
3. **每个 slug 只出现一次**；跨领域标签按其最核心语义归组，领域专属 Agent 归 10。
4. **命名统一**：全小写 kebab-case，只含 `a-z` `0-9` `-`，不含空格、不含尾随空格；长度**建议 ≤ 35 字符**（GitHub Topics **官方上限 50 字符**），**每个仓库最多 20 个 topics**。单一概念一律用单数（`agent`、`build-agent`、`train-agent`、`study-material`），复数仅用于表示集合类的标签（如 `research-models`、`visualization-models`）。
5. **语义边界**：`data-set` / `*-dataset` / `dataset-management` 表示数据集，归 02；`database` / `*-mcp` 表示数据管理软件，归 08 / 05；`research-*` 等科研 Agent 归 10.4，不放 04。`diffusion-model` 等模型架构归 01、生成任务归 06；`data-science`（学科）/ `data-scientist`（角色）/ `database`（软件）/ `data-visualization`（任务）为不同实体类型，08 组内按此区分；`computer-use` 表示 GUI/OS 级计算机操作 Agent，与 `terminal-agent`（命令行）、`browser-automation`（浏览器）并列但不等同。
6. **清单定位与新增流程**：清单是**标准词表**，不是线上标签的镜像。新增 slug 以「是否有通用检索价值」为准，**允许暂时零使用**，不必先有仓库在用。流程：先判断归属组 → 检查是否与已有 slug 重复或同义 → 插入组内字母序位置 → 在变更映射表登记（含基线 commit 与前后位置）。
7. **格式**：组内用纯文本代码块，一行一个 slug，方便直接复制去 GitHub 打标签；不再使用 `<br>` 硬换行。
8. **打标执行**：每个仓库尽量 **3–6 个标签**，精简兼顾覆盖；**禁止同义标签并列**（如 `rag` 与全称、`text-to-speech` 与 `tts`）；新增标签优先用于修正内容错配，不要为凑数硬套 `tool` 等泛标签；仓库应补全 `description` 与 README 的中文一句话简介。**禁止把固定标签组合成套套用**（如 `development-agent`+`research-agent`+`research-development-agent`、`data-extraction`+`data-governance`、`finance`+`quantitative-trading`+`trading-agent`）；每个标签都应能在 description 或 README 首段找到依据。

## 变更映射表

### 版本基线

映射表以原始清单的最后一个提交为基线，向下累计维护，不覆盖历史记录：

| 阶段 | commit | 内容 |
| --- | --- | --- |
| 基线 | `046449535bede44cb34aacbb5e4598fea8afd84e` | 原始 115 行平铺清单，无分类 |
| 第一轮 | `5c8bce24075f78aa70836bbf71147d31e087d89c` | 9 大分类、108 个规范 slug |
| 第二轮 | `fd761143016f10d611427e27c8f8e2fbc102b5ca` | 10 大分类；数据集、生物、科研、学习拆分；1 处改名 |
| 第三轮 | 2026-11-12 账号标签核对 | 补齐 6 个账号在用但清单外标签，108 → 114 个 slug |
| 第四轮 | 2026-11-12 项目名/笔误标签清理 | 移除 4 个项目名与连写笔误标签，114 → 110 个 slug；同步调整 4 个仓库的线上 Topics |
| 第五轮 | 2026-11-13 规范与命名修订 | 修正官方限制表述、断链锚点与统计口径；5 处 slug 改名（单复数统一 + 连写修正），slug 总数仍为 110 |
| 第六轮 | 2026-11-13 清单瘦身（P1） | 合并 3 个冗余/同义 slug、4 处改名、`translation` 移组，110 → 107 个 slug |
| 第七轮 | 2026-11-13 清单增补（P2） | 按账号收藏方向补 16 个通用主题、新增 10.8 子组，107 → 123 个 slug；线上 Topics 不变 |
| 第八轮 | 2026-11-13 打标执行（P3） | 新增打标执行规范第 8 条；58 个仓库标签精简、19 个 description、13 个 README 简介补齐；清单仍 123 个 slug |
| 第九轮（本版） | 2026-11-13 词表修订与线上打标 | 新增 5 个 slug、改名迁移 1 个、合并下线 1 个，123 → 127 个；P1 追加 102 处、P0 下线 122 处错配并补 65 处、P2 试打标 38 处与旧 slug 同步 8 处 |

完整差异：[compare 0464495...main](https://github.com/zhangchenhaobest/github-topics/compare/046449535bede44cb34aacbb5e4598fea8afd84e...main)

### A. 基线 → 第一轮：命名与去重

| 类型 | 原值 | 新值 | 说明 |
| --- | --- | --- | --- |
| 去重 | `working` ×2 | `working` ×1 | 原第 67、78 行重复 |
| 单复数 | `llms` | `llm` | 统一单数 |
| 单复数 | `models` | `model` | 统一单数 |
| 单复数 | `tools` | `tool` | 统一单数 |
| 单复数 | `medical-llms` | `medical-llm` | 统一单数 |
| 单复数 | `medical-databases` | `medical-database` | 统一单数，第二轮再改为 `medical-dataset` |
| 单复数 | `time-series-models` | `time-series-model` | 统一单数 |
| 非法 slug | `spatiotemporal forecasting` | `spatiotemporal-forecasting` | 原值含空格，**不是合法 GitHub topic** |
| 格式修正 | `translation ` | `translation` | 去除尾随空格 |
| 格式修正 | 每行末尾 `<br>` | Markdown 代码块 | 原文件用 HTML 换行，不利于脚本读取 |

### B. 第一轮 → 第二轮：分类迁移与改名

| 类型 | slug | 原位置 | 新位置 | 说明 |
| --- | --- | --- | --- | --- |
| 拆分新建 | `data-set` | 01 模型与训练 | **02 数据集** | 数据集独立成组 |
| 拆分新建 | `dataset-management` | 01 模型与训练 | **02 数据集** | 同上 |
| 改名 + 迁移 | `medical-database` → `medical-dataset` | 09.2 医疗健康 | **02 数据集** | 语义是数据集而非数据库软件；基线链路 `medical-databases` → `medical-database` → `medical-dataset` |
| 领域重归 | `research-agent` | 03 Agent 与编排 | **10.4 科研** | 科研类 Agent |
| 领域重归 | `research-development-agent` | 03 Agent 与编排 | **10.4 科研** | 科研类 Agent |
| 拆分组 | `biology` | 09.3 生物与科研 | **10.3 生物** | 生物与科研拆开 |
| 拆分组 | `paper-writing` | 09.3 生物与科研 | **10.4 科研** | 同上 |
| 拆分组 | `paper-writing-agent` | 09.3 生物与科研 | **10.4 科研** | 同上 |
| 独立成组 | `study-materials` | 09.3 生物与科研 | **10.7 学习** | 学习独立 |
| 独立成组 | `language-learning` | 09.3 生物与科研 | **10.7 学习** | 学习独立 |
| 迁移 | `lims` | 09.3 生物与科研 | **09 开发与系统** | 实验室信息系统属软件 |
| 迁移 | `office` | 08 开发与系统 | **10.6 职场与效率** | 办公场景 |
| 确认保留 | `security` | 08 开发与系统 | 09 开发与系统 | 本就在系统组，仅编号顺延 |
| 确认保留 | `bid` | 09.5 职场与效率 | 10.6 职场与效率 | 本就在职场组，仅编号顺延 |
| 确认保留 | `database` | 07 数据、可视化与时空 | 08 数据、可视化与时空 | 数据管理软件，与数据集区分，仅编号顺延 |

### C. 编号迁移

| 第一轮 | 第二轮起 | 分类 |
| --- | --- | --- |
| 01 | 01 | 模型与训练 |
| — | **02** | 数据集（新增） |
| 02 | 03 | 检索增强与知识工程 |
| 03 | 04 | Agent 与编排 |
| 04 | 05 | MCP 与工具链 |
| 05 | 06 | 视觉与多模态生成 |
| 06 | 07 | 语音与跨模态转换 |
| 07 | 08 | 数据、可视化与时空 |
| 08 | 09 | 开发与系统 |
| 09 | 10 | 垂直领域与场景 |
| 09.1 | 10.1 | 金融 |
| 09.2 | 10.2 | 医疗健康 |
| 09.3 | **10.3 / 10.4 / 10.7** | 生物与科研 → 拆为生物、科研、学习 |
| 09.4 | 10.5 | 自动驾驶与机器人 |
| 09.5 | 10.6 | 职场与效率 |

### D. 第二轮 → 第三轮：补齐账号在用标签

对照账号全部仓库的线上 Topics，把「仓库在用、清单未登记」的 6 个标签全部纳入主清单，清单 108 → 114。其中 4 项（`secretary`、`githubdaily`、`omnipartser`、`toolutility`）已在第四轮移除，见下方 F 节；本表保留作为历史记录。

| 标签 | 实际频次 | 所在仓库 | 纳入分组 | 备注 |
| --- | ---: | --- | --- | --- |
| `data-science` | 1 | agents | 08 数据、可视化与时空 | 通用学科标签 |
| `web-search` | 1 | Agent-Reach | 03 检索增强与知识工程 | 通用能力标签 |
| `secretary` | 1 | MineContext | 10.6 职场与效率 | 通用场景标签 |
| `githubdaily` | 1 | GitHubDaily | 09 开发与系统 | 项目名 |
| `omnipartser` | 1 | OmniParser | 06 视觉与多模态生成 | 项目名 |
| `toolutility` | 1 | marin | 05 MCP 与工具链 | 疑为 `tool` + `utility` 连写笔误，待后续修正 |

数据口径（第三轮历史快照，2026-11-12 18:00）：618 个仓库 / 614 个带标签 / 1786 次打标。纳入后清单 114 个 slug 与账号 114 个在用标签**双向零差异**。

**第五轮盘点快照**（2026-11-13 早间，公开仓库、未登录态）：**609 个仓库 / 605 个带标签 / 1774 次打标 / 110 个在用标签**，清单 110 个 slug 与之双向零差异。历史快照与当前实测的差额来自统计时点与仓库可见范围，私有仓库不在口径内；**当前口径以 K 节为准**。

### E. 保留但建议后续合并的同义词

前两对已在第六轮合并（见 H 节）；其余保留，避免已有仓库标签失效：

| 主标签 | 同义/冗余标签 | 建议 |
| --- | --- | --- |
| `rag` | `retrieval-augmented-generation` | **第六轮已合并**：保留 `rag`，全称下线 |
| `ocr` | `optical-character-recognition` | **第六轮已合并**：保留 `ocr`，全称下线 |
| `visualization` | `data-visualization`、`visualization-models` | **第九轮已合并** `visualization-models` → `visualization`；`visualization` 与 `data-visualization` 语义有差别，继续保留 |
| `data-set` | `dataset-management` | 同属 02 数据集，一个指本体一个指管理，暂保留 |

### F. 第三轮 → 第四轮：清理项目名与笔误标签

第三轮补齐的 6 个标签中，2 个是项目名（其中 `omnipartser` 为误拼）、1 个是 `tool` + `utility` 连写笔误、1 个是过窄的场景标签，作为通用主题检索价值低。本轮从清单移除，并把对应仓库的 Topics 改为清单内已有的通用标签，**不新增任何 slug**。

| 移除标签 | 原分组 | 类型 | 关联仓库 | 该仓库新 Topics |
| --- | --- | --- | --- | --- |
| `secretary` | 10.6 职场与效率 | 过窄的场景标签 | MineContext | `office`, `research-agent` |
| `githubdaily` | 09 开发与系统 | 项目名 | GitHubDaily | `study-materials` |
| `omnipartser` | 06 视觉与多模态生成 | 项目名（且为 `OmniParser` 误拼） | OmniParser | `computer-vision`, `web-agent` |
| `toolutility` | 05 MCP 与工具链 | `tool` + `utility` 连写笔误 | marin | `utility`, `research-development-agent`, `tool` |

四个标签在账号内各只出现 1 次，移除后清单与账号在用标签恢复双向零差异：114 → 110 个 slug。各分组内部字母序保持不变。

### G. 第四轮 → 第五轮：规范修订与命名统一

本轮只做规范与命名修订，**不增删 slug 总数**（仍为 110 个）。历史映射表 A–F 中的旧值保留原样，仅记录当时的真实状态。

| 类型 | 原值 | 新值 | 说明 |
| --- | --- | --- | --- |
| 连写修正 | `objectstorage` | `object-storage` | 与第四轮清理 `toolutility` 采用同一标准 |
| 单复数统一 | `agents` | `agent` | 单一概念用单数 |
| 单复数统一 | `build-agents` | `build-agent` | 同上 |
| 单复数统一 | `train-agents` | `train-agent` | 同上 |
| 单复数统一 | `study-materials` | `study-material` | 同上；`research-models`、`visualization-models` 属集合类，保留复数 |
| 规范纠正 | 长度 ≤ 35 字符（GitHub 硬性要求） | 建议 ≤ 35 字符，**官方上限 50 字符** | 依据 GitHub 官方文档 |
| 规范补充 | — | 每个仓库最多 20 个 topics | 依据 GitHub 官方文档 |
| 文档修复 | `#08-…data--visualization--spatiotemporal` | `#08-…data-visualization--spatiotemporal` | 断链锚点，共 2 处 |
| 文档修复 | 盘点快照文件的悬空引用 | 删除该引用 | 仓库内不存在该文件 |
| 口径更新 | 618 / 614 / 1786 | 609 / 605 / 1774 / 110（2026-11-13，公开仓库、未登录态） | 原数字保留为第三轮历史快照 |

5 处改名需同步更新线上仓库 Topics，涉及原标签 `agents` 40 次、`build-agents` 4 次、`train-agents` 2 次、`study-materials` 74 次、`objectstorage` 2 次打标。

### H. 第五轮 → 第六轮：清单瘦身（P1）

本轮合并 100% 共现的同义/冗余标签、统一 07 组术语，并把 `translation` 移出跨模态组。历史映射表 A–G 中的旧值保留原样。

| 类型 | 原值 | 新值 | 涉及打标 | 说明 |
| --- | --- | --- | ---: | --- |
| 同义合并 | `retrieval-augmented-generation` | `rag` | 21 | 21/21 完全共现，零损失 |
| 同义合并 | `optical-character-recognition` | `ocr` | 9 | 9/9 完全共现，零损失 |
| 冗余合并 | `utility` | `tool` | 129 | `utility` 从不单独出现，129 次全部伴随 `tool` |
| 术语统一 | `text-to-voice` | `text-to-speech` | 5 | 对齐社区通用 TTS 命名 |
| 术语统一 | `voice-to-text` | `speech-to-text` | 5 | 对齐社区通用 ASR 命名 |
| 术语统一 | `picture-to-voice` | `image-to-speech` | 1 | `image` / `speech` 与全组一致 |
| 改名 + 迁移 | `translation`（07） | `machine-translation`（**03**） | 1 | 文本→文本不属跨模态转换 |

未选择「`tool` / `utility` 一并下线」：实测会让 33 个仓库变成零标签，且需引入清单外的 `automation`，与瘦身目标冲突；本轮先消除 100% 冗余，`tool` 本身的宽泛性留作后续项。

**本轮结果**：移除 3 个 slug、改名 4 处、迁移 1 处，清单 110 → **107 个 slug**；线上打标 1774 → **1615 次**。

### I. 第六轮 → 第七轮：清单增补（P2）

本轮按账号 609 个公开仓库的实际收藏方向（description + README 关键词盘点）补入通用主题，**允许暂时零使用**：清单自此是标准词表，不再是线上标签的镜像。**本轮不改动任何线上 Topics**。

| 新增 slug | 归入分组 | 内容命中仓库数 | 依据 / 用途 |
| --- | --- | ---: | --- |
| `benchmark` | 01 | 41 | 基准/榜单类项目，与 `evaluation`（评测方法）区分 |
| `fine-tuning` | 01 | 42 | 微调 / LoRA，补齐 `sft` 之外的通用训练方法 |
| `embedding` | 03 | 19 | 向量化与语义检索底座 |
| `browser-automation` | 04 | 20 | 浏览器 / 计算机操作类 Agent |
| `diffusion-model` | 06 | 6 | 扩散模型 |
| `image-generation` | 06 | 11 | 文生图 / 图像生成 |
| `voice-cloning` | 07 | 3 | 声音克隆，与 TTS / ASR 区分 |
| `vector-database` | 08 | 12 | 向量数据库属数据管理软件，按规范第 5 条归 08 而非 03 |
| `code-generation` | 09 | 54 | AI 编码 / 代码生成 |
| `prediction-market` | 10.1 | 3 | 预测市场，此前被笼统归入 `quantitative-trading` |
| `bioinformatics` | 10.3 | 11 | 生物信息学，替代 AlphaFold 系列误打的 `medical-*` |
| `protein-structure-prediction` | 10.3 | 3 | 蛋白质结构预测 |
| `awesome-list` | 10.7 | 37 | 资源列表类仓库，此前多被硬套 `study-material` |
| `news-monitoring` | **10.8（新增）** | 9 | 新闻 / 热点聚合监控 |
| `osint` | **10.8（新增）** | 10 | 开源情报 |
| `sentiment-analysis` | **10.8（新增）** | 8 | 舆情情感分析 |

新增子组 **10.8 情报与舆情**，用于承接此前误套到 10.1 金融组的一批资讯 / 情报 / 监控类项目。

**未采纳的高频泛词**（命中高，但会重演 `tool` / `utility` 的泛化问题或与已有 slug 同义）：`automation` 78（已有 `workflow`）、`docker` 72、`documentation` 47、`tutorial` 65（已有 `study-material`）、`self-hosted` 36、`tts` / `asr`（已有 `text-to-speech` / `speech-to-text`）、`market-intelligence`（并入 10.8）；`genomics` 已于第九轮采纳为独立 slug，见 K 节。

**本轮结果**：清单 107 → **123 个 slug**（新增 16 个），子组 7 → 8；线上 Topics 未改动，仍为 609 个公开仓库 / 1615 次打标 / 109 个在用标签（清单中在用的 107 个 slug + 2 个 DMCA 残留）。新增 16 个 slug 暂时零使用，留待后续打标时优先用于修正审计报告 3.2 / 3.3 节的错配。

### J. 第七轮 → 第八轮：打标执行（P3）

本轮把清单落到线上：新增规范第 8 条，按「3–6 个标签、禁止同义并列」精简标签，并补齐仓库元数据。**清单 slug 数不变（123 个）**。

| 动作 | 计划 | 实际完成 | 说明 |
| --- | ---: | ---: | --- |
| Topics 调整 | 59 | **58** | 含 4 个零标签补齐、3.2 / 3.3 / 3.4 错配修正、22 个 ≥7 标签仓库精简；`n8n-workflows` 因 DMCA 451 失败 |
| `description` 补齐 | 19 | **19** | 全部为中文一句话简介；执行后无 description 的仓库为 0 |
| README 简介补齐 | 21 | **14** | 6 个复核发现已有完整 README（7–83 KB），未覆盖；2 个 DMCA 仓库无法写入；第九轮实测含补齐标记为 14 个 |

**标签分布变化**：≥7 个标签的仓库 **22 → 0**；3–6 个标签的仓库 228 → **269**；打标 1615 → **1565 次**；严格同义并列（`rag`+全称、`ocr`+全称、`tool`+`utility`、`text-to-speech`+`tts`）均为 **0**。清单 16 个零使用标签中 **15 个已落地**（`awesome-list`、`osint`、`news-monitoring`、`sentiment-analysis`、`bioinformatics`、`vector-database` 等），仅 `voice-cloning` 仍零使用。**注**：「已落地」仅表示非零使用；第九轮实测 `benchmark`、`fine-tuning`、`code-generation`、`embedding`、`vector-database` 当时各仅 1 次，覆盖率不足，已在 K 节 P1 阶段补齐。

**未强行补足**：339 个仓库仍只有 1–2 个标签。规范用「尽量 3–6 个」而非硬性下限，避免为凑数引入不准确标签，留待按项目内容逐步补充。

**盘点口径修正**：最初记录的「21 个无 README」中有 6 个是 raw 域名抓取时的网络失败导致的误判（仓库实际有完整 README），本轮已复核并**保留原文件、未覆盖**；真正缺失的 13 个已补中文简介。第九轮全量复核（607/609 抓取成功，2 个失败均为 DMCA 屏蔽仓库）验证了该修正。

**执行后线上**（609 个公开仓库）：唯一标签 **124 个** = 清单中在用的 122 个 + 2 个 DMCA 残留旧名；清单独有 **1 个**（`voice-cloning`，符合规范第 6 条）；零标签仓库 1 个（`n8n-workflows`，平台封禁）。

**统计**：基线 115 行（114 个唯一值）→ 110 个规范 slug（前两轮规范化后 108，第三轮补齐 6 个，第四轮移除 4 个）；一级分类 9 → 10，子组 5 → 7；第二轮改名 1 处、迁移 11 处、确认保留 3 处；第三轮新增 6 处；第四轮移除 4 处；第五轮改名 5 处、规范与文档修订 5 项，slug 总数不变；第六轮合并 3 个、改名 4 处、迁移 1 处，110 → 107 个 slug；第七轮新增 16 个 slug、子组 7 → 8，107 → 123 个 slug（其中 16 个暂时零使用）；第八轮新增打标执行规范、58 个仓库标签精简、19 个 description 与 13 个 README 简介补齐，slug 总数不变；第九轮新增 5 个 slug、改名迁移 1 个、合并下线 1 个，123 → **127 个**，一级分类结构自第二轮起未再变动。

### K. 第八轮 → 第九轮：按内容落地与词表修订

本轮按「**P1 把已有精准词用起来 → P0 清掉错配标签并用精准词替换 → P2 改词表并登记**」的顺序执行，全部线上变更经 `description` + README 首段核验，逐仓库明细见审计目录 `p1-plan.csv` / `p0-plan.csv`。

| 阶段 | 动作 | 覆盖范围 |
| --- | --- | ---: |
| P1 | 追加清单内已有但几乎未落地的精准标签（只认 description 级强证据，逐条人工复核） | **93 个仓库 / 102 次追加** |
| P0 | 下线语义错配标签，用清单内精准词替换，并给删到只剩 1 个标签的仓库补词 | **94 个仓库 / 删除 122 次、追加 65 次** |
| P2 | 词表结构调整、规范修订、文档自洽性修订与变更登记 | 123 → **127 个 slug** |

**新增 5 个通用 slug**（按仓库实际内容命中补入，字母序插入）：

| slug | 归组 | 用途 / 承接的错配 |
| --- | --- | --- |
| `computer-use` | 04 | GUI/OS 级计算机操作 Agent，承接 `cua` / `Agent-S` / `OS-Copilot` 等被误打成 `terminal-agent` 的项目 |
| `multimodal` | 06 | 06 组名含「多模态」但此前无对应 slug |
| `document-parsing` | 08 | PDF / 文档解析，替换被误打 `data-governance` 的 `MinerU`、`docling`、`olmocr` 等 |
| `genomics` | 10.3 | 基因组学，第七轮曾并入 `bioinformatics`，实测该词仅 6 次使用而内容命中更多，独立成词 |
| `deep-research` | 10.4 | 深度调研能力，与泛化的 `research-agent` 区分 |

**改名迁移 1 处**：`time-series-forecasting-pipeline`（01）→ `time-series-forecasting`（**08**），统一 01/08 的时序主题，去掉与 `workflow` 撞车的 `pipeline`。
**合并下线 1 处**：`visualization-models`（仅 3 次、含义模糊）→ `visualization`。

**线上错配清理结果**（执行前 → P0 后）：

| 标签 | 执行前 | P0 后 | 说明 |
| --- | ---: | ---: | --- |
| `data-governance` | 33 | **0** | 全部为抽取/爬虫/解析/问数项目误用，保留 slug 并收紧语义边界 |
| `prompt-optimizer` | 19 | **2** | 仅保留 `prompt-optimizer`、`AI-Gist`，其余改 `awesome-list` / `prompt-engineering` |
| `development-agent` | 71 | **41** | 下线 30 处无编码迹象的模板化打标 |
| `research-development-agent` | 25 | **15** | 下线 10 处通用 Agent 框架 |
| `paper-writing-agent` | 17 | **13** | 下线 4 处错配 |
| `awesome-list` | 7 | **33** | 资源列表类仓库改用精准词 |
| `voice-cloning` | 0 | **2** | 零使用清零 |

**执行后线上口径**（P0 完成时）：**608 个带标签 / 1610 次打标 / 124 个唯一标签**；1–2 标签仓库 339 → **308**，3–6 标签仓库 269 → **300**。

**最终线上口径**（P2 试打标与旧 slug 同步完成后，609 个公开仓库）：**608 个带标签 / 1645 次打标 / 128 个唯一标签** = 清单 127 个 slug 中在用的 126 个 + 2 个 DMCA 旧名残留；1–2 标签仓库 339 → **299**，3–6 标签仓库 269 → **309**；标签数 ≥7 与严格同义并列均为 **0**。清单独有零使用 1 个（`data-governance`，按规范第 6 条保留）；线上独有 2 个仍为 DMCA 旧名，见「已知例外」。词表与线上双向对齐，全部差异均可解释。

**新增 5 个 slug 的线上试打标**已在登记后完成：38 个仓库 / 38 次追加（`computer-use` 12、`document-parsing` 7、`genomics` 5、`deep-research` 6、`multimodal` 8），明细见 `p2-plan.csv`；另同步 8 个仓库的旧 slug 改名与合并（`time-series-forecasting-pipeline` → `time-series-forecasting` 5 处、`visualization-models` → `visualization` 3 处），明细见 `p2b-plan.csv`。

## 待确认项


- `tool` 仍过于宽泛（134 次，原 `utility` 已于第六轮并入），检索价值低；第九轮未批量替换，需逐个补具体标签，暂列后续项。
- E. 节 `visualization` / `data-visualization` 与 `data-set` / `dataset-management` 两组语义有差别，确认后再决定是否合并；`visualization-models` 已于第九轮合并下线。
- `data-governance` 线上已清零，slug 按规范第 6 条保留为零使用标准词，后续仅用于真正的数据治理项目。
- **308 个仓库**仍只有 1–2 个标签，未按「3–6 个」硬性下限强行补齐，后续按项目内容逐步补充。
- `n8n-workflows` 因 DMCA 屏蔽无法打标签或补 README，见文末「已知例外」。

## 已知例外

- **`agentic-design-patterns-cn`**：因 DMCA 版权限制（GitHub 于 2026-03-05 依据 Springer Nature 的投诉屏蔽该仓库，API 返回 `451 Repository access blocked`），账号无法修改该仓库的 Topics。第五轮单复数改名后，该仓库仍保留旧标签 `agents`、`study-materials`。
- **`n8n-workflows`**：因 DMCA 版权限制（GitHub 于 2025-08-26 屏蔽，API 同样返回 `451 Repository access blocked`），账号无法修改该仓库的 Topics 或补 README，是账号内唯一零标签仓库。

因此第九轮 P0 完成时线上在用标签为 **124 个** = 清单中在用的 122 个 slug + 上述 2 个残留旧名；当时清单共 **123 个 slug**，仅 `voice-cloning` 按规范第 6 条暂时零使用。第九轮改词表后清单为 **127 个 slug**，其中仅 `data-governance` 按第 6 条保留零使用，新增 5 个 slug 已于 P2 阶段试打标落地，见 K 节。上文 D 节的「双向零差异」为第五轮执行前的盘点快照，此后以本例外与规范第 6 条为准。以上均为平台限制导致，不影响清单本身的有效性。
