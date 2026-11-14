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
6. **清单定位与新增流程**：清单是**标准词表**，不是线上标签的镜像。新增 slug 以「是否有通用检索价值」为准，**允许暂时零使用**，不必先有仓库在用。流程：先判断归属组 → 检查是否与已有 slug 重复或同义 → 插入组内字母序位置 → 在变更映射表登记（含基线 commit 与前后位置）。候选词若在 README 全文命中超过 30% 的仓库，视为文档与部署说明噪声（如 `docker`、`documentation`），不纳入；技术栈、部署形态与属性词同理。
7. **格式**：组内用纯文本代码块，一行一个 slug，方便直接复制去 GitHub 打标签；不再使用 `<br>` 硬换行。
8. **打标执行**：每个仓库尽量 **3–6 个标签**，精简兼顾覆盖；**禁止同义标签并列**（如 `rag` 与全称、`text-to-speech` 与 `tts`）；新增标签优先用于修正内容错配，不要为凑数硬套泛标签；仓库应补全 `description` 与 README 的中文一句话简介。**禁止把固定标签组合成套套用**（如 `development-agent`+`research-agent`+`research-development-agent`、`data-extraction`+`data-governance`、`finance`+`quantitative-trading`+`trading-agent`）；每个标签都应能在 description 或 README 首段找到依据。



## 已知例外

- **`agentic-design-patterns-cn`**：因 DMCA 版权限制（GitHub 于 2026-03-05 依据 Springer Nature 的投诉屏蔽该仓库，API 返回 `451 Repository access blocked`），账号无法修改该仓库的 Topics。第五轮单复数改名后，该仓库仍保留旧标签 `agents`、`study-materials`。
- **`n8n-workflows`**：因 DMCA 版权限制（GitHub 于 2025-08-26 屏蔽，API 同样返回 `451 Repository access blocked`），账号无法修改该仓库的 Topics 或补 README，是账号内唯一零标签仓库。
