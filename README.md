# GitHub Topics 分类清单

一份用于给仓库打标签的 GitHub Topics 清单，按「模型底座 → 能力层 → 数据与工程 → 行业场景」四段组织：01–05 为模型与能力层，06–07 为多模态能力，08–09 为数据与工程，10 为行业场景；11 为社区通用锚点词（对外检索），12 为仓库状态标签。

> 打标采用**双层结构**：01–10 归档词（对内分类）+ 11 社区通用锚点词（对外可发现性）+ 12 状态标签（生命周期）。维护规则见 [排序与维护规范](#排序与维护规范)，热度实测见 [低热度词映射表](#低热度词映射表)，完整变更见 [变更映射表](#变更映射表)。

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
- [11 社区通用锚点词](#11-社区通用锚点词-community-anchors)
- [12 仓库状态](#12-仓库状态-repository-status)
- [排序与维护规范](#排序与维护规范)
- [低热度词映射表](#低热度词映射表)
- [变更映射表](#变更映射表)
- [已知例外](#已知例外)

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
```

## 02 数据集 Datasets

数据集本体及其管理，含领域数据集。

```
dataset-management
medical-dataset
```

## 03 检索增强与知识工程 RAG & Knowledge

检索、语义匹配、知识图谱与结构化查询。

```
context-aware
embedding
fuzzy-matching
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
github-topics
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
circrna
drug-target-interaction
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
```

### 10.7 学习 Learning

```
awesome-list
language-learning
```

### 10.8 情报与舆情 Intelligence & OSINT

开源情报、新闻聚合与舆情情感分析。

```
news-monitoring
osint
sentiment-analysis
```

### 10.9 农业与食品安全 Agriculture & Food Safety

农产品检测、农药残留与食品安全判定。

```
food-safety
```

---

## 11 社区通用锚点词 Community Anchors

GitHub 全站被广泛使用的通用词，用于提升仓库在站内搜索与 Topics 主题页的可发现性。与 01–10 的归档词混用，**每个仓库建议 1–2 个，最多 2 个**；只描述技术栈、任务类型或学科，不承担内部分类职责。收录门槛：全站 ≥ 1,000 个公开仓库（实测口径见 [低热度词映射表](#低热度词映射表)）。

**本组只登记 01–10 中尚未收录的新词**（遵守第 3 条「每个 slug 只出现一次」）。已收录且达到门槛的 `agent`、`awesome-list`、`benchmark`、`bioinformatics`、`cli`、`genomics`、`llm`、`mcp`、`rag`、`time-series-forecasting` **自动兼任锚点词**，不在此重复登记；统计「是否含锚点词」时一并计入。

```
best-practices
data-cleaning
dataset
deep-learning
docker
excel
fastapi
framework
machine-learning
matrix-factorization
metadata
mlops
ontology
optuna
pandas
python
pytorch
rest-api
selenium
taxonomy
time-series
tutorial
web-app
web-scraping
```

## 12 仓库状态 Repository Status

与功能语义无关的生命周期标记，独立成组，不与 01–11 的词做同义判定。

```
working
```

- `working`：**作者本人正在开发 / 进行中的仓库**。这是保留状态位，任何批量整理都不得删除，删除需作者明确确认。
- 规范中的「3–6 个标签」指语义标签；状态位单独占 1 个，故带 `working` 的仓库语义标签取 3–5 个，线上总数 4–6 个。

---

## 排序与维护规范

1. **一级分类固定编号 01–12**，按认知链路排列：模型底座(01) → 数据集(02) → 检索能力(03) → Agent 能力(04) → 工具链(05) → 视觉与多模态生成(06) → 语音与跨模态转换(07) → 数据可视化与时空(08) → 开发与系统(09) → 行业应用(10) → 社区锚点(11) → 仓库状态(12)。不按字母序，也不按添加时间。
2. **组内一律按字母序（A→Z）**，数字开头的 slug（如 `3d-reconstruction`）排在组首。便于查找、code review 和脚本 diff。
3. **每个 slug 只出现一次**；跨领域标签按其最核心语义归组，领域专属 Agent 归 10；11 组只登记尚未收录的新词，已达门槛的既有词自动兼任锚点词，不重复登记。
4. **命名统一**：全小写 kebab-case，只含 `a-z` `0-9` `-`，不含空格、不含尾随空格；长度**建议 ≤ 35 字符**（GitHub Topics **官方上限 50 字符**），**每个仓库最多 20 个 topics**。单一概念一律用单数（`agent`、`build-agent`、`train-agent`、`tutorial`），复数仅用于表示集合类的标签（如 `research-models`、`visualization-models`）。
5. **语义边界**：`dataset` / `*-dataset` / `dataset-management` 表示数据集，归 02；`database` / `*-mcp` 表示数据管理软件，归 08 / 05；`research-*` 等科研 Agent 归 10.4，不放 04。`diffusion-model` 等模型架构归 01、生成任务归 06；`data-science`（学科）/ `data-scientist`（角色）/ `database`（软件）/ `data-visualization`（任务）为不同实体类型，08 组内按此区分；`computer-use` 表示 GUI/OS 级计算机操作 Agent，与 `terminal-agent`（命令行）、`browser-automation`（浏览器）并列但不等同；`working` 属于 12 仓库状态，是生命周期标记而非功能词，不与 10.6 的职场效率类标签混用。
6. **清单定位与新增流程**：清单是**标准词表**，不是线上标签的镜像。新增 slug 以「是否有通用检索价值」为准，**允许暂时零使用**，不必先有仓库在用。流程：先判断归属组 → 检查是否与已有 slug 重复或同义 → 插入组内字母序位置 → 在变更映射表登记（含基线 commit 与前后位置）。候选词若在 README 全文命中超过 30% 的仓库，视为文档与部署说明噪声（如 `documentation`），不纳入；技术栈、部署形态与属性词同理。**例外**：11 组社区通用锚点词专为对外检索设立，允许收录技术栈词，但每个仓库最多使用 2 个。
7. **格式**：组内用纯文本代码块，一行一个 slug，方便直接复制去 GitHub 打标签；不再使用 `<br>` 硬换行。
8. **打标执行**：每个仓库尽量 **3–6 个标签**，其中**至少 1 个来自 11 组社区通用锚点词**（带 `working` 状态位时语义标签取 3–5 个）；精简兼顾覆盖；**禁止同义标签并列**（如 `rag` 与全称、`text-to-speech` 与 `tts`）；新增标签优先用于修正内容错配，不要为凑数硬套泛标签；仓库应补全 `description` 与 README 的中文一句话简介。**禁止把固定标签组合成套套用**（如 `development-agent`+`research-agent`+`research-development-agent`、`data-extraction`+`data-governance`、`finance`+`quantitative-trading`+`trading-agent`）；每个标签都应能在 description 或 README 首段找到依据。**`working` 为作者保留的状态标签，任何批量整理均不得删除。**



## 低热度词映射表

2026-11-14 通过 GitHub Search API 的 `topic:slug` 实测全站公开仓库数。第七轮按作者确认的白名单执行：**仅 5 组执行全量替换，其余词明确保留不替换**。「本轮处置」中的仓库数为线上实际替换量。

| 归档词 | 全站仓库数 | 替换 / 保留结论 | 目标词全站仓库数 | 本轮处置 |
|---|---:|---|---:|---|
| `time-series-model` | 2 | **用 `time-series` 替换** | 16,264 | 已全量替换 14 个仓库；01 组下线，由 11 组承接 |
| `spatiotemporal-forecasting` | 40 | **用 `time-series-forecasting` 替换** | 3,366 | 已全量替换 5 个仓库；08 组下线，由组内既有词承接 |
| `study-material` | 86 | **用 `tutorial` 替换** | 24,182 | 已全量替换 80 个仓库；10.7 组下线，由 11 组承接 |
| `data-set` | 128 | **用 `dataset` 替换** | 21,338 | 已全量替换 21 个仓库；02 组下线，由 11 组承接 |
| `spider` | 2,952 | **用 `web-scraping` 替换** | 25,461 | 已全量替换 32 个仓库；05 组下线，由 11 组承接 |
| `research-development-agent` | 0 | **不用 `agent` 替换，保留** | — | 保留在 10.4 |
| `development-agent` | 1 | **不用 `agent` 替换，保留** | — | 保留在 04 |
| `model-management` | 195 | **不用 `mlops` 替换，保留** | — | 保留在 01 |
| `application-development` | 197 | **不用 `web-app` 替换，保留** | — | 保留在 09 |
| `research-agent` | 651 | **不用 `agent` 替换，保留** | — | 保留在 10.4 |
| `visualization` | 30,835 | **不用 `data-visualization` 替换，保留** | — | 保留在 08；与 `data-visualization` 并存，不视为同义 |
| `ai-framework` | 420 | 保留（本轮未指定替换） | — | 保留在 01 |
| `working` | 284 | 保留 | — | 12 组状态位，禁止批量删除 |

> 「不用替换」的词是作者明确确认的归档语义，不因全站检索量低而合并；后续任何整理都不得擅自替换。

长尾领域词虽然量小，但语义不可替代，已按第 6 条流程补入对应组：`circrna` / `drug-target-interaction` 归 10.3 生物、`food-safety` 归新增的 10.9、`fuzzy-matching` 归 03、`github-topics` 归 09；在具体仓库中与 11 组锚点词搭配使用。

---

## 变更映射表

| 轮次 | 日期 | 基线 commit | 变更 | 前后位置 |
|---|---|---|---|---|
| 第六轮 | 2026-11-14 | `c086353` | 新增 11 社区通用锚点词组（24 个新 slug + 10 个既有词兼任）与 12 仓库状态组；`working` 从 10.6 移出，正式定义为「作者本人正在开发中」，设为不可批量删除的状态位 | 10 之后新增 11 / 12；10.6 删除 `working` |
| 第六轮 | 2026-11-14 | `c086353` | 补登 5 个长尾领域词，使原创仓库全部线上标签在词表内均有归宿；新增 10.9 农业与食品安全组 | 03、09、10.3、10.9 |
| 第六轮 | 2026-11-14 | `c086353` | 规范 1 / 3 / 5 / 6 / 8 条修订：编号扩至 01–12、11 组不重复登记、11 组技术栈词例外、每仓至少 1 个锚点词、状态位配额与保护 | 排序与维护规范 |
| 第六轮 | 2026-11-14 | `c086353` | 新增低热度词映射表（13 组实测数据）；采用软下线而非删除，保持 608 个 fork 存量标签有效 | 规范之后新增章节 |
| 第六轮 | 2026-11-14 | `c086353` | 账号 10 个原创仓库按审计报告补全 description 与 topics、补齐 7 份 README.md、为 2 个第三方副本补来源声明；全部保留 `working` | 线上仓库 |
| 第七轮 | 2026-11-14 | `4985632` | 按作者白名单全量替换 5 组 slug：`time-series-model`→`time-series`、`spatiotemporal-forecasting`→`time-series-forecasting`、`study-material`→`tutorial`、`data-set`→`dataset`、`spider`→`web-scraping`；共 144 个仓库、152 个标签实例，全部回读验证通过 | 全账号扫描，144 个 fork 的线上 topics 命中替换 |
| 第七轮 | 2026-11-14 | `4985632` | 6 个词明确不用推荐词替换并保留：`research-development-agent`、`development-agent`、`model-management`、`application-development`、`research-agent`、`visualization`；`visualization` 与 `data-visualization` 并存 | 低热度词映射表 |
| 第七轮 | 2026-11-14 | `4985632` | 01 / 02 / 05 / 08 / 10.7 组移除 5 个已替换旧 slug，新写法由 11 组锚点词或 08 组既有词承接，避免重复登记；词表 155 → 150 slug | 各组代码块 |
| 第七轮 | 2026-11-14 | `4985632` | 规范第 4 / 5 条举例同步（`study-material`→`tutorial`、`data-set`→`dataset`）；低热度词映射表改写为处置结论表 | 排序与维护规范、映射表 |

---

## 已知例外

- **`agentic-design-patterns-cn`**：因 DMCA 版权限制（GitHub 于 2026-03-05 依据 Springer Nature 的投诉屏蔽该仓库，API 返回 `451 Repository access blocked`），账号无法修改该仓库的 Topics。第五轮单复数改名后，该仓库仍保留旧标签 `agents`、`study-materials`。
- **`n8n-workflows`**：因 DMCA 版权限制（GitHub 于 2025-08-26 屏蔽，API 同样返回 `451 Repository access blocked`），账号无法修改该仓库的 Topics 或补 README，是账号内唯一零标签仓库。
