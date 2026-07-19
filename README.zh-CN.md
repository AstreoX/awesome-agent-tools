<div align="center">

<!-- 标题与徽章 -->
# Awesome Agent Tools

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/AstreoX/awesome-agent-tools/graphs/commit-activity)

**精选的 AI 智能体框架、平台、工具和资源列表，涵盖构建、编排和部署 AI 智能体的方方面面。**

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [Español](README.es.md)

<sub>AI 智能体是由大语言模型驱动的自主系统，能够进行推理、规划、使用工具并采取行动来完成复杂任务。<br/>本列表持续追踪快速发展的智能体工具生态。</sub>

**[什么是 AI 智能体？](#什么是-ai-智能体) | [如何贡献](CONTRIBUTING.md)**

</div>

---

## 目录

- [智能体框架](#智能体框架)
- [多智能体编排](#多智能体编排)
- [代码智能体](#代码智能体)
- [工具使用与函数调用](#工具使用与函数调用)
- [模型上下文协议 (MCP)](#模型上下文协议-mcp)
- [智能体记忆](#智能体记忆)
- [智能体 RAG](#智能体-rag)
- [智能体监控与可观测性](#智能体监控与可观测性)
- [智能体评估与测试](#智能体评估与测试)
- [智能体安全与防护](#智能体安全与防护)
- [智能体原生开发](#智能体原生开发)
- [语音与多模态智能体](#语音与多模态智能体)
- [智能体部署与基础设施](#智能体部署与基础设施)
- [浏览器与网页智能体](#浏览器与网页智能体)
- [研究型智能体](#研究型智能体)
- [工作流与任务自动化](#工作流与任务自动化)
- [智能体通信协议](#智能体通信协议)
- [学习资源](#学习资源)
- [研究论文](#研究论文)
- [社区](#社区)

---

## 什么是 AI 智能体？

AI 智能体是一种以大语言模型作为核心推理引擎的系统，它能够：

- **推理**：分析问题并制定解决方案
- **行动**：调用工具、API 或执行代码
- **观察**：获取行动的结果
- **迭代**：反复执行直至任务完成

这使得智能体区别于简单的聊天机器人或单轮大语言模型应用。

---

## 智能体框架

*用于构建 AI 智能体的通用框架。*

- [LangChain](https://github.com/langchain-ai/langchain) - 基于大语言模型开发应用的框架，支持可组合的链式调用和智能体。
- [LangGraph](https://github.com/langchain-ai/langgraph) - 基于 LangChain 构建的库，用于开发有状态的多参与者大语言模型应用。
- [CrewAI](https://github.com/crewAIInc/crewAI) - 用于编排角色扮演型自主 AI 智能体的框架。
- [AutoGen](https://github.com/microsoft/autogen) - 微软的多智能体对话系统构建框架。
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) - 微软的 SDK，通过插件架构将大语言模型集成到应用中。
- [Haystack](https://github.com/deepset-ai/haystack) - 端到端 NLP 框架，具有智能体能力和基于管道的架构。
- [LlamaIndex](https://github.com/run-llama/llama_index) - 大语言模型应用的数据框架，提供智能体抽象。
- [Smolagents](https://github.com/huggingface/smolagents) - Hugging Face 的轻量级库，以代码优先的方式构建强大的智能体。
- [PydanticAI](https://github.com/pydantic/pydantic-ai) - 由 Pydantic 团队开发的智能体框架，使用 Pydantic 实现类型安全的工具定义。
- [Agno](https://github.com/agno-agi/agno) - 轻量级框架，用于构建具有记忆、知识和工具的多模态智能体。
- [Atomic Agents](https://github.com/BrainBlend-AI/atomic-agents) - 模块化框架，通过原子化的可组合组件构建智能体系统。
- [Letta](https://github.com/letta-ai/letta) - 构建具有长期记忆的有状态智能体的框架（前身为 MemGPT）。
- [Mirascope](https://github.com/Mirascope/mirascope) - Pythonic 风格的工具包，以简洁优雅的 API 构建大语言模型驱动的智能体。
- [ControlFlow](https://github.com/PrefectHQ/ControlFlow) - 由 Prefect 开发的 Python 智能体工作流构建框架。
- [Claude Agent SDK](https://github.com/anthropics/claude-code/tree/main/packages/claude-agent-sdk) - Anthropic 官方 SDK，用于构建基于 Claude 的自定义智能体。
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) - OpenAI 的 SDK，支持构建具有交接和防护机制的智能体应用。
- [Google ADK](https://github.com/google/adk-python) - Google 的智能体开发工具包，用于构建 AI 智能体。
- [Bee Agent Framework](https://github.com/i-am-bee/bee-agent-framework) - IBM 的开源框架，用于构建、部署和运行智能体。
- [Julep](https://github.com/julep-ai/julep) - 构建具有长期记忆和复杂工作流的持久化 AI 智能体平台。
- [Eliza](https://github.com/elizaOS/eliza) - 多智能体仿真框架，用于创建自主 AI 角色。

## 多智能体编排

*管理和协调多个智能体协同工作的工具。*

- [AutoGen](https://github.com/microsoft/autogen) - 对话式多智能体框架，支持多种协作模式。
- [CrewAI](https://github.com/crewAIInc/crewAI) - 基于角色的多智能体编排，支持顺序和层级化流程。
- [LangGraph](https://github.com/langchain-ai/langgraph) - 有状态的多智能体图框架，支持循环和可控性。
- [OpenAI Swarm](https://github.com/openai/swarm) - 探索轻量级多智能体编排的教学框架。
- [MetaGPT](https://github.com/geekan/MetaGPT) - 为 GPT 分配不同角色以组成协作软件实体的多智能体框架。
- [ChatDev](https://github.com/OpenBMB/ChatDev) - 由多个不同角色的智能体驱动的虚拟软件公司。
- [Camel](https://github.com/camel-ai/camel) - 用于探索大语言模型社会"心智"的交流型智能体。
- [Agency Swarm](https://github.com/VRSEN/agency-swarm) - 开源框架，用于创建 AI 智能体协作群。
- [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one) - 微软的通用型多智能体系统，用于解决复杂任务。
- [Langtrace](https://github.com/Scale3-Labs/langtrace) - 面向多智能体大语言模型应用的开源可观测性工具。

## 代码智能体

*专注于软件工程任务的智能体。*

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) - Anthropic 的智能编码工具，直接在终端中运行。
- [Cursor](https://cursor.com/) - AI 优先的代码编辑器，内置智能体功能。
- [GitHub Copilot](https://github.com/features/copilot) - AI 结对编程工具，具有多文件编辑和终端命令的智能体模式。
- [Cline](https://github.com/cline/cline) - VS Code 中的自主编码智能体，可创建/编辑文件、运行命令和使用浏览器。
- [Aider](https://github.com/Aider-AI/aider) - 终端中的 AI 结对编程工具，集成 Git。
- [Windsurf](https://codeium.com/windsurf) - Codeium 的智能体 IDE，提供 Cascade 流程实现多步编码。
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) - 自主软件开发智能体平台（前身为 OpenDevin）。
- [SWE-agent](https://github.com/princeton-nlp/SWE-agent) - 以语言模型为大脑自主修复 GitHub Issue 的智能体。
- [Devika](https://github.com/stitionai/Devika) - 智能体式 AI 软件工程师，能够理解需求、规划和编写代码。
- [GPT Engineer](https://github.com/gpt-engineer-org/gpt-engineer) - 根据单个提示词生成完整代码库的智能体。
- [Codex CLI](https://github.com/openai/codex) - OpenAI 的轻量级编码智能体，在终端中运行。
- [Roo Code](https://github.com/RooVetGit/Roo-Code) - VS Code 的 AI 编码智能体扩展，支持多模型。
- [Augment Code](https://www.augmentcode.com/) - 深度理解代码库的 AI 编码智能体。
- [Tabnine](https://www.tabnine.com/) - 具有智能体式代码补全功能的 AI 编码助手。
- [Trae](https://www.trae.ai/) - 字节跳动的自适应 AI IDE，具有 Builder 模式实现智能体编码。
- [Kilo Code](https://github.com/kilocode-ai/kilocode) - 开源 VS Code 扩展，将 AI 编码智能体集成到编辑器中。

## 工具使用与函数调用

*使大语言模型能够使用工具和调用函数的库和框架。*

- [LangChain Tools](https://python.langchain.com/docs/modules/agents/tools/) - 丰富的预构建工具集合和工具创建实用程序。
- [Composio](https://github.com/ComposioHQ/composio) - 集成平台，为 AI 智能体提供 250 多种工具，并具有托管认证。
- [Toolhouse](https://toolhouse.ai/) - 为大语言模型配备行动能力和知识的云基础设施。
- [ACI.dev](https://github.com/aipoool/aci) - 开源平台，为 AI 智能体提供统一的工具使用基础设施。
- [Arcade AI](https://github.com/ArcadeAI/arcade-ai) - 工具使用平台，让任何大语言模型都能轻松添加工具。
- [Instructor](https://github.com/jxnl/instructor) - 结构化输出库，使函数调用更加可靠。
- [Outlines](https://github.com/dottxt-ai/outlines) - 结构化文本生成，实现可靠的工具使用。
- [NPI](https://github.com/npi-ai/npi) - 工具使用 API 平台，使智能体能够操作各种软件工具。

## 模型上下文协议 (MCP)

*实现 Anthropic 模型上下文协议以标准化工具集成的工具和服务器。*

- [MCP Specification](https://modelcontextprotocol.io/) - 模型上下文协议官方规范。
- [MCP Servers](https://github.com/modelcontextprotocol/servers) - MCP 服务器的官方参考实现。
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - 用于构建 MCP 客户端和服务器的官方 TypeScript SDK。
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) - 用于构建 MCP 客户端和服务器的官方 Python SDK。
- [MCP Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk) - 用于在 JVM 上构建 MCP 服务器和客户端的官方 Kotlin SDK。
- [FastMCP](https://github.com/jlowin/fastmcp) - 快速、Pythonic 风格的 MCP 服务器和客户端构建方式。
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - MCP 服务器实现的精选列表。
- [mcp-use](https://github.com/pietrozullo/mcp-use) - 开源库，将任何大语言模型连接到任何 MCP 服务器。
- [Smithery](https://smithery.ai/) - 发现和部署 MCP 服务器的注册中心和市场。
- [Glama](https://glama.ai/mcp/servers) - MCP 服务器发现和目录平台。
- [mcpx](https://github.com/arcadeai-labs/mcpx) - 用于检查和调用 MCP 服务器的命令行客户端。

## 智能体记忆

*为智能体提供短期和长期记忆的系统。*

- [Mem0](https://github.com/mem0ai/mem0) - 面向大语言模型应用的自我改进记忆层。
- [Letta](https://github.com/letta-ai/letta) - 具有长期记忆管理的有状态智能体（前身为 MemGPT）。
- [Zep](https://github.com/getzep/zep) - AI 助手的长期记忆，支持自动摘要。
- [Motorhead](https://github.com/getmetal/motorhead) - 大语言模型的记忆和上下文管理服务器。
- [LangMem](https://github.com/langchain-ai/langmem) - LangChain 面向大语言模型应用的长期记忆 SDK。
- [Cognee](https://github.com/topoteretes/cognee) - 使用知识图谱和向量存储的 AI 智能体记忆管理。

## 智能体 RAG

*增强智能体知识的检索增强生成工具。*

- [LlamaIndex](https://github.com/run-llama/llama_index) - 将自定义数据连接到大语言模型的数据框架，具有高级检索功能。
- [ChromaDB](https://github.com/chroma-core/chroma) - 面向 AI 应用的开源嵌入向量数据库。
- [Weaviate](https://github.com/weaviate/weaviate) - 面向可扩展 AI 应用的开源向量数据库。
- [Qdrant](https://github.com/qdrant/qdrant) - 高性能向量相似度搜索引擎。
- [Pinecone](https://www.pinecone.io/) - 面向高性能 AI 应用的托管向量数据库。
- [Milvus](https://github.com/milvus-io/milvus) - 为可扩展相似度搜索而构建的开源向量数据库。
- [Unstructured](https://github.com/Unstructured-IO/unstructured) - 用于 RAG 管道中文档预处理和导入的库。
- [R2R](https://github.com/SciPhi-AI/R2R) - 具有智能体功能的生产级 RAG 引擎。
- [RAGFlow](https://github.com/infiniflow/ragflow) - 基于深度文档理解的开源 RAG 引擎。
- [LightRAG](https://github.com/HKUDS/LightRAG) - 使用图结构进行索引的简洁快速 RAG 引擎。

## 智能体监控与可观测性

*用于追踪、调试和理解智能体行为的工具。*

- [LangSmith](https://smith.langchain.com/) - 大语言模型应用的调试、测试、评估和监控平台。
- [LangFuse](https://github.com/langfuse/langfuse) - 大语言模型应用的开源可观测性和分析平台。
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - 大语言模型应用的开源可观测性工具，支持追踪和评估。
- [Helicone](https://github.com/Helicone/helicone) - 开源大语言模型可观测性平台，提供日志和分析功能。
- [Braintrust](https://github.com/braintrustdata/braintrust-sdk) - 企业级技术栈，用于构建、发布和监控 AI 产品。
- [Weave](https://github.com/wandb/weave) - Weights & Biases 的大语言模型应用追踪和评估工具包。
- [AgentOps](https://github.com/AgentOps-AI/agentops) - AI 智能体监控、测试和回放分析的 Python SDK。
- [OpenLLMetry](https://github.com/traceloop/openllmetry) - 基于 OpenTelemetry 的大语言模型开源可观测性。
- [Pydantic Logfire](https://github.com/pydantic/logfire) - 对 Pydantic 和大语言模型应用提供一流支持的可观测性平台。

## 智能体评估与测试

*评估和基准测试智能体性能的框架。*

- [SWE-bench](https://github.com/princeton-nlp/SWE-bench) - 在真实软件工程问题上评估语言模型的基准。
- [GAIA](https://huggingface.co/gaia-benchmark) - 在真实任务上评估通用 AI 助手的基准。
- [AgentBench](https://github.com/THUDM/AgentBench) - 在多种环境中评估大语言模型作为智能体的基准。
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) - 英国 AISI 开发的大语言模型评估框架。
- [RAGAS](https://github.com/explodinggradients/ragas) - RAG 管道评估框架。
- [DeepEval](https://github.com/confident-ai/deepeval) - 包含 14 种以上指标的大语言模型评估框架。
- [Promptfoo](https://github.com/promptfoo/promptfoo) - 大语言模型输出测试和评估工具。
- [TauBench](https://github.com/sierra-research/tau-bench) - 在真实场景中评估工具-智能体-用户交互的基准。
- [Agent-as-a-Judge](https://github.com/metauto-ai/agent-as-a-judge) - 使用智能体来评估智能体输出。

## 智能体安全与防护

*使智能体安全、可靠且可控的工具。*

- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - 为大语言模型输出添加结构、类型和质量保障的框架。
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - NVIDIA 的工具包，为基于大语言模型的应用添加可编程防护栏。
- [LLM Guard](https://github.com/protectai/llm-guard) - 大语言模型交互安全工具包，支持输入/输出扫描。
- [Rebuff](https://github.com/protectai/rebuff) - 自适应增强的提示注入检测器。
- [Lakera Guard](https://www.lakera.ai/) - 实时 AI 安全防护，防止提示注入和数据泄露。
- [Invariant Labs](https://github.com/invariantlabs-ai/invariant) - AI 智能体的安全测试和执行。
- [Prompt Armor](https://promptarmor.com/) - 提示注入攻击防护。

## 智能体原生开发

*从零开始为智能体驱动的开发而构建的工具和平台。*

- [E2B](https://github.com/e2b-dev/e2b) - 面向 AI 智能体的开源运行时，提供安全沙箱环境。
- [Modal](https://modal.com/) - 理想的无服务器云平台，适合运行智能体工作负载。
- [Fly.io](https://fly.io/) - 全球化运行智能体应用的平台。
- [Daytona](https://github.com/daytonaio/daytona) - 支持智能体的开源开发环境管理器。
- [Runloop](https://runloop.ai/) - 专为 AI 编码智能体打造的云基础设施。
- [Morph](https://github.com/morphcloud/morph) - 用于创建、快照和管理 AI 智能体环境的云平台。

## 语音与多模态智能体

*构建能听、能看、能说的智能体的框架。*

- [Pipecat](https://github.com/pipecat-ai/pipecat) - 面向语音和多模态对话 AI 的开源框架。
- [LiveKit Agents](https://github.com/livekit/agents) - 构建实时多模态 AI 智能体的框架。
- [Vocode](https://github.com/vocodedev/vocode-core) - 构建基于语音的大语言模型智能体的开源库。
- [Retell AI](https://www.retell.ai/) - 构建和部署语音 AI 智能体的平台。
- [Vapi](https://vapi.ai/) - 构建、测试和部署语音 AI 智能体的平台。
- [Bland AI](https://www.bland.ai/) - 构建 AI 电话呼叫智能体的 API。
- [OpenAI Realtime API](https://platform.openai.com/docs/guides/realtime) - 低延迟多模态 API，支持语音到语音交互。

## 智能体部署与基础设施

*在生产环境中部署和运行智能体的平台和工具。*

- [LangServe](https://github.com/langchain-ai/langserve) - 将 LangChain 可运行组件和链部署为 REST API。
- [BentoML](https://github.com/bentoml/BentoML) - 用于服务、管理和部署机器学习模型及智能体的框架。
- [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - 可扩展的模型服务库，用于构建在线推理 API。
- [LiteLLM](https://github.com/BerriAI/litellm) - 统一接口，以 OpenAI 格式调用 100 多种大语言模型 API。
- [vLLM](https://github.com/vllm-project/vllm) - 高吞吐量、高效内存利用的大语言模型推理引擎。
- [Ollama](https://github.com/ollama/ollama) - 轻松设置即可在本地运行大语言模型。
- [LM Studio](https://lmstudio.ai/) - 运行本地大语言模型的桌面应用，提供 OpenAI 兼容 API。
- [OpenRouter](https://openrouter.ai/) - 访问多个大语言模型提供商的统一 API。

## 浏览器与网页智能体

*能够浏览和交互操作网页浏览器的智能体。*

- [Browser Use](https://github.com/browser-use/browser-use) - 使网站对 AI 智能体可访问的库。
- [Playwright MCP](https://github.com/anthropics/anthropic-quickstarts/tree/main/mcp-server-playwright) - 通过 Playwright 实现浏览器自动化的 MCP 服务器。
- [Stagehand](https://github.com/browserbase/stagehand) - Browserbase 开发的 AI 驱动的浏览器自动化框架。
- [Skyvern](https://github.com/Skyvern-AI/skyvern) - 使用大语言模型和计算机视觉自动化基于浏览器的工作流。
- [LaVague](https://github.com/lavague-ai/LaVague) - 大型行动模型框架，用于自动化网页交互。
- [Browserbase](https://www.browserbase.com/) - 面向 AI 智能体的云浏览器基础设施。
- [MultiOn](https://www.multion.ai/) - 代替用户与网站交互的 AI 智能体。
- [WebVoyager](https://github.com/MinorJerry/WebVoyager) - 使用大型多模态模型构建端到端网页智能体。

## 研究型智能体

*专注于研究、分析和信息收集的智能体。*

- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) - 自主进行全面在线研究的智能体。
- [STORM](https://github.com/stanford-oval/storm) - 斯坦福的大语言模型驱动的知识策展系统，用于生成研究文章。
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG) - 为研究寻找最优 RAG 管道的 AutoML 工具。
- [Tavily](https://tavily.com/) - 为 AI 智能体和 RAG 应用优化的搜索 API。
- [Exa](https://exa.ai/) - 为 AI 设计的搜索引擎，基于嵌入向量搜索。
- [Perplexity API](https://docs.perplexity.ai/) - AI 驱动的搜索和研究 API。

## 工作流与任务自动化

*使用 AI 智能体构建自动化工作流的平台。*

- [n8n](https://github.com/n8n-io/n8n) - 具有 AI 智能体节点的工作流自动化工具。
- [Langflow](https://github.com/langflow-ai/langflow) - 构建多智能体和 RAG 应用的可视化框架。
- [Flowise](https://github.com/FlowiseAI/Flowise) - 拖拽式 UI，构建自定义的大语言模型流程。
- [Dify](https://github.com/langgenius/dify) - 构建具有智能体工作流的 AI 原生应用平台。
- [Activepieces](https://github.com/activepieces/activepieces) - 具有 AI 功能的开源自动化工具。
- [Temporal](https://github.com/temporalio/temporal) - 持久化执行平台，非常适合复杂的智能体工作流。
- [Inngest](https://github.com/inngest/inngest) - 事件驱动平台，用于运行可靠的 AI 工作流。
- [Prefect](https://github.com/PrefectHQ/prefect) - 支持 AI/ML 的工作流编排框架。

## 智能体通信协议

*智能体间及智能体与系统间通信的标准和协议。*

- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) - Anthropic 的开放协议，用于将 AI 模型连接到数据源和工具。
- [Agent2Agent (A2A)](https://github.com/google/A2A) - Google 的智能体间通信开放协议。
- [Agent Communication Protocol (ACP)](https://github.com/agntcy/acp-spec) - Cisco 的智能体通信协议规范。
- [Agent Network Protocol (ANP)](https://github.com/agent-network-protocol/agent-network-protocol) - 构建开放智能体网络的开放协议。
- [OpenAPI](https://www.openapis.org/) - 定义智能体可消费的 REST API 的标准。

## 学习资源

*构建 AI 智能体的教程、课程和指南。*

- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) - Lilian Weng 关于智能体架构的全面博客文章。
- [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) - Anthropic 的实用 AI 智能体构建指南。
- [The AI Agent Landscape](https://www.langchain.com/stateofaiagents) - LangChain 对智能体生态的全面概述。
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course) - 免费的 AI 智能体构建课程。
- [DeepLearning.AI Agent Courses](https://www.deeplearning.ai/) - Andrew Ng 的使用各种框架构建 AI 智能体的课程。
- [AI Agent Infrastructure](https://a16z.com/ai-agent-infrastructure/) - a16z 对新兴 AI 智能体技术栈的分析。

## 研究论文

*关于 AI 智能体架构和技术的重要学术论文。*

- [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) - 关于在语言模型中结合推理与行动的奠基性论文。
- [Toolformer](https://arxiv.org/abs/2302.04761) - 训练语言模型决定调用哪些工具、何时调用及使用什么参数。
- [Reflexion](https://arxiv.org/abs/2303.11366) - 具有语言强化学习能力的语言智能体。
- [Generative Agents](https://arxiv.org/abs/2304.03442) - 人类行为的交互式仿真。
- [Voyager](https://arxiv.org/abs/2305.16291) - 基于大语言模型的开放式具身智能体。
- [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) - 激发大语言模型推理能力的思维链提示。
- [Tree of Thoughts](https://arxiv.org/abs/2305.10601) - 使用大语言模型进行深思熟虑的问题求解。
- [LATS](https://arxiv.org/abs/2310.04406) - 语言智能体树搜索，统一推理、行动和规划。
- [AutoGPT Paper](https://arxiv.org/abs/2306.02224) - 对自主智能体系统能力的全面研究。

## 社区

- [r/AI_Agents](https://www.reddit.com/r/AI_Agents/) - 专注于 AI 智能体的 Reddit 社区。
- [LangChain Discord](https://discord.gg/langchain) - LangChain 社区 Discord 服务器。
- [AI Agent Dev Discord](https://discord.gg/aiagents) - AI 智能体开发者社区。
- [Hugging Face Forum](https://discuss.huggingface.co/) - 机器学习和智能体讨论论坛。

---

## Star 历史

<a href="https://star-history.com/#AstreoX/awesome-agent-tools&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date" />
 </picture>
</a>

---

## 贡献

欢迎贡献！请先阅读[贡献指南](CONTRIBUTING.md)。

## 许可证

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

在法律允许的范围内，贡献者已放弃本作品的所有版权及相关或邻接权利。
