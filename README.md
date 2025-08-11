<p align="center">
  <img src="assets/TauricResearch.png" style="width: 60%; height: auto;">
</p>

<div align="center" style="line-height: 1;">
  <a href="https://arxiv.org/abs/2412.20138" target="_blank"><img alt="arXiv" src="https://img.shields.io/badge/arXiv-2412.20138-B31B1B?logo=arxiv"/></a>
  <a href="https://discord.com/invite/hk9PGKShPK" target="_blank"><img alt="Discord" src="https://img.shields.io/badge/Discord-TradingResearch-7289da?logo=discord&logoColor=white&color=7289da"/></a>
  <a href="./assets/wechat.png" target="_blank"><img alt="WeChat" src="https://img.shields.io/badge/WeChat-TauricResearch-brightgreen?logo=wechat&logoColor=white"/></a>
  <a href="https://x.com/TauricResearch" target="_blank"><img alt="X Follow" src="https://img.shields.io/badge/X-TauricResearch-white?logo=x&logoColor=white"/></a>
  <br>
  <a href="https://github.com/TauricResearch/" target="_blank"><img alt="Community" src="https://img.shields.io/badge/Join_GitHub_Community-TauricResearch-14C290?logo=discourse"/></a>
</div>

<div align="center">
  <!-- 请保留以下链接，readme-i18n 会自动生成翻译版本 -->
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=de">Deutsch</a> |
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=es">Español</a> |
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=fr">français</a> |
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ja">日本語</a> |
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ko">한국어</a> |
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=pt">Português</a> |
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ru">Русский</a> |
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=en">English</a>
</div>

---

# TradingAgents：多智能体 LLM 金融交易框架

> 🎉 **TradingAgents** 正式发布！非常感谢社区对我们的关注与支持。
>
> 我们决定完全开源这一框架，期待与您一起打造有影响力的项目。

<div align="center">
<a href="https://www.star-history.com/#TauricResearch/TradingAgents&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=TauricResearch/TradingAgents&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=TauricResearch/TradingAgents&type=Date" />
   <img alt="TradingAgents Star History" src="https://api.star-history.com/svg?repos=TauricResearch/TradingAgents&type=Date" style="width: 80%; height: auto;" />
 </picture>
</a>
</div>

<div align="center">

