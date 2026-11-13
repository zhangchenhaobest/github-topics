# GitHub Topics 分类清单

一份用于给仓库打标签的 GitHub Topics 清单，按「技术底座 → 能力层 → 应用场景」组织。

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

基础模型、训练方法、评测与模型管理。数据集相关标签已拆分至 [02 数据集](#02-数据集-datasets)。

```
ai-framework
evaluation
llm
model
model-management
reinforcement-learning
research-models
sft
time-series-forecasting-pipeline
time-series-model
```

## 02 数据集 Datasets

数据集本体及其管理，含领域数据集。**与数据管理软件 `database` 不是一类**：`data-set` 是数据集，`database` 是数据库软件，归 [08](#08-数据可视化与时空-data-visualization--spatiotemporal)。

```
data-set
dataset-management
medical-dataset
```

## 03 检索增强与知识工程 RAG & Knowledge

检索、语义匹配、知识图谱与结构化查询。

```
context-aware
information-integration
knowledge-graph
nlp
rag
retrieval-augmented-generation
semantic-retrieval
text-to-sql
web-search
```

## 04 Agent 与编排 Agents & Orchestration

通用智能体框架、编排、记忆与提示工程。领域专属 Agent 归入 [10](#10-垂直领域与场景-domains--use-cases)，科研类 Agent 归 [10.4 科研](#104-科研-research)。

```
agent
ai-operating-system
build-agent
chatbot
chatbot-framework
claude-code
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
utility
web-mcp
windows-mcp
```

## 06 视觉与多模态生成 Vision & Multimodal

计算机视觉、图像/视频处理与生成。

```
3d-reconstruction
computer-vision
digital-human
image-processing
microscope
object-detection
ocr
optical-character-recognition
radar
video-generation
```

## 07 语音与跨模态转换 Speech & Conversion

语音、文本、图像、视频之间的相互转换。

```
picture-to-voice
text-to-voice
translation
video-to-text
video-to-voice
voice-to-text
voice-to-voice
```

## 08 数据、可视化与时空 Data, Visualization & Spatiotemporal

数据治理、可视化、数据库软件与时空/图数据分析。`database` 在此表示**数据管理软件**；数据集见 [02](#02-数据集-datasets)。

```
data-extraction
data-governance
data-science
data-scientist
data-visualization
database
gcn
gis
object-storage
spatiotemporal-data-analysis
spatiotemporal-forecasting
visualization
visualization-models
```

## 09 开发与系统 Development & Systems

应用开发、平台、网络、安全与行业信息系统。

```
application-development
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
quantitative-trading
trading-agent
```

### 10.2 医疗健康 Healthcare

医疗领域数据集 `medical-dataset` 已归 [02 数据集](#02-数据集-datasets)。

```
medical
medical-evaluation-framework
medical-llm
medical-research-agent
```

### 10.3 生物 Biology

```
biology
```

### 10.4 科研 Research

科研写作与科研智能体，含通用 Agent 中拆出的 `research-*` 标签。

```
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

学习资料与语言学习，从原「生物与科研」独立。

```
language-learning
study-material
```

---

## 排序与维护规范

1. **一级分类固定编号 01–10**，按认知链路排列：模型底座 → 数据集 → 检索能力 → Agent 能力 → 工具链 → 多模态 → 数据 → 工程 → 行业应用。不按字母序，也不按添加时间。
2. **组内一律按字母序（A→Z）**，数字开头的 slug（如 `3d-reconstruction`）排在组首。便于查找、code review 和脚本 diff。
3. **每个 slug 只出现一次**；跨领域标签按其最核心语义归组，领域专属 Agent 归 10。
4. **命名统一**：全小写 kebab-case，只含 `a-z` `0-9` `-`，不含空格、不含尾随空格；长度**建议 ≤ 35 字符**（GitHub Topics **官方上限 50 字符**），**每个仓库最多 20 个 topics**。单一概念一律用单数（`agent`、`build-agent`、`train-agent`、`study-material`），复数仅用于表示集合类的标签（如 `research-models`、`visualization-models`）。
5. **语义边界**：`data-set` / `*-dataset` / `dataset-management` 表示数据集，归 02；`database` / `*-mcp` 表示数据管理软件，归 08 / 05；`research-*` 等科研 Agent 归 10.4，不放 04。
6. **新增流程**：先判断归属组 → 检查是否与已有 slug 重复或同义 → 插入组内字母序位置 → 在变更映射表登记（含基线 commit 与前后位置）。
7. **格式**：组内用纯文本代码块，一行一个 slug，方便直接复制去 GitHub 打标签；不再使用 `<br>` 硬换行。

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
| 第五轮（本版） | 2026-11-13 规范与命名修订 | 修正官方限制表述、断链锚点与统计口径；5 处 slug 改名（单复数统一 + 连写修正），slug 总数仍为 110 |

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

**当前实测口径**（2026-11-13，公开仓库、未登录态）：**609 个仓库 / 605 个带标签 / 1774 次打标 / 110 个在用标签**，清单 110 个 slug 与之双向零差异。历史快照与当前实测的差额来自统计时点与仓库可见范围，私有仓库不在当前口径内。

### E. 保留但建议后续合并的同义词

本版未删，避免已有仓库标签失效：

| 主标签 | 同义/冗余标签 | 建议 |
| --- | --- | --- |
| `rag` | `retrieval-augmented-generation` | 保留 `rag`（GitHub 上更常用），全称可弃 |
| `ocr` | `optical-character-recognition` | 保留 `ocr`，全称可弃 |
| `visualization` | `data-visualization`、`visualization-models` | 三者语义有差别，确认后再合并 |
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

**统计**：基线 115 行（114 个唯一值）→ 110 个规范 slug（前两轮规范化后 108，第三轮补齐 6 个，第四轮移除 4 个）；一级分类 9 → 10，子组 5 → 7；第二轮改名 1 处、迁移 11 处、确认保留 3 处；第三轮新增 6 处；第四轮移除 4 处；第五轮改名 5 处、规范与文档修订 5 项，slug 总数不变。三级分类结构自第二轮起未再变动。

## 待确认项


- `tool`、`utility` 过于宽泛，检索价值低，建议替换为更具体的标签。
- E. 保留但建议后续合并的同义词
