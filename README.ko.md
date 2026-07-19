<div align="center">

<!-- Title & Badges -->
# Awesome Agent Tools

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/AstreoX/awesome-agent-tools/graphs/commit-activity)

**AI 에이전트를 구축, 오케스트레이션 및 배포하기 위한 프레임워크, 플랫폼, 도구, 리소스 모음집.**

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [Español](README.es.md)

<sub>AI 에이전트는 LLM을 기반으로 추론, 계획, 도구 사용, 행동 수행을 통해 복잡한 작업을 처리하는 자율 시스템입니다. <br/>이 목록은 빠르게 발전하는 에이전트 도구 생태계를 추적합니다.</sub>

**[AI 에이전트란?](#ai-에이전트란) | [기여 방법](CONTRIBUTING.md)**

</div>

---

## 목차

- [에이전트 프레임워크](#에이전트-프레임워크)
- [멀티 에이전트 오케스트레이션](#멀티-에이전트-오케스트레이션)
- [코드 에이전트](#코드-에이전트)
- [도구 사용 및 함수 호출](#도구-사용-및-함수-호출)
- [Model Context Protocol (MCP)](#model-context-protocol-mcp)
- [에이전트 메모리](#에이전트-메모리)
- [에이전트를 위한 RAG](#에이전트를-위한-rag)
- [에이전트 모니터링 및 관측 가능성](#에이전트-모니터링-및-관측-가능성)
- [에이전트 평가 및 테스트](#에이전트-평가-및-테스트)
- [에이전트 보안 및 가드레일](#에이전트-보안-및-가드레일)
- [에이전트 네이티브 개발](#에이전트-네이티브-개발)
- [음성 및 멀티모달 에이전트](#음성-및-멀티모달-에이전트)
- [에이전트 배포 및 인프라](#에이전트-배포-및-인프라)
- [브라우저 및 웹 에이전트](#브라우저-및-웹-에이전트)
- [리서치 에이전트](#리서치-에이전트)
- [워크플로 및 작업 자동화](#워크플로-및-작업-자동화)
- [에이전트 통신 프로토콜](#에이전트-통신-프로토콜)
- [학습 자료](#학습-자료)
- [연구 논문](#연구-논문)
- [커뮤니티](#커뮤니티)

---

## AI 에이전트란?

AI 에이전트는 LLM을 핵심 추론 엔진으로 사용하며 다음을 수행할 수 있는 시스템입니다:

- **추론** - 문제를 분석하고 해결책을 계획
- **행동** - 도구, API 호출 또는 코드 실행
- **관찰** - 행동 결과를 확인
- **반복** - 작업이 완료될 때까지 반복 수행

이러한 특성이 에이전트를 단순한 챗봇이나 단일 턴 LLM 애플리케이션과 구별합니다.

---

## 에이전트 프레임워크

*AI 에이전트를 구축하기 위한 범용 프레임워크.*

- [LangChain](https://github.com/langchain-ai/langchain) - 조합 가능한 체인과 에이전트로 LLM 기반 애플리케이션을 개발하기 위한 프레임워크.
- [LangGraph](https://github.com/langchain-ai/langgraph) - LangChain 기반으로 상태를 가진 멀티 액터 LLM 애플리케이션을 구축하기 위한 라이브러리.
- [CrewAI](https://github.com/crewAIInc/crewAI) - 역할 기반 자율 AI 에이전트를 오케스트레이션하기 위한 프레임워크.
- [AutoGen](https://github.com/microsoft/autogen) - 멀티 에이전트 대화 시스템을 구축하기 위한 Microsoft의 프레임워크.
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) - 플러그인 아키텍처로 LLM을 앱에 통합하기 위한 Microsoft의 SDK.
- [Haystack](https://github.com/deepset-ai/haystack) - 에이전트 기능과 파이프라인 기반 아키텍처를 갖춘 엔드투엔드 NLP 프레임워크.
- [LlamaIndex](https://github.com/run-llama/llama_index) - 에이전트 추상화를 갖춘 LLM 애플리케이션용 데이터 프레임워크.
- [Smolagents](https://github.com/huggingface/smolagents) - 코드 우선 접근 방식으로 강력한 에이전트를 구축하기 위한 Hugging Face의 경량 라이브러리.
- [PydanticAI](https://github.com/pydantic/pydantic-ai) - 타입 안전한 도구 정의를 위해 Pydantic을 사용하는 Pydantic 팀의 에이전트 프레임워크.
- [Agno](https://github.com/agno-agi/agno) - 메모리, 지식, 도구를 갖춘 멀티모달 에이전트 구축을 위한 경량 프레임워크.
- [Atomic Agents](https://github.com/BrainBlend-AI/atomic-agents) - 원자적이고 조합 가능한 컴포넌트로 에이전트 시스템을 구축하기 위한 모듈형 프레임워크.
- [Letta](https://github.com/letta-ai/letta) - 장기 메모리를 갖춘 상태 기반 에이전트 구축 프레임워크 (이전 MemGPT).
- [Mirascope](https://github.com/Mirascope/mirascope) - 간결하고 우아한 API로 LLM 기반 에이전트를 구축하기 위한 파이썬 툴킷.
- [ControlFlow](https://github.com/PrefectHQ/ControlFlow) - Prefect가 만든 에이전트 워크플로 구축을 위한 Python 프레임워크.
- [Claude Agent SDK](https://github.com/anthropics/claude-code/tree/main/packages/claude-agent-sdk) - Claude를 기반으로 커스텀 에이전트를 구축하기 위한 Anthropic의 공식 SDK.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) - 핸드오프와 가드레일을 갖춘 에이전트 애플리케이션 구축을 위한 OpenAI의 SDK.
- [Google ADK](https://github.com/google/adk-python) - AI 에이전트 구축을 위한 Google의 Agent Development Kit.
- [Bee Agent Framework](https://github.com/i-am-bee/bee-agent-framework) - 에이전트 구축, 배포, 서빙을 위한 IBM의 오픈소스 프레임워크.
- [Julep](https://github.com/julep-ai/julep) - 장기 메모리와 복잡한 워크플로를 갖춘 영속적 AI 에이전트 구축 플랫폼.
- [Eliza](https://github.com/elizaOS/eliza) - 자율 AI 캐릭터를 생성하기 위한 멀티 에이전트 시뮬레이션 프레임워크.

## 멀티 에이전트 오케스트레이션

*여러 에이전트의 협업을 관리하고 조율하기 위한 도구.*

- [AutoGen](https://github.com/microsoft/autogen) - 다양한 협업 패턴을 지원하는 대화형 멀티 에이전트 프레임워크.
- [CrewAI](https://github.com/crewAIInc/crewAI) - 순차적 및 계층적 프로세스 흐름을 갖춘 역할 기반 멀티 에이전트 오케스트레이션.
- [LangGraph](https://github.com/langchain-ai/langgraph) - 순환과 제어 가능성을 갖춘 상태 기반 멀티 에이전트 그래프 프레임워크.
- [OpenAI Swarm](https://github.com/openai/swarm) - 인체공학적이고 경량화된 멀티 에이전트 오케스트레이션을 탐구하는 교육용 프레임워크.
- [MetaGPT](https://github.com/geekan/MetaGPT) - GPT에 다양한 역할을 부여하여 협업 소프트웨어 엔티티를 구성하는 멀티 에이전트 프레임워크.
- [ChatDev](https://github.com/OpenBMB/ChatDev) - 다양한 역할의 여러 지능형 에이전트로 운영되는 가상 소프트웨어 회사.
- [Camel](https://github.com/camel-ai/camel) - LLM 사회의 "마음" 탐구를 위한 커뮤니케이션 에이전트.
- [Agency Swarm](https://github.com/VRSEN/agency-swarm) - AI 에이전트 협업 스웜을 생성하기 위한 오픈소스 프레임워크.
- [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one) - 복잡한 작업을 해결하기 위한 Microsoft의 범용 멀티 에이전트 시스템.
- [Langtrace](https://github.com/Scale3-Labs/langtrace) - 멀티 에이전트 LLM 애플리케이션을 위한 오픈소스 관측 도구.

## 코드 에이전트

*소프트웨어 엔지니어링 작업에 특화된 에이전트.*

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) - 터미널에서 직접 작동하는 Anthropic의 에이전트형 코딩 도구.
- [Cursor](https://cursor.com/) - 내장 에이전트 기능을 갖춘 AI 퍼스트 코드 에디터.
- [GitHub Copilot](https://github.com/features/copilot) - 멀티 파일 편집 및 터미널 명령을 위한 에이전트 모드를 갖춘 AI 페어 프로그래머.
- [Cline](https://github.com/cline/cline) - 파일 생성/편집, 명령 실행, 브라우저 사용이 가능한 VS Code 자율 코딩 에이전트.
- [Aider](https://github.com/Aider-AI/aider) - git 통합을 갖춘 터미널 기반 AI 페어 프로그래밍.
- [Windsurf](https://codeium.com/windsurf) - 다단계 코딩을 위한 Cascade 흐름을 갖춘 Codeium의 에이전트형 IDE.
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) - 자율 소프트웨어 개발 에이전트 플랫폼 (이전 OpenDevin).
- [SWE-agent](https://github.com/princeton-nlp/SWE-agent) - LM을 두뇌로 사용하여 GitHub 이슈를 자율적으로 해결하는 에이전트.
- [Devika](https://github.com/stitionai/Devika) - 이해, 계획, 코드 작성이 가능한 에이전트형 AI 소프트웨어 엔지니어.
- [GPT Engineer](https://github.com/gpt-engineer-org/gpt-engineer) - 단일 프롬프트로 전체 코드베이스를 생성하는 에이전트.
- [Codex CLI](https://github.com/openai/codex) - 터미널에서 실행되는 OpenAI의 경량 코딩 에이전트.
- [Roo Code](https://github.com/RooVetGit/Roo-Code) - 멀티 모델을 지원하는 VS Code용 AI 코딩 에이전트 확장 프로그램.
- [Augment Code](https://www.augmentcode.com/) - 코드베이스에 대한 깊은 이해를 갖춘 AI 코딩 에이전트.
- [Tabnine](https://www.tabnine.com/) - 에이전트형 코드 완성 기능을 갖춘 AI 코딩 어시스턴트.
- [Trae](https://www.trae.ai/) - 에이전트형 코딩을 위한 Builder 모드를 갖춘 ByteDance의 적응형 AI IDE.
- [Kilo Code](https://github.com/kilocode-ai/kilocode) - 에디터에 AI 코딩 에이전트를 제공하는 오픈소스 VS Code 확장 프로그램.

## 도구 사용 및 함수 호출

*LLM이 도구를 사용하고 함수를 호출할 수 있도록 하는 라이브러리 및 프레임워크.*

- [LangChain Tools](https://python.langchain.com/docs/modules/agents/tools/) - 사전 구축된 도구와 도구 생성 유틸리티의 광범위한 컬렉션.
- [Composio](https://github.com/ComposioHQ/composio) - 관리형 인증을 갖춘 AI 에이전트용 250개 이상의 도구를 제공하는 통합 플랫폼.
- [Toolhouse](https://toolhouse.ai/) - LLM에 액션과 지식을 장착하기 위한 클라우드 인프라.
- [ACI.dev](https://github.com/aipoool/aci) - AI 에이전트를 위한 통합 도구 사용 인프라를 제공하는 오픈소스 플랫폼.
- [Arcade AI](https://github.com/ArcadeAI/arcade-ai) - 모든 LLM에 도구를 쉽게 추가할 수 있는 도구 사용 플랫폼.
- [Instructor](https://github.com/jxnl/instructor) - 함수 호출을 신뢰성 있게 만드는 구조화된 출력 라이브러리.
- [Outlines](https://github.com/dottxt-ai/outlines) - 신뢰할 수 있는 도구 사용을 위한 구조화된 텍스트 생성.
- [NPI](https://github.com/npi-ai/npi) - 에이전트가 다양한 소프트웨어 도구를 조작할 수 있게 하는 도구 사용 API 플랫폼.

## Model Context Protocol (MCP)

*표준화된 도구 통합을 위한 Anthropic의 Model Context Protocol을 구현하는 도구 및 서버.*

- [MCP Specification](https://modelcontextprotocol.io/) - 공식 Model Context Protocol 명세.
- [MCP Servers](https://github.com/modelcontextprotocol/servers) - MCP 서버의 공식 참조 구현체.
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - MCP 클라이언트 및 서버 구축을 위한 공식 TypeScript SDK.
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) - MCP 클라이언트 및 서버 구축을 위한 공식 Python SDK.
- [MCP Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk) - JVM에서 MCP 서버 및 클라이언트 구축을 위한 공식 Kotlin SDK.
- [FastMCP](https://github.com/jlowin/fastmcp) - 빠르고 파이썬다운 방식으로 MCP 서버 및 클라이언트를 구축.
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - MCP 서버 구현체 큐레이션 목록.
- [mcp-use](https://github.com/pietrozullo/mcp-use) - 모든 LLM을 모든 MCP 서버에 연결하기 위한 오픈소스 라이브러리.
- [Smithery](https://smithery.ai/) - MCP 서버를 검색하고 배포하기 위한 레지스트리 및 마켓플레이스.
- [Glama](https://glama.ai/mcp/servers) - MCP 서버 검색 및 디렉토리 플랫폼.
- [mcpx](https://github.com/arcadeai-labs/mcpx) - MCP 서버를 검사하고 호출하는 명령줄 클라이언트.

## 에이전트 메모리

*에이전트에 단기 및 장기 메모리를 제공하기 위한 시스템.*

- [Mem0](https://github.com/mem0ai/mem0) - LLM 애플리케이션을 위한 자기 개선 메모리 레이어.
- [Letta](https://github.com/letta-ai/letta) - 장기 메모리 관리를 갖춘 상태 기반 에이전트 (이전 MemGPT).
- [Zep](https://github.com/getzep/zep) - 자동 요약 기능을 갖춘 AI 어시스턴트용 장기 메모리.
- [Motorhead](https://github.com/getmetal/motorhead) - LLM을 위한 메모리 및 컨텍스트 관리 서버.
- [LangMem](https://github.com/langchain-ai/langmem) - LLM 애플리케이션의 장기 메모리를 위한 LangChain의 SDK.
- [Cognee](https://github.com/topoteretes/cognee) - 지식 그래프와 벡터 스토어를 사용하는 AI 에이전트 메모리 관리.

## 에이전트를 위한 RAG

*에이전트의 지식을 강화하는 검색 증강 생성(RAG) 도구.*

- [LlamaIndex](https://github.com/run-llama/llama_index) - 고급 검색 기능으로 커스텀 데이터를 LLM에 연결하는 데이터 프레임워크.
- [ChromaDB](https://github.com/chroma-core/chroma) - AI 애플리케이션을 위한 오픈소스 임베딩 데이터베이스.
- [Weaviate](https://github.com/weaviate/weaviate) - 확장 가능한 AI 애플리케이션을 위한 오픈소스 벡터 데이터베이스.
- [Qdrant](https://github.com/qdrant/qdrant) - 고성능 벡터 유사성 검색 엔진.
- [Pinecone](https://www.pinecone.io/) - 고성능 AI 애플리케이션을 위한 관리형 벡터 데이터베이스.
- [Milvus](https://github.com/milvus-io/milvus) - 확장 가능한 유사성 검색을 위해 구축된 오픈소스 벡터 데이터베이스.
- [Unstructured](https://github.com/Unstructured-IO/unstructured) - RAG 파이프라인을 위한 문서 전처리 및 수집 라이브러리.
- [R2R](https://github.com/SciPhi-AI/R2R) - 에이전트 기능을 갖춘 프로덕션 레디 RAG 엔진.
- [RAGFlow](https://github.com/infiniflow/ragflow) - 심층 문서 이해 기반의 오픈소스 RAG 엔진.
- [LightRAG](https://github.com/HKUDS/LightRAG) - 인덱싱에 그래프 구조를 사용하는 간단하고 빠른 RAG 엔진.

## 에이전트 모니터링 및 관측 가능성

*에이전트 동작을 추적, 디버깅, 이해하기 위한 도구.*

- [LangSmith](https://smith.langchain.com/) - LLM 애플리케이션의 디버깅, 테스트, 평가, 모니터링을 위한 플랫폼.
- [LangFuse](https://github.com/langfuse/langfuse) - LLM 애플리케이션을 위한 오픈소스 관측 및 분석 도구.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - 트레이싱과 평가를 갖춘 LLM 애플리케이션용 오픈소스 관측 도구.
- [Helicone](https://github.com/Helicone/helicone) - 로깅과 분석을 갖춘 오픈소스 LLM 관측 플랫폼.
- [Braintrust](https://github.com/braintrustdata/braintrust-sdk) - AI 제품의 구축, 배포, 모니터링을 위한 엔터프라이즈급 스택.
- [Weave](https://github.com/wandb/weave) - LLM 애플리케이션 추적 및 평가를 위한 Weights & Biases 툴킷.
- [AgentOps](https://github.com/AgentOps-AI/agentops) - AI 에이전트 모니터링, 테스트, 리플레이 분석을 위한 Python SDK.
- [OpenLLMetry](https://github.com/traceloop/openllmetry) - OpenTelemetry 기반의 LLM 오픈소스 관측 도구.
- [Pydantic Logfire](https://github.com/pydantic/logfire) - Pydantic 및 LLM 애플리케이션을 위한 퍼스트클래스 지원을 갖춘 관측 플랫폼.

## 에이전트 평가 및 테스트

*에이전트 성능을 평가하고 벤치마킹하기 위한 프레임워크.*

- [SWE-bench](https://github.com/princeton-nlp/SWE-bench) - 실제 소프트웨어 엔지니어링 문제에 대한 LM 평가 벤치마크.
- [GAIA](https://huggingface.co/gaia-benchmark) - 실제 작업에 대한 범용 AI 어시스턴트 벤치마크.
- [AgentBench](https://github.com/THUDM/AgentBench) - 다양한 환경에서 에이전트로서의 LLM을 평가하기 위한 벤치마크.
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) - 영국 AISI의 대규모 언어 모델 평가 프레임워크.
- [RAGAS](https://github.com/explodinggradients/ragas) - RAG 파이프라인 평가 프레임워크.
- [DeepEval](https://github.com/confident-ai/deepeval) - 14개 이상의 메트릭을 갖춘 LLM 평가 프레임워크.
- [Promptfoo](https://github.com/promptfoo/promptfoo) - LLM 출력을 테스트하고 평가하기 위한 도구.
- [TauBench](https://github.com/sierra-research/tau-bench) - 실제 도메인에서 도구-에이전트-사용자 상호작용을 평가하기 위한 벤치마크.
- [Agent-as-a-Judge](https://github.com/metauto-ai/agent-as-a-judge) - 에이전트를 사용하여 에이전트 출력을 평가.

## 에이전트 보안 및 가드레일

*에이전트를 안전하고, 보안성 있고, 제어 가능하게 만들기 위한 도구.*

- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - LLM 출력에 구조적, 타입, 품질 보증을 추가하기 위한 프레임워크.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - LLM 기반 앱에 프로그래밍 가능한 가드레일을 추가하기 위한 NVIDIA의 툴킷.
- [LLM Guard](https://github.com/protectai/llm-guard) - 입출력 스캐닝을 갖춘 LLM 상호작용 보안 툴킷.
- [Rebuff](https://github.com/protectai/rebuff) - 자기 강화형 프롬프트 인젝션 감지기.
- [Lakera Guard](https://www.lakera.ai/) - 프롬프트 인젝션 및 데이터 유출 방지를 위한 실시간 AI 보안.
- [Invariant Labs](https://github.com/invariantlabs-ai/invariant) - AI 에이전트를 위한 보안 테스트 및 시행.
- [Prompt Armor](https://promptarmor.com/) - 프롬프트 인젝션 공격으로부터의 보호.

## 에이전트 네이티브 개발

*에이전트 중심 개발을 위해 처음부터 구축된 도구 및 플랫폼.*

- [E2B](https://github.com/e2b-dev/e2b) - 안전한 샌드박스 환경을 갖춘 AI 에이전트용 오픈소스 런타임.
- [Modal](https://modal.com/) - 에이전트 워크로드 실행에 적합한 서버리스 클라우드 플랫폼.
- [Fly.io](https://fly.io/) - 에이전트 애플리케이션을 전 세계적으로 실행하기 위한 플랫폼.
- [Daytona](https://github.com/daytonaio/daytona) - 에이전트 지원을 갖춘 오픈소스 개발 환경 관리자.
- [Runloop](https://runloop.ai/) - AI 코딩 에이전트를 위해 특별히 구축된 클라우드 인프라.
- [Morph](https://github.com/morphcloud/morph) - AI 에이전트 환경의 생성, 스냅샷, 관리를 위한 클라우드 플랫폼.

## 음성 및 멀티모달 에이전트

*듣고, 보고, 말할 수 있는 에이전트를 구축하기 위한 프레임워크.*

- [Pipecat](https://github.com/pipecat-ai/pipecat) - 음성 및 멀티모달 대화형 AI를 위한 오픈소스 프레임워크.
- [LiveKit Agents](https://github.com/livekit/agents) - 실시간 멀티모달 AI 에이전트 구축 프레임워크.
- [Vocode](https://github.com/vocodedev/vocode-core) - 음성 기반 LLM 에이전트 구축을 위한 오픈소스 라이브러리.
- [Retell AI](https://www.retell.ai/) - 음성 AI 에이전트 구축 및 배포 플랫폼.
- [Vapi](https://vapi.ai/) - 음성 AI 에이전트의 구축, 테스트, 배포를 위한 플랫폼.
- [Bland AI](https://www.bland.ai/) - AI 전화 통화 에이전트 구축을 위한 API.
- [OpenAI Realtime API](https://platform.openai.com/docs/guides/realtime) - 음성 간 상호작용을 위한 저지연 멀티모달 API.

## 에이전트 배포 및 인프라

*프로덕션 환경에서 에이전트를 배포하고 서빙하기 위한 플랫폼 및 도구.*

- [LangServe](https://github.com/langchain-ai/langserve) - LangChain 런너블 및 체인을 REST API로 배포.
- [BentoML](https://github.com/bentoml/BentoML) - ML 모델 및 에이전트의 서빙, 관리, 배포를 위한 프레임워크.
- [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - 온라인 추론 API 구축을 위한 확장 가능한 모델 서빙 라이브러리.
- [LiteLLM](https://github.com/BerriAI/litellm) - OpenAI 형식으로 100개 이상의 LLM API를 호출하기 위한 통합 인터페이스.
- [vLLM](https://github.com/vllm-project/vllm) - LLM을 위한 고처리량 및 메모리 효율적 추론 엔진.
- [Ollama](https://github.com/ollama/ollama) - 간편한 설정으로 LLM을 로컬에서 실행.
- [LM Studio](https://lmstudio.ai/) - OpenAI 호환 API를 갖춘 로컬 LLM 실행 데스크톱 앱.
- [OpenRouter](https://openrouter.ai/) - 여러 LLM 제공업체에 접근하기 위한 통합 API.

## 브라우저 및 웹 에이전트

*웹 브라우저를 탐색하고 상호작용할 수 있는 에이전트.*

- [Browser Use](https://github.com/browser-use/browser-use) - AI 에이전트가 웹사이트에 접근할 수 있게 하는 라이브러리.
- [Playwright MCP](https://github.com/anthropics/anthropic-quickstarts/tree/main/mcp-server-playwright) - Playwright를 통한 브라우저 자동화를 위한 MCP 서버.
- [Stagehand](https://github.com/browserbase/stagehand) - Browserbase의 AI 기반 브라우저 자동화 프레임워크.
- [Skyvern](https://github.com/Skyvern-AI/skyvern) - LLM과 컴퓨터 비전을 사용한 브라우저 기반 워크플로 자동화.
- [LaVague](https://github.com/lavague-ai/LaVague) - 웹 상호작용 자동화를 위한 Large Action Model 프레임워크.
- [Browserbase](https://www.browserbase.com/) - AI 에이전트를 위한 클라우드 브라우저 인프라.
- [MultiOn](https://www.multion.ai/) - 사용자를 대신하여 웹사이트와 상호작용하는 AI 에이전트.
- [WebVoyager](https://github.com/MinorJerry/WebVoyager) - LMM으로 엔드투엔드 웹 에이전트 구축.

## 리서치 에이전트

*연구, 분석, 정보 수집에 특화된 에이전트.*

- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) - 종합적인 온라인 리서치를 위한 자율 에이전트.
- [STORM](https://github.com/stanford-oval/storm) - 연구 논문을 위한 Stanford의 LLM 기반 지식 큐레이션 시스템.
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG) - 연구를 위한 최적의 RAG 파이프라인을 찾는 AutoML 도구.
- [Tavily](https://tavily.com/) - AI 에이전트 및 RAG 애플리케이션에 최적화된 검색 API.
- [Exa](https://exa.ai/) - 임베딩 기반 검색을 갖춘 AI 전용 검색 엔진.
- [Perplexity API](https://docs.perplexity.ai/) - AI 기반 검색 및 리서치를 위한 API.

## 워크플로 및 작업 자동화

*AI 에이전트를 활용한 자동화 워크플로를 구축하기 위한 플랫폼.*

- [n8n](https://github.com/n8n-io/n8n) - AI 에이전트 노드를 갖춘 워크플로 자동화 도구.
- [Langflow](https://github.com/langflow-ai/langflow) - 멀티 에이전트 및 RAG 애플리케이션 구축을 위한 비주얼 프레임워크.
- [Flowise](https://github.com/FlowiseAI/Flowise) - 맞춤형 LLM 흐름을 구축하기 위한 드래그 앤 드롭 UI.
- [Dify](https://github.com/langgenius/dify) - 에이전트 워크플로를 갖춘 AI 네이티브 애플리케이션 구축 플랫폼.
- [Activepieces](https://github.com/activepieces/activepieces) - AI 기능을 갖춘 오픈소스 자동화 도구.
- [Temporal](https://github.com/temporalio/temporal) - 복잡한 에이전트 워크플로에 적합한 내구성 있는 실행 플랫폼.
- [Inngest](https://github.com/inngest/inngest) - 신뢰할 수 있는 AI 워크플로 실행을 위한 이벤트 기반 플랫폼.
- [Prefect](https://github.com/PrefectHQ/prefect) - AI/ML 지원을 갖춘 워크플로 오케스트레이션 프레임워크.

## 에이전트 통신 프로토콜

*에이전트 간 및 에이전트-시스템 간 통신을 위한 표준 및 프로토콜.*

- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) - AI 모델을 데이터 소스 및 도구에 연결하기 위한 Anthropic의 오픈 프로토콜.
- [Agent2Agent (A2A)](https://github.com/google/A2A) - 에이전트 간 통신을 위한 Google의 오픈 프로토콜.
- [Agent Communication Protocol (ACP)](https://github.com/agntcy/acp-spec) - 에이전트 통신을 위한 Cisco의 프로토콜 명세.
- [Agent Network Protocol (ANP)](https://github.com/agent-network-protocol/agent-network-protocol) - 개방형 에이전트 네트워크 구축을 위한 오픈 프로토콜.
- [OpenAPI](https://www.openapis.org/) - 에이전트가 사용할 수 있는 REST API를 정의하기 위한 표준.

## 학습 자료

*AI 에이전트 구축을 위한 튜토리얼, 강좌, 가이드.*

- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) - 에이전트 아키텍처에 대한 Lilian Weng의 종합 블로그 포스트.
- [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) - 실용적인 AI 에이전트 구축에 대한 Anthropic의 가이드.
- [The AI Agent Landscape](https://www.langchain.com/stateofaiagents) - 에이전트 생태계에 대한 LangChain의 종합 개요.
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course) - AI 에이전트 구축에 대한 무료 강좌.
- [DeepLearning.AI Agent Courses](https://www.deeplearning.ai/) - 다양한 프레임워크를 활용한 AI 에이전트 구축에 대한 Andrew Ng의 강좌.
- [AI Agent Infrastructure](https://a16z.com/ai-agent-infrastructure/) - 새롭게 부상하는 AI 에이전트 스택에 대한 a16z의 분석.

## 연구 논문

*AI 에이전트 아키텍처 및 기술에 관한 주요 학술 논문.*

- [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) - LM에서 추론과 행동을 결합하는 기초 논문.
- [Toolformer](https://arxiv.org/abs/2302.04761) - LM이 어떤 도구를 언제, 어떤 인수로 호출할지 결정하도록 학습.
- [Reflexion](https://arxiv.org/abs/2303.11366) - 언어적 강화 학습을 사용하는 언어 에이전트.
- [Generative Agents](https://arxiv.org/abs/2304.03442) - 인간 행동의 인터랙티브 시뮬라크라.
- [Voyager](https://arxiv.org/abs/2305.16291) - LLM을 활용한 개방형 구현 에이전트.
- [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) - LLM에서 추론을 이끌어내는 방법.
- [Tree of Thoughts](https://arxiv.org/abs/2305.10601) - LLM을 활용한 신중한 문제 해결.
- [LATS](https://arxiv.org/abs/2310.04406) - 추론, 행동, 계획을 통합하는 언어 에이전트 트리 탐색.
- [AutoGPT Paper](https://arxiv.org/abs/2306.02224) - 자동 에이전트 시스템의 역량에 대한 종합 연구.

## 커뮤니티

- [r/AI_Agents](https://www.reddit.com/r/AI_Agents/) - AI 에이전트에 초점을 맞춘 Reddit 커뮤니티.
- [LangChain Discord](https://discord.gg/langchain) - LangChain 커뮤니티 Discord 서버.
- [AI Agent Dev Discord](https://discord.gg/aiagents) - AI 에이전트 개발자를 위한 커뮤니티.
- [Hugging Face Forum](https://discuss.huggingface.co/) - ML 및 에이전트에 대한 토론 포럼.

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

## 기여하기

기여를 환영합니다! 먼저 [기여 가이드라인](CONTRIBUTING.md)을 읽어주세요.

## 라이선스

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

법적으로 가능한 범위 내에서 기여자들은 이 저작물에 대한 모든 저작권 및 관련 권리를 포기하였습니다.
