# Claim Graph Paper Writer

先把论文拆成可检查的命题与逻辑关系，经过作者修改和确认，再重组为学术正文。

**AI 初稿 → 命题节点 → 证据与逻辑检查 → 人工修改和连接 → 重组论文**

An agent skill for making scientific reasoning visible and editable before polishing academic prose.

## 核心功能

- **拆分命题**：每个节点只表达一条可独立判断的命题。
- **保留证据**：引用、图表、公式和数据始终跟随对应命题。
- **区分证据与推断**：使用 Confirmed、Reasoned inference、Unverified 三类状态。
- **检查逻辑关系**：识别缺失前提、证据错配、重复判断、矛盾和不充分的因果推断。
- **人工控制含义**：作者修改节点与连接，Agent 检查受到影响的后续结论。
- **按确认后的结构写作**：保留论断强度、适用条件和引用，检查重组前后含义是否一致。

## 文件

[SKILL.md](SKILL.md) 是完整的技能指令，包含五种模式：Extract、Build Graph、Logic Audit、Human Repair 和 Reconstruct。

## 安装

将本仓库中的 `SKILL.md` 放入支持 Agent Skills 的工具所使用的技能目录：

```text
<skills-directory>/
└── claim-graph-paper-writer/
    └── SKILL.md
```

技能目录位置取决于所用工具。也可以直接把 `SKILL.md` 上传给 AI，并要求按文件中的流程工作。

## 使用示例

### 1. 拆分并检查

> 使用 Claim Graph Paper Writer 分析下面这段 Discussion。先拆成原子命题，保留引用，标注证据状态，建立逻辑关系并检查缺失前提。暂时不要改写正文。

### 2. 修改节点

> 将 N3 的结论限定在本研究测试条件内，删除 N5，检查受影响的下游结论并更新逻辑图。

### 3. 重组正文

> 我已确认当前节点和连接。请按确认后的逻辑结构重组为学术英文，保留引用、适用条件和论断强度，最后检查是否引入了新含义。

## 适用场景

论文或博士论文的段落分析、Introduction 研究缺口梳理、Discussion 逻辑重构、Conclusion 证据追溯，以及 AI 生成初稿的论证检查。

可在纯 Markdown 中使用，也可手动将节点与连接整理到图形画布中；无需依赖特定软件。

## Evidence discipline

The skill separates supplied evidence from interpretation. It does not invent data, citations, mechanisms or validation steps. Citation support remains unverified when the relevant source has not been checked.

The workflow provides a structured review of supplied material; the author retains responsibility for scientific judgements and approval of the argument.

## Workflow

1. Extract atomic claims.
2. Attach evidence and classify evidence status.
3. Build explicit logical connections.
4. Audit unsupported jumps and missing conditions.
5. Let the author repair and approve the graph.
6. Reconstruct prose and check that meaning is preserved.