🚀 [TradingAgents](#tradingagents框架) | ⚡ [安装与命令行](#安装与命令行) | 🎬 [演示](https://www.youtube.com/watch?v=90gr5lwjIho) | 📦 [Python 包使用](#tradingagents-包) | 🤝 [参与贡献](#参与贡献) | 📄 [引用](#引用)

</div>

## TradingAgents 框架

TradingAgents 是一个模拟真实交易公司的多智能体交易框架。我们部署了多个专用的 LLM 智能体：包括基本面分析师、情绪分析师、新闻分析师、技术分析师、交易员以及风险管理团队等。它们协作评估市场状况并输出交易决策，同时智能体之间还会进行讨论以寻找最优策略。

<p align="center">
  <img src="assets/schema.png" style="width: 100%; height: auto;">
</p>

> TradingAgents 主要用于研究目的。其交易表现可能受所选底座模型、温度、回测期间、数据质量等因素影响，并具有非确定性特征。 [本项目不构成任何投资或交易建议。](https://tauric.ai/disclaimer/)

该框架将复杂的交易任务拆分为多个角色，使系统能够以更稳健、可扩展的方式进行市场分析和决策。

### 分析师团队
- **基本面分析师**：评估公司财务和经营指标，识别内在价值与潜在风险。
- **情绪分析师**：通过社交媒体与舆情数据分析市场情绪，判断短期走势。
- **新闻分析师**：监控全球新闻及宏观经济指标，评估事件对市场的影响。
- **技术分析师**：利用 MACD、RSI 等技术指标识别交易模式并预测价格走势。

<p align="center">
  <img src="assets/analyst.png" width="100%" style="display: inline-block; margin: 0 2%;">
</p>

### 研究团队
由看多与看空的研究员组成，对分析师团队的观点进行审视。通过结构化辩论权衡收益与风险。

<p align="center">
  <img src="assets/researcher.png" width="70%" style="display: inline-block; margin: 0 2%;">
</p>

### 交易员
整合分析师与研究员的报告，做出最终交易决策，并决定交易时间与规模。

<p align="center">
  <img src="assets/trader.png" width="70%" style="display: inline-block; margin: 0 2%;">
</p>

### 风险管理与投资组合经理
- 持续评估市场波动性、流动性等风险因素，调整交易策略并向投资组合经理提交评估报告。
- 投资组合经理负责批准或拒绝交易提案，若通过则会将订单发送到模拟交易所执行。

<p align="center">
  <img src="assets/risk.png" width="70%" style="display: inline-block; margin: 0 2%;">
</p>

## 安装与命令行

### 安装

克隆仓库：
```bash
git clone https://github.com/TauricResearch/TradingAgents.git
```

创建并激活 Conda 环境：
```bash
conda create -n tradingagents python=3.13
conda activate tradingagents
```

安装依赖：
```bash
pip install -r requirements.txt
```

### 必需的 API

为了获取金融数据，需要 FinnHub API（免费额度即可）：
```bash
export FINNHUB_API_KEY=$YOUR_FINNHUB_API_KEY
```

所有智能体默认使用 OpenAI API：
```bash
export OPENAI_API_KEY=$YOUR_OPENAI_API_KEY
```

若需通过 SiliconFlow 合成语音回复，请设置 API Key 并在配置中指定模型：
```bash
export SILICONFLOW_API_KEY=$YOUR_SILICONFLOW_API_KEY
```

可在 `default_config.py` 中通过 `role_llms` 为每个角色指定语言模型，也可在 `role_speech_models` 中为角色指定语音模型。

### 命令行使用

运行 CLI：
```bash
python -m cli.main
```
按照提示选择股票代码、日期、模型与研究深度等参数。程序运行后可实时查看各智能体的输出与进度。

<p align="center">
  <img src="assets/cli/cli_init.png" width="100%" style="display: inline-block; margin: 0 2%;">
</p>

<p align="center">
  <img src="assets/cli/cli_news.png" width="100%" style="display: inline-block; margin: 0 2%;">
</p>

<p align="center">
  <img src="assets/cli/cli_transaction.png" width="100%" style="display: inline-block; margin: 0 2%;">
</p>

## TradingAgents 包

### 实现细节

TradingAgents 基于 LangGraph 构建，强调灵活与模块化。实验中我们使用 `o1-preview` 与 `gpt-4o` 作为深度与快速思考模型。若仅测试，可选用 `o4-mini` 与 `gpt-4.1-mini` 以降低成本，因为框架会调用大量 API。

### Python 使用示例

在代码中可直接导入 `tradingagents` 模块并初始化 `TradingAgentsGraph()`：

```python
from tradingagents.graph.trading_graph import TradingAgentsGraph
from tradingagents.default_config import DEFAULT_CONFIG

ta = TradingAgentsGraph(debug=True, config=DEFAULT_CONFIG.copy())

# 前向传播
_, decision = ta.propagate("NVDA", "2024-05-10")
print(decision)
```

你也可以通过修改默认配置选择不同模型、调整辩论轮数等：

```python
from tradingagents.graph.trading_graph import TradingAgentsGraph
from tradingagents.default_config import DEFAULT_CONFIG

# 自定义配置
config = DEFAULT_CONFIG.copy()
config["deep_think_llm"] = "gpt-4.1-nano"   # 更换模型
config["quick_think_llm"] = "gpt-4.1-nano"  # 更换模型
config["max_debate_rounds"] = 1            # 辩论轮数
config["online_tools"] = True              # 使用在线工具

ta = TradingAgentsGraph(debug=True, config=config)

_, decision = ta.propagate("NVDA", "2024-05-10")
print(decision)
```

> 若将 `online_tools` 设为 True，可获取实时数据。离线工具依赖我们整理的 **Tauric TradingDB** 缓存数据，目前仍在完善中，未来会随后续项目一同发布。

更多配置项请参考 `tradingagents/default_config.py`。

## 参与贡献

欢迎社区贡献！无论是修复 bug、改进文档还是提出新功能，您的帮助都会让项目更好。如果你对该方向感兴趣，欢迎加入我们的开源金融 AI 社区 [Tauric Research](https://tauric.ai/)。

## 引用

如果 TradingAgents 对您的研究或项目有所帮助，请引用我们的论文：

```
@misc{xiao2025tradingagentsmultiagentsllmfinancial,
      title={TradingAgents: Multi-Agents LLM Financial Trading Framework},
      author={Yijia Xiao and Edward Sun and Di Luo and Wei Wang},
      year={2025},
      eprint={2412.20138},
      archivePrefix={arXiv},
      primaryClass={q-fin.TR},
      url={https://arxiv.org/abs/2412.20138},
}
```

