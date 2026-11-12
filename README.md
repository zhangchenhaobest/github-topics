# GitHub Topics 分类清单

一份用于给仓库打标签的 GitHub Topics 清单，按「技术底座 → 能力层 → 应用场景」组织。

> 维护规则见 [排序与维护规范](#排序与维护规范)，历史变更见 [变更映射表](#变更映射表)。

## 目录

- [01 模型与训练](#01-模型与训练-models--training)
- [02 检索增强与知识工程](#02-检索增强与知识工程-rag--knowledge)
- [03 Agent 与编排](#03-agent-与编排-agents--orchestration)
- [04 MCP 与工具链](#04-mcp-与工具链-mcp--tooling)
- [05 视觉与多模态生成](#05-视觉与多模态生成-vision--multimodal)
- [06 语音与跨模态转换](#06-语音与跨模态转换-speech--conversion)
- [07 数据、可视化与时空](#07-数据可视化与时空-data--visualization--spatiotemporal)
- [08 开发与系统](#08-开发与系统-development--systems)
- [09 垂直领域与场景](#09-垂直领域与场景-domains--use-cases)
- [排序与维护规范](#排序与维护规范)
- [变更映射表](#变更映射表)
- [待确认项](#待确认项)

---

## 01 模型与训练 Models & Training

基础模型、训练方法、评测与模型/数据集管理。

```
ai-framework
data-set
dataset-management
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

## 02 检索增强与知识工程 RAG & Knowledge

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
```

## 03 Agent 与编排 Agents & Orchestration

通用智能体框架、编排、记忆与提示工程。领域专属 Agent 归入 [09](#09-垂直领域与场景-domains--use-cases)。

```
agents
ai-operating-system
build-agents
chatbot
chatbot-framework
claude-code
development-agent
memory-management
memory-plugin
multi-agent
prompt-engineering
prompt-optimizer
research-agent
research-development-agent
skill
terminal-agent
train-agents
web-agent
windows-agent
workflow
```

## 04 MCP 与工具链 MCP & Tooling

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

## 05 视觉与多模态生成 Vision & Multimodal

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

## 06 语音与跨模态转换 Speech & Conversion

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

## 07 数据、可视化与时空 Data, Visualization & Spatiotemporal

数据治理、可视化、数据库与时空/图数据分析。

```
data-extraction
data-governance
data-scientist
data-visualization
database
gcn
gis
objectstorage
spatiotemporal-data-analysis
spatiotemporal-forecasting
visualization
visualization-models
```

## 08 开发与系统 Development & Systems

应用开发、平台、网络与基础设施。

```
application-development
github-app-store
network
office
security
virtualization
web-development
```

## 09 垂直领域与场景 Domains & Use Cases

按行业/场景归类的标签，含该领域专属 Agent。

### 09.1 金融 Finance

```
finance
quantitative-trading
trading-agent
```

### 09.2 医疗健康 Healthcare

```
medical
medical-database
medical-evaluation-framework
medical-llm
medical-research-agent
```

### 09.3 生物与科研 Bio & Research

```
biology
language-learning
lims
paper-writing
paper-writing-agent
study-materials
```

### 09.4 自动驾驶与机器人 Autonomy & Robotics

```
autopilot
robot
```

### 09.5 职场与效率 Work & Productivity

```
bid
find-job
product-manager
working
```

---

## 排序与维护规范

1. **一级分类固定编号 01–09**，按认知链路排列：模型底座 → 检索能力 → Agent 能力 → 工具链 → 多模态 → 数据 → 工程 → 行业应用。不按字母序，也不按添加时间。
2. **组内一律按字母序（A→Z）**，数字开头的 slug（如 `3d-reconstruction`）排在组首。便于查找、code review 和脚本 diff。
3. **每个 slug 只出现一次**；跨领域标签按其最核心语义归组，领域专属 Agent 归 09。
4. **命名统一**：全小写 kebab-case，只含 `a-z` `0-9` `-`，不含空格、不含尾随空格，长度 ≤ 35 字符（GitHub Topics 硬性要求）；单复数统一用单数。
5. **新增流程**：先判断归属组 → 检查是否与已有 slug 重复或同义 → 插入组内字母序位置 → 在变更映射表登记。
6. **格式**：组内用纯文本代码块，一行一个 slug，方便直接复制去 GitHub 打标签；不再使用 `<br>` 硬换行。

## 变更映射表

本次整理对原清单的处理（原 → 新）：

| 类型 | 原值 | 新值 | 说明 |
| --- | --- | --- | --- |
| 去重 | `working` ×2 | `working` ×1 | 原第 67、78 行重复 |
| 单复数 | `llms` | `llm` | 统一单数 |
| 单复数 | `models` | `model` | 统一单数 |
| 单复数 | `tools` | `tool` | 统一单数 |
| 单复数 | `medical-llms` | `medical-llm` | 统一单数 |
| 单复数 | `medical-databases` | `medical-database` | 统一单数 |
| 单复数 | `time-series-models` | `time-series-model` | 统一单数 |
| 非法 slug | `spatiotemporal forecasting` | `spatiotemporal-forecasting` | 原值含空格，**不是合法 GitHub topic** |
| 格式修正 | `translation ` | `translation` | 去除尾随空格 |
| 格式修正 | 每行末尾 `<br>` | Markdown 代码块 | 原文件用 HTML 换行，不利于脚本读取 |

**保留但建议后续合并的同义词**（本次未删，避免已有仓库标签失效）：

| 主标签 | 同义/冗余标签 | 建议 |
| --- | --- | --- |
| `rag` | `retrieval-augmented-generation` | 保留 `rag`（GitHub 上更常用），全称可弃 |
| `ocr` | `optical-character-recognition` | 保留 `ocr`，全称可弃 |
| `visualization` | `data-visualization`、`visualization-models` | 三者语义有差别，确认后再合并 |
| `database` | `data-set`、`dataset-management` | 分属不同层级，暂保留 |

**统计**：原 115 行（114 个唯一值）→ 现 108 个规范 slug，合并 6 组单复数、去掉 1 个重复、修正 2 个格式问题。

## 待确认项

- `working` 语义含糊（工作求职？运行中？），建议改成 `job` / `work-automation`，或直接删除。
- `tool`、`utility` 过于宽泛，检索价值低，建议替换为更具体的标签。
- `claude-code`、`n8n-mcp`、`github-app-store` 是产品/项目名而非通用主题，确认是否长期保留。
- `microscope`、`radar`、`lims`、`bid`、`biology` 与 AI 主线跨度较大，若继续扩充可独立成「10 其他领域」。
- 若希望全清单严格按字母序检索，可在文末追加一份「按字母序索引」章节，与主分类并存。
