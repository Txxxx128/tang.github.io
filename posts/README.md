<div align="center">

# WukongAgent v0.1

**PersonaLLM 驱动的微电网 Multi-Agent 调度系统**

[![Python](https://img.shields.io/badge/Python-3.13-blue.svg)](https://www.python.org/)
[![AutoGen](https://img.shields.io/badge/AutoGen-0.7.x-orange.svg)](https://microsoft.github.io/autogen/)
[![LangChain](https://img.shields.io/badge/LangChain-1.3.x-green.svg)](https://www.langchain.com/)
[![DeepSeek](https://img.shields.io/badge/LLM-DeepSeek-purple.svg)](https://platform.deepseek.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

基于多智能体（Multi-Agent）框架的微电网调度系统，实现设备角色化、市场报价协商与人格化决策。

</div>

---

## 📖 项目简介

WukongAgent 是一个探索性项目，用 **AutoGen** 多智能体框架搭建微电网调度系统，让每个设备（光伏、储能、负荷、调度）成为拥有独立角色、工具和人格的智能体，通过**价格信号**实现去中心化协调。

核心问题：**当储能有了"人格"，调度会发生什么变化？**

| 维度 | 传统集中式 | WukongAgent |
|------|-----------|-------------|
| 决策方式 | 单一优化算法 | 多 Agent 协商 |
| 协调机制 | 中央命令 | 价格信号 |
| 主体行为 | 完全理性 | 人格化（保守/激进/均衡） |

---

## ✨ 核心特性

- **四角色 Agent 架构**：PV / 储能 / 负荷 / 调度，各司其职
- **报价-协商-执行协议**：Agent 自主定价、讨价还价，收敛到均衡点
- **PersonaLLM 人格注入**：保守型 / 激进型 / 均衡型三种决策风格
- **经济性量化**：LP 精确计算不同人格的套利收益
- **真实 LLM 驱动**：DeepSeek function calling 自主调用工具

---

## 🚀 快速开始

### 环境要求

- Python 3.13+
- DeepSeek API Key

### 安装依赖

```bash
pip install pyautogen autogen-ext langchain langchain-openai
```

### 配置 API Key

```bash
# Windows（用户级环境变量，永久生效）
setx DEEPSEEK_API_KEY "sk-你的key"
```

### 运行

```bash
# HelloWorld 入门
python autogen_helloworld.py
python langchain_helloworld.py

# 4 角色协作调度
python autogen_4agents.py

# 报价-协商-执行协议
python autogen_negotiation.py

# PersonaLLM 人格注入
python autogen_persona.py

# 人格经济性对比（LP 量化）
python persona_economic_comparison.py
```

---

## 🗂️ 目录结构

```
W11/
├── autogen_helloworld.py           # AutoGen 双 Agent 对话入门
├── langchain_helloworld.py         # LangChain 消息流入门
├── autogen_4agents.py              # 4 角色 Agent 协作调度
├── autogen_negotiation.py          # 报价-协商-执行协议
├── autogen_persona.py              # PersonaLLM 人格注入
├── persona_economic_comparison.py  # 人格经济性 LP 对比
├── W11_协商结果.txt                 # 协商对话完整记录
├── W11_人格对比.txt / .png          # 人格决策对比 + 图表
├── W11_周报.docx / .pdf             # 周报文档
└── blog10_persona_multiaid.md/.html # 配套博客
```

---

## 📊 实验结果

### 报价-协商收敛

储能 Agent 报价 0.45 元/kWh → 调度 Agent 还价 0.30 元/kWh → 双方达成一致。

### 三种人格经济性对比

| 人格 | SOC 区间 | 日收益 | 可用容量 |
|------|---------|--------|---------|
| 保守型 | 20%~80% | 3.06 元 | 3.6 kWh |
| 均衡型 | 20%~90% | 3.57 元 | 4.2 kWh |
| 激进型 | 10%~95% | 4.32 元 | 5.1 kWh |

**结论**：收益与安全存在 trade-off，激进型收益最高但有 SOC 越界风险。

---

## 🛠️ 技术栈

- [AutoGen](https://microsoft.github.io/autogen/) — 多智能体框架
- [LangChain](https://www.langchain.com/) — LLM 应用框架
- [DeepSeek](https://platform.deepseek.com/) — 大语言模型
- [SciPy](https://scipy.org/) — 线性规划求解
- [Matplotlib](https://matplotlib.org/) — 可视化

---

## 📝 相关文档

- 配套博客：`blog10_persona_multiaid.md`（Markdown）/ `.html`（网页）
- 周报：`W11_周报.docx` / `W11_周报.pdf`

---

## 🗺️ 路线图

- [x] v0.1 — 多 Agent 框架 + 报价协商 + 人格注入
- [ ] v1.0 — 约束感知推理 + 安全层（W12）
- [ ] v1.1 — 自然语言控制接口（W13）

---

## 📄 License

MIT License

<div align="center">
<sub>W11 成果 · 电力电子 × AI 学习笔记</sub>
</div>
