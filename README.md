<div align="center">

<!-- Title & Badges -->
# Awesome Agent Tools

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/AstreoX/awesome-agent-tools/graphs/commit-activity)

**A curated list of frameworks, platforms, tools, and resources for building, orchestrating, and deploying AI agents.**

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [Español](README.es.md)

<sub>AI agents are autonomous systems powered by LLMs that can reason, plan, use tools, and take actions to accomplish complex tasks. <br/>This list tracks the rapidly evolving ecosystem of agent tooling.</sub>

**[What is an AI Agent?](#what-is-an-ai-agent) | [How to Contribute](CONTRIBUTING.md)**

</div>

---

## Contents

- [Agent Frameworks](#agent-frameworks)
- [Multi-Agent Orchestration](#multi-agent-orchestration)
- [Code Agents](#code-agents)
- [Tool Use & Function Calling](#tool-use--function-calling)
- [Model Context Protocol (MCP)](#model-context-protocol-mcp)
- [Agent Memory](#agent-memory)
- [RAG for Agents](#rag-for-agents)
- [Agent Monitoring & Observability](#agent-monitoring--observability)
- [Agent Evaluation & Testing](#agent-evaluation--testing)
- [Agent Security & Guardrails](#agent-security--guardrails)
- [Agent-Native Development](#agent-native-development)
- [Voice & Multimodal Agents](#voice--multimodal-agents)
- [Agent Deployment & Infrastructure](#agent-deployment--infrastructure)
- [Browser & Web Agents](#browser--web-agents)
- [Research Agents](#research-agents)
- [Workflow & Task Automation](#workflow--task-automation)
- [Agent Communication Protocols](#agent-communication-protocols)
- [Learning Resources](#learning-resources)
- [Research Papers](#research-papers)
- [Community](#community)

---

## What is an AI Agent?

An AI agent is a system that uses an LLM as its core reasoning engine and can:

- **Reason** about problems and plan solutions
- **Act** by calling tools, APIs, or executing code
- **Observe** the results of its actions
- **Iterate** until the task is complete

This distinguishes agents from simple chatbots or single-turn LLM applications.

---

## Agent Frameworks

*General-purpose frameworks for building AI agents.*

- [LangChain](https://github.com/langchain-ai/langchain) - Framework for developing applications powered by LLMs with composable chains and agents.
- [LangGraph](https://github.com/langchain-ai/langgraph) - Library for building stateful, multi-actor applications with LLMs, built on LangChain.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Framework for orchestrating role-playing autonomous AI agents.
- [AutoGen](https://github.com/microsoft/autogen) - Microsoft's framework for building multi-agent conversational systems.
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) - Microsoft's SDK for integrating LLMs into apps with plugin architecture.
- [Haystack](https://github.com/deepset-ai/haystack) - End-to-end NLP framework with agent capabilities and pipeline-based architecture.
- [LlamaIndex](https://github.com/run-llama/llama_index) - Data framework for LLM applications with agent abstractions.
- [Smolagents](https://github.com/huggingface/smolagents) - Hugging Face's minimal library for building powerful agents with code-first approach.
- [PydanticAI](https://github.com/pydantic/pydantic-ai) - Agent framework by the Pydantic team, using Pydantic for type-safe tool definitions.
- [Agno](https://github.com/agno-agi/agno) - Lightweight framework for building multi-modal agents with memory, knowledge, and tools.
- [Atomic Agents](https://github.com/BrainBlend-AI/atomic-agents) - Modular framework for building agent systems with atomic, composable components.
- [Letta](https://github.com/letta-ai/letta) - Framework for building stateful agents with long-term memory (formerly MemGPT).
- [Mirascope](https://github.com/Mirascope/mirascope) - Pythonic toolkit for building LLM-powered agents with a simple, elegant API.
- [ControlFlow](https://github.com/PrefectHQ/ControlFlow) - Python framework for building agentic workflows by Prefect.
- [Claude Agent SDK](https://github.com/anthropics/claude-code/tree/main/packages/claude-agent-sdk) - Anthropic's official SDK for building custom agents powered by Claude.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) - OpenAI's SDK for building agentic applications with handoffs and guardrails.
- [Google ADK](https://github.com/google/adk-python) - Google's Agent Development Kit for building AI agents.
- [Bee Agent Framework](https://github.com/i-am-bee/bee-agent-framework) - IBM's open-source framework for building, deploying, and serving agents.
- [Julep](https://github.com/julep-ai/julep) - Platform for building persistent AI agents with long-term memory and complex workflows.
- [Eliza](https://github.com/elizaOS/eliza) - Multi-agent simulation framework for creating autonomous AI characters.

## Multi-Agent Orchestration

*Tools for managing and coordinating multiple agents working together.*

- [AutoGen](https://github.com/microsoft/autogen) - Conversational multi-agent framework supporting diverse collaboration patterns.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Role-based multi-agent orchestration with sequential and hierarchical process flows.
- [LangGraph](https://github.com/langchain-ai/langgraph) - Stateful multi-agent graph framework with cycles and controllability.
- [OpenAI Swarm](https://github.com/openai/swarm) - Educational framework exploring ergonomic, lightweight multi-agent orchestration.
- [MetaGPT](https://github.com/geekan/MetaGPT) - Multi-agent framework that assigns different roles to GPTs to form a collaborative software entity.
- [ChatDev](https://github.com/OpenBMB/ChatDev) - Virtual software company powered by multiple intelligent agents in different roles.
- [Camel](https://github.com/camel-ai/camel) - Communicative agents for "Mind" exploration of LLM society.
- [Agency Swarm](https://github.com/VRSEN/agency-swarm) - Open-source framework for creating collaborative swarms of AI agents.
- [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one) - Microsoft's generalist multi-agent system for solving complex tasks.
- [Langtrace](https://github.com/Scale3-Labs/langtrace) - Open-source observability for multi-agent LLM applications.

## Code Agents

*Agents specialized for software engineering tasks.*

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) - Anthropic's agentic coding tool that operates directly in the terminal.
- [Cursor](https://cursor.com/) - AI-first code editor with built-in agent capabilities.
- [GitHub Copilot](https://github.com/features/copilot) - AI pair programmer with agent mode for multi-file editing and terminal commands.
- [Cline](https://github.com/cline/cline) - Autonomous coding agent in VS Code that can create/edit files, run commands, and use the browser.
- [Aider](https://github.com/Aider-AI/aider) - AI pair programming in the terminal with git integration.
- [Windsurf](https://codeium.com/windsurf) - Agentic IDE by Codeium with Cascade flows for multi-step coding.
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) - Platform for autonomous software development agents (formerly OpenDevin).
- [SWE-agent](https://github.com/princeton-nlp/SWE-agent) - Agent that autonomously fixes GitHub issues using an LM as the brain.
- [Devika](https://github.com/stitionai/Devika) - Agentic AI software engineer that can understand, plan, and write code.
- [GPT Engineer](https://github.com/gpt-engineer-org/gpt-engineer) - Agent that generates entire codebases from a single prompt.
- [Codex CLI](https://github.com/openai/codex) - OpenAI's lightweight coding agent that runs in the terminal.
- [Roo Code](https://github.com/RooVetGit/Roo-Code) - AI coding agent extension for VS Code with multi-model support.
- [Augment Code](https://www.augmentcode.com/) - AI coding agent with deep codebase understanding.
- [Tabnine](https://www.tabnine.com/) - AI coding assistant with agent-like code completions.
- [Trae](https://www.trae.ai/) - Adaptive AI IDE by ByteDance with Builder mode for agentic coding.
- [Kilo Code](https://github.com/kilocode-ai/kilocode) - Open-source VS Code extension bringing AI coding agents to your editor.

## Tool Use & Function Calling

*Libraries and frameworks for enabling LLMs to use tools and call functions.*

- [LangChain Tools](https://python.langchain.com/docs/modules/agents/tools/) - Extensive collection of pre-built tools and tool creation utilities.
- [Composio](https://github.com/ComposioHQ/composio) - Integration platform providing 250+ tools for AI agents with managed auth.
- [Toolhouse](https://toolhouse.ai/) - Cloud infrastructure for equipping LLMs with actions and knowledge.
- [ACI.dev](https://github.com/aipoool/aci) - Open-source platform providing unified tool-use infrastructure for AI agents.
- [Arcade AI](https://github.com/ArcadeAI/arcade-ai) - Tool-use platform that makes it easy to add tools to any LLM.
- [Instructor](https://github.com/jxnl/instructor) - Structured output library making function calling reliable.
- [Outlines](https://github.com/dottxt-ai/outlines) - Structured text generation for reliable tool use.
- [NPI](https://github.com/npi-ai/npi) - Tool-use API platform enabling agents to operate various software tools.

## Model Context Protocol (MCP)

*Tools and servers implementing Anthropic's Model Context Protocol for standardized tool integration.*

- [MCP Specification](https://modelcontextprotocol.io/) - The official Model Context Protocol specification.
- [MCP Servers](https://github.com/modelcontextprotocol/servers) - Official reference implementations of MCP servers.
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - Official TypeScript SDK for building MCP clients and servers.
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) - Official Python SDK for building MCP clients and servers.
- [MCP Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk) - Official Kotlin SDK for building MCP servers and clients on JVM.
- [FastMCP](https://github.com/jlowin/fastmcp) - Fast, Pythonic way to build MCP servers and clients.
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - Curated list of MCP server implementations.
- [mcp-use](https://github.com/pietrozullo/mcp-use) - Open-source library to connect any LLM to any MCP server.
- [Smithery](https://smithery.ai/) - Registry and marketplace for discovering and deploying MCP servers.
- [Glama](https://glama.ai/mcp/servers) - MCP server discovery and directory platform.
- [mcpx](https://github.com/ArcadeAI/mcpx) - Runner for MCP servers with one-command install and run.
- [Statsnet](https://github.com/usenetstate/statsnet-mcp) - Background check any company in the world: registration, executives, courts and finances. Remote MCP: https://statsnet.co/mcp

## Agent Memory

*Systems for providing agents with short-term and long-term memory.*

- [Mem0](https://github.com/mem0ai/mem0) - Self-improving memory layer for LLM applications.
- [Letta](https://github.com/letta-ai/letta) - Stateful agents with long-term memory management (formerly MemGPT).
- [Zep](https://github.com/getzep/zep) - Long-term memory for AI assistants with automatic summarization.
- [Motorhead](https://github.com/getmetal/motorhead) - Memory and context management server for LLMs.
- [LangMem](https://github.com/langchain-ai/langmem) - LangChain's SDK for long-term memory in LLM applications.
- [Cognee](https://github.com/topoteretes/cognee) - Memory management for AI agents using knowledge graphs and vector stores.

## RAG for Agents

*Retrieval-Augmented Generation tools that enhance agent knowledge.*

- [LlamaIndex](https://github.com/run-llama/llama_index) - Data framework for connecting custom data to LLMs with advanced retrieval.
- [ChromaDB](https://github.com/chroma-core/chroma) - Open-source embedding database for AI applications.
- [Weaviate](https://github.com/weaviate/weaviate) - Open-source vector database for scalable AI applications.
- [Qdrant](https://github.com/qdrant/qdrant) - High-performance vector similarity search engine.
- [Pinecone](https://www.pinecone.io/) - Managed vector database for high-performance AI applications.
- [Milvus](https://github.com/milvus-io/milvus) - Open-source vector database built for scalable similarity search.
- [Unstructured](https://github.com/Unstructured-IO/unstructured) - Library for preprocessing and ingesting documents for RAG pipelines.
- [R2R](https://github.com/SciPhi-AI/R2R) - Production-ready RAG engine with agent capabilities.
- [RAGFlow](https://github.com/infiniflow/ragflow) - Open-source RAG engine based on deep document understanding.
- [LightRAG](https://github.com/HKUDS/LightRAG) - Simple and fast RAG engine using graph structures for indexing.

## Agent Monitoring & Observability

*Tools for tracking, debugging, and understanding agent behavior.*

- [LangSmith](https://smith.langchain.com/) - Platform for debugging, testing, evaluating, and monitoring LLM applications.
- [LangFuse](https://github.com/langfuse/langfuse) - Open-source observability and analytics for LLM applications.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Open-source observability for LLM applications with tracing and evaluation.
- [Helicone](https://github.com/Helicone/helicone) - Open-source LLM observability platform with logging and analytics.
- [Braintrust](https://github.com/braintrustdata/braintrust-sdk) - Enterprise-grade stack for building, shipping, and monitoring AI products.
- [Weave](https://github.com/wandb/weave) - Weights & Biases toolkit for tracking and evaluating LLM applications.
- [AgentOps](https://github.com/AgentOps-AI/agentops) - Python SDK for AI agent monitoring, testing, and replay analytics.
- [OpenLLMetry](https://github.com/traceloop/openllmetry) - Open-source observability for LLMs based on OpenTelemetry.
- [Pydantic Logfire](https://github.com/pydantic/logfire) - Observability platform with first-class support for Pydantic and LLM applications.

## Agent Evaluation & Testing

*Frameworks for evaluating and benchmarking agent performance.*

- [SWE-bench](https://github.com/princeton-nlp/SWE-bench) - Benchmark for evaluating LMs on real-world software engineering problems.
- [GAIA](https://huggingface.co/gaia-benchmark) - Benchmark for general AI assistants on real-world tasks.
- [AgentBench](https://github.com/THUDM/AgentBench) - Benchmark for evaluating LLMs as agents across diverse environments.
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) - Framework for large language model evaluations by UK AISI.
- [RAGAS](https://github.com/explodinggradients/ragas) - Evaluation framework for RAG pipelines.
- [DeepEval](https://github.com/confident-ai/deepeval) - LLM evaluation framework with 14+ metrics.
- [Promptfoo](https://github.com/promptfoo/promptfoo) - Tool for testing and evaluating LLM outputs.
- [TauBench](https://github.com/sierra-research/tau-bench) - Benchmark for evaluating tool-agent-user interactions in real-world domains.
- [Agent-as-a-Judge](https://github.com/metauto-ai/agent-as-a-judge) - Using agents to evaluate agent outputs.

## Agent Security & Guardrails

*Tools for making agents safe, secure, and controllable.*

- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Framework for adding structural, type, and quality guarantees to LLM outputs.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - NVIDIA's toolkit for adding programmable guardrails to LLM-based apps.
- [LLM Guard](https://github.com/protectai/llm-guard) - Security toolkit for LLM interactions with input/output scanning.
- [Rebuff](https://github.com/protectai/rebuff) - Self-hardening prompt injection detector.
- [Lakera Guard](https://www.lakera.ai/) - Real-time AI security for protecting against prompt injection and data leakage.
- [Invariant Labs](https://github.com/invariantlabs-ai/invariant) - Security testing and enforcement for AI agents.
- [Prompt Armor](https://promptarmor.com/) - Protection against prompt injection attacks.

## Agent-Native Development

*Tools and platforms built from the ground up for agent-driven development.*

- [E2B](https://github.com/e2b-dev/e2b) - Open-source runtime for AI agents with secure sandboxed environments.
- [Modal](https://modal.com/) - Serverless cloud platform ideal for running agent workloads.
- [Fly.io](https://fly.io/) - Platform for running agent applications globally.
- [Daytona](https://github.com/daytonaio/daytona) - Open-source development environment manager with agent support.
- [Runloop](https://runloop.ai/) - Cloud infrastructure purpose-built for AI coding agents.
- [Morph](https://github.com/morphcloud/morph) - Cloud platform for creating, snapshotting, and managing AI agent environments.

## Voice & Multimodal Agents

*Frameworks for building agents that can hear, see, and speak.*

- [Pipecat](https://github.com/pipecat-ai/pipecat) - Open-source framework for voice and multimodal conversational AI.
- [LiveKit Agents](https://github.com/livekit/agents) - Framework for building real-time multimodal AI agents.
- [Vocode](https://github.com/vocodedev/vocode-core) - Open-source library for building voice-based LLM agents.
- [Retell AI](https://www.retell.ai/) - Platform for building and deploying voice AI agents.
- [Vapi](https://vapi.ai/) - Platform for building, testing, and deploying voice AI agents.
- [Bland AI](https://www.bland.ai/) - API for building AI phone calling agents.
- [OpenAI Realtime API](https://platform.openai.com/docs/guides/realtime) - Low-latency multimodal API for speech-to-speech interactions.

## Agent Deployment & Infrastructure

*Platforms and tools for deploying and serving agents in production.*

- [LangServe](https://github.com/langchain-ai/langserve) - Deploy LangChain runnables and chains as REST APIs.
- [BentoML](https://github.com/bentoml/BentoML) - Framework for serving, managing, and deploying ML models and agents.
- [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Scalable model serving library for building online inference APIs.
- [LiteLLM](https://github.com/BerriAI/litellm) - Unified interface to call 100+ LLM APIs in OpenAI format.
- [vLLM](https://github.com/vllm-project/vllm) - High-throughput and memory-efficient inference engine for LLMs.
- [Ollama](https://github.com/ollama/ollama) - Run LLMs locally with easy setup.
- [LM Studio](https://lmstudio.ai/) - Desktop app for running local LLMs with an OpenAI-compatible API.
- [OpenRouter](https://openrouter.ai/) - Unified API for accessing multiple LLM providers.

## Browser & Web Agents

*Agents that can navigate and interact with web browsers.*

- [Browser Use](https://github.com/browser-use/browser-use) - Library for making websites accessible to AI agents.
- [Playwright MCP](https://github.com/anthropics/anthropic-quickstarts/tree/main/mcp-server-playwright) - MCP server for browser automation via Playwright.
- [Stagehand](https://github.com/browserbase/stagehand) - AI-powered browser automation framework by Browserbase.
- [Skyvern](https://github.com/Skyvern-AI/skyvern) - Automate browser-based workflows using LLMs and computer vision.
- [LaVague](https://github.com/lavague-ai/LaVague) - Large Action Model framework for automating web interactions.
- [Browserbase](https://www.browserbase.com/) - Cloud browser infrastructure for AI agents.
- [MultiOn](https://www.multion.ai/) - AI agent for interacting with websites on behalf of users.
- [WebVoyager](https://github.com/MinorJerry/WebVoyager) - Building an end-to-end web agent with LMMs.

## Research Agents

*Agents specialized for research, analysis, and information gathering.*

- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) - Autonomous agent for comprehensive online research.
- [STORM](https://github.com/stanford-oval/storm) - Stanford's LLM-powered knowledge curation system for research articles.
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG) - AutoML tool for finding optimal RAG pipelines for research.
- [Tavily](https://tavily.com/) - Search API optimized for AI agents and RAG applications.
- [Exa](https://exa.ai/) - Search engine designed for AI with embeddings-based search.
- [Perplexity API](https://docs.perplexity.ai/) - API for AI-powered search and research.

## Workflow & Task Automation

*Platforms for building automated workflows with AI agents.*

- [n8n](https://github.com/n8n-io/n8n) - Workflow automation tool with AI agent nodes.
- [Langflow](https://github.com/langflow-ai/langflow) - Visual framework for building multi-agent and RAG applications.
- [Flowise](https://github.com/FlowiseAI/Flowise) - Drag-and-drop UI to build customized LLM flows.
- [Dify](https://github.com/langgenius/dify) - Platform for building AI-native applications with agent workflows.
- [Activepieces](https://github.com/activepieces/activepieces) - Open-source automation tool with AI capabilities.
- [Temporal](https://github.com/temporalio/temporal) - Durable execution platform ideal for complex agent workflows.
- [Inngest](https://github.com/inngest/inngest) - Event-driven platform for running reliable AI workflows.
- [Prefect](https://github.com/PrefectHQ/prefect) - Workflow orchestration framework with AI/ML support.

## Agent Communication Protocols

*Standards and protocols for agent-to-agent and agent-to-system communication.*

- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) - Anthropic's open protocol for connecting AI models to data sources and tools.
- [Agent2Agent (A2A)](https://github.com/google/A2A) - Google's open protocol for agent-to-agent communication.
- [Agent Communication Protocol (ACP)](https://github.com/agntcy/acp-spec) - Cisco's protocol specification for agent communication.
- [Agent Network Protocol (ANP)](https://github.com/agent-network-protocol/agent-network-protocol) - Open protocol for building an open agent network.
- [OpenAPI](https://www.openapis.org/) - Standard for defining REST APIs that agents can consume.

## Learning Resources

*Tutorials, courses, and guides for building AI agents.*

- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) - Lilian Weng's comprehensive blog post on agent architectures.
- [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) - Anthropic's guide to building practical AI agents.
- [The AI Agent Landscape](https://www.langchain.com/stateofaiagents) - LangChain's comprehensive overview of the agent ecosystem.
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course) - Free course on building AI agents.
- [DeepLearning.AI Agent Courses](https://www.deeplearning.ai/) - Andrew Ng's courses on building AI agents with various frameworks.
- [AI Agent Infrastructure](https://a16z.com/ai-agent-infrastructure/) - a16z's analysis of the emerging AI agent stack.

## Research Papers

*Key academic papers on AI agent architectures and techniques.*

- [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) - Foundational paper on combining reasoning and acting in LMs.
- [Toolformer](https://arxiv.org/abs/2302.04761) - Training LMs to decide which tools to call, when, and with what arguments.
- [Reflexion](https://arxiv.org/abs/2303.11366) - Language agents with verbal reinforcement learning.
- [Generative Agents](https://arxiv.org/abs/2304.03442) - Interactive simulacra of human behavior.
- [Voyager](https://arxiv.org/abs/2305.16291) - Open-ended embodied agent with LLMs.
- [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) - Eliciting reasoning in LLMs.
- [Tree of Thoughts](https://arxiv.org/abs/2305.10601) - Deliberate problem solving with LLMs.
- [LATS](https://arxiv.org/abs/2310.04406) - Language agent tree search unifies reasoning, acting, and planning.
- [AutoGPT Paper](https://arxiv.org/abs/2306.02224) - A comprehensive study on the capabilities of auto-agent systems.

## Community

- [r/AI_Agents](https://www.reddit.com/r/AI_Agents/) - Reddit community focused on AI agents.
- [LangChain Discord](https://discord.gg/langchain) - LangChain community Discord server.
- [AI Agent Dev Discord](https://discord.gg/aiagents) - Community for AI agent developers.
- [Hugging Face Forum](https://discuss.huggingface.co/) - Discussion forum for ML and agents.

---

## Star History

<a href="https://star-history.com/#AstreoX/awesome-agent-tools&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date" />
 </picture>
</a>

---

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
