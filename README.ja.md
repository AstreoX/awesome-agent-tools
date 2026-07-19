<div align="center">

<!-- Title & Badges -->
# Awesome Agent Tools

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/AstreoX/awesome-agent-tools/graphs/commit-activity)

**AIエージェントの構築、オーケストレーション、デプロイのためのフレームワーク、プラットフォーム、ツール、リソースの厳選リスト。**

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [Español](README.es.md)

<sub>AIエージェントとは、LLMを基盤として推論・計画・ツール使用・アクション実行を行い、複雑なタスクを達成する自律型システムです。<br/>このリストは、急速に進化するエージェントツールのエコシステムを追跡しています。</sub>

**[AIエージェントとは？](#aiエージェントとは) | [コントリビュート方法](CONTRIBUTING.md)**

</div>

---

## 目次

- [エージェントフレームワーク](#エージェントフレームワーク)
- [マルチエージェントオーケストレーション](#マルチエージェントオーケストレーション)
- [コードエージェント](#コードエージェント)
- [ツール使用とファンクションコーリング](#ツール使用とファンクションコーリング)
- [Model Context Protocol (MCP)](#model-context-protocol-mcp)
- [エージェントメモリ](#エージェントメモリ)
- [エージェント向けRAG](#エージェント向けrag)
- [エージェントの監視とオブザーバビリティ](#エージェントの監視とオブザーバビリティ)
- [エージェントの評価とテスト](#エージェントの評価とテスト)
- [エージェントのセキュリティとガードレール](#エージェントのセキュリティとガードレール)
- [エージェントネイティブ開発](#エージェントネイティブ開発)
- [音声・マルチモーダルエージェント](#音声マルチモーダルエージェント)
- [エージェントのデプロイとインフラ](#エージェントのデプロイとインフラ)
- [ブラウザ・Webエージェント](#ブラウザwebエージェント)
- [リサーチエージェント](#リサーチエージェント)
- [ワークフロー・タスク自動化](#ワークフロータスク自動化)
- [エージェント通信プロトコル](#エージェント通信プロトコル)
- [学習リソース](#学習リソース)
- [研究論文](#研究論文)
- [コミュニティ](#コミュニティ)

---

## AIエージェントとは？

AIエージェントとは、LLMをコア推論エンジンとして使用し、以下の能力を持つシステムです：

- **推論する** - 問題を分析し、解決策を計画する
- **行動する** - ツール、API、コードを実行する
- **観察する** - 行動の結果を確認する
- **反復する** - タスクが完了するまで繰り返す

これにより、エージェントは単純なチャットボットや単発のLLMアプリケーションとは区別されます。

---

## エージェントフレームワーク

*AIエージェント構築のための汎用フレームワーク。*

- [LangChain](https://github.com/langchain-ai/langchain) - コンポーザブルなチェーンとエージェントでLLMを活用したアプリケーション開発フレームワーク。
- [LangGraph](https://github.com/langchain-ai/langgraph) - LangChain上に構築された、ステートフルなマルチアクターLLMアプリケーション構築ライブラリ。
- [CrewAI](https://github.com/crewAIInc/crewAI) - ロールプレイング型自律AIエージェントのオーケストレーションフレームワーク。
- [AutoGen](https://github.com/microsoft/autogen) - Microsoft製のマルチエージェント会話システム構築フレームワーク。
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) - プラグインアーキテクチャでLLMをアプリに統合するMicrosoft製SDK。
- [Haystack](https://github.com/deepset-ai/haystack) - エージェント機能とパイプラインベースアーキテクチャを備えたエンドツーエンドNLPフレームワーク。
- [LlamaIndex](https://github.com/run-llama/llama_index) - エージェント抽象化を備えたLLMアプリケーション向けデータフレームワーク。
- [Smolagents](https://github.com/huggingface/smolagents) - コードファーストのアプローチで強力なエージェントを構築するHugging Face製の軽量ライブラリ。
- [PydanticAI](https://github.com/pydantic/pydantic-ai) - Pydanticチームによる、型安全なツール定義にPydanticを活用するエージェントフレームワーク。
- [Agno](https://github.com/agno-agi/agno) - メモリ、知識、ツールを備えたマルチモーダルエージェント構築のための軽量フレームワーク。
- [Atomic Agents](https://github.com/BrainBlend-AI/atomic-agents) - アトミックでコンポーザブルなコンポーネントによるエージェントシステム構築のモジュラーフレームワーク。
- [Letta](https://github.com/letta-ai/letta) - 長期記憶を持つステートフルエージェント構築フレームワーク（旧MemGPT）。
- [Mirascope](https://github.com/Mirascope/mirascope) - シンプルでエレガントなAPIでLLM搭載エージェントを構築するPython的ツールキット。
- [ControlFlow](https://github.com/PrefectHQ/ControlFlow) - Prefect製のエージェンティックワークフロー構築Pythonフレームワーク。
- [Claude Agent SDK](https://github.com/anthropics/claude-code/tree/main/packages/claude-agent-sdk) - Claudeを活用したカスタムエージェント構築のためのAnthropic公式SDK。
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) - ハンドオフとガードレールを備えたエージェンティックアプリケーション構築のためのOpenAI製SDK。
- [Google ADK](https://github.com/google/adk-python) - AIエージェント構築のためのGoogle製Agent Development Kit。
- [Bee Agent Framework](https://github.com/i-am-bee/bee-agent-framework) - エージェントの構築、デプロイ、サービング向けIBM製オープンソースフレームワーク。
- [Julep](https://github.com/julep-ai/julep) - 長期記憶と複雑なワークフローを持つ永続的AIエージェント構築プラットフォーム。
- [Eliza](https://github.com/elizaOS/eliza) - 自律型AIキャラクター作成のためのマルチエージェントシミュレーションフレームワーク。

## マルチエージェントオーケストレーション

*複数のエージェントの連携を管理・調整するためのツール。*

- [AutoGen](https://github.com/microsoft/autogen) - 多様なコラボレーションパターンをサポートする会話型マルチエージェントフレームワーク。
- [CrewAI](https://github.com/crewAIInc/crewAI) - シーケンシャルおよび階層的プロセスフローを備えたロールベースのマルチエージェントオーケストレーション。
- [LangGraph](https://github.com/langchain-ai/langgraph) - サイクルと制御性を備えたステートフルなマルチエージェントグラフフレームワーク。
- [OpenAI Swarm](https://github.com/openai/swarm) - 人間工学的で軽量なマルチエージェントオーケストレーションを探求する教育用フレームワーク。
- [MetaGPT](https://github.com/geekan/MetaGPT) - 異なる役割をGPTに割り当て、協調的なソフトウェアエンティティを形成するマルチエージェントフレームワーク。
- [ChatDev](https://github.com/OpenBMB/ChatDev) - 異なる役割のインテリジェントエージェントで構成された仮想ソフトウェア企業。
- [Camel](https://github.com/camel-ai/camel) - LLM社会の「マインド」探求のためのコミュニカティブエージェント。
- [Agency Swarm](https://github.com/VRSEN/agency-swarm) - AIエージェントの協調的スウォーム作成のためのオープンソースフレームワーク。
- [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one) - 複雑なタスクを解決するためのMicrosoft製汎用マルチエージェントシステム。
- [Langtrace](https://github.com/Scale3-Labs/langtrace) - マルチエージェントLLMアプリケーション向けオープンソースオブザーバビリティ。

## コードエージェント

*ソフトウェアエンジニアリングタスクに特化したエージェント。*

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) - ターミナル上で直接動作するAnthropic製エージェンティックコーディングツール。
- [Cursor](https://cursor.com/) - エージェント機能を内蔵したAIファーストのコードエディタ。
- [GitHub Copilot](https://github.com/features/copilot) - マルチファイル編集とターミナルコマンドのエージェントモードを備えたAIペアプログラマー。
- [Cline](https://github.com/cline/cline) - VS Code上でファイルの作成・編集、コマンド実行、ブラウザ操作が可能な自律型コーディングエージェント。
- [Aider](https://github.com/Aider-AI/aider) - git統合を備えたターミナルでのAIペアプログラミング。
- [Windsurf](https://codeium.com/windsurf) - マルチステップコーディングのCascadeフローを備えたCodeium製エージェンティックIDE。
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) - 自律型ソフトウェア開発エージェントプラットフォーム（旧OpenDevin）。
- [SWE-agent](https://github.com/princeton-nlp/SWE-agent) - LMを頭脳としてGitHub Issueを自律的に修正するエージェント。
- [Devika](https://github.com/stitionai/Devika) - コードの理解、計画、記述が可能なエージェンティックAIソフトウェアエンジニア。
- [GPT Engineer](https://github.com/gpt-engineer-org/gpt-engineer) - 単一のプロンプトからコードベース全体を生成するエージェント。
- [Codex CLI](https://github.com/openai/codex) - ターミナルで動作するOpenAI製軽量コーディングエージェント。
- [Roo Code](https://github.com/RooVetGit/Roo-Code) - マルチモデル対応のVS Code向けAIコーディングエージェント拡張機能。
- [Augment Code](https://www.augmentcode.com/) - コードベースの深い理解を持つAIコーディングエージェント。
- [Tabnine](https://www.tabnine.com/) - エージェント的なコード補完を備えたAIコーディングアシスタント。
- [Trae](https://www.trae.ai/) - エージェンティックコーディングのBuilderモードを備えたByteDance製アダプティブAI IDE。
- [Kilo Code](https://github.com/kilocode-ai/kilocode) - AIコーディングエージェントをエディタに導入するオープンソースVS Code拡張機能。

## ツール使用とファンクションコーリング

*LLMがツールを使用し、関数を呼び出すためのライブラリとフレームワーク。*

- [LangChain Tools](https://python.langchain.com/docs/modules/agents/tools/) - 豊富なプリビルトツールとツール作成ユーティリティのコレクション。
- [Composio](https://github.com/ComposioHQ/composio) - 管理された認証付きでAIエージェント向け250以上のツールを提供する統合プラットフォーム。
- [Toolhouse](https://toolhouse.ai/) - LLMにアクションと知識を装備するクラウドインフラ。
- [ACI.dev](https://github.com/aipoool/aci) - AIエージェント向け統一ツール使用インフラを提供するオープンソースプラットフォーム。
- [Arcade AI](https://github.com/ArcadeAI/arcade-ai) - 任意のLLMにツールを簡単に追加できるツール使用プラットフォーム。
- [Instructor](https://github.com/jxnl/instructor) - ファンクションコーリングの信頼性を高める構造化出力ライブラリ。
- [Outlines](https://github.com/dottxt-ai/outlines) - 信頼性の高いツール使用のための構造化テキスト生成。
- [NPI](https://github.com/npi-ai/npi) - エージェントが各種ソフトウェアツールを操作できるようにするツール使用APIプラットフォーム。

## Model Context Protocol (MCP)

*標準化されたツール統合のためのAnthropicのModel Context Protocolを実装するツールとサーバー。*

- [MCP Specification](https://modelcontextprotocol.io/) - Model Context Protocolの公式仕様。
- [MCP Servers](https://github.com/modelcontextprotocol/servers) - MCPサーバーの公式リファレンス実装。
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - MCPクライアントとサーバー構築のための公式TypeScript SDK。
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) - MCPクライアントとサーバー構築のための公式Python SDK。
- [MCP Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk) - JVM上でMCPサーバーとクライアントを構築するための公式Kotlin SDK。
- [FastMCP](https://github.com/jlowin/fastmcp) - MCPサーバーとクライアントを高速かつPython的に構築する方法。
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - MCPサーバー実装の厳選リスト。
- [mcp-use](https://github.com/pietrozullo/mcp-use) - 任意のLLMを任意のMCPサーバーに接続するオープンソースライブラリ。
- [Smithery](https://smithery.ai/) - MCPサーバーの発見とデプロイのためのレジストリ・マーケットプレイス。
- [Glama](https://glama.ai/mcp/servers) - MCPサーバーの発見とディレクトリプラットフォーム。
- [mcpx](https://github.com/arcadeai-labs/mcpx) - MCP サーバーの検査と呼び出しを行うコマンドラインクライアント。

## エージェントメモリ

*エージェントに短期・長期記憶を提供するシステム。*

- [Mem0](https://github.com/mem0ai/mem0) - LLMアプリケーション向け自己改善型メモリレイヤー。
- [Letta](https://github.com/letta-ai/letta) - 長期記憶管理を備えたステートフルエージェント（旧MemGPT）。
- [Zep](https://github.com/getzep/zep) - 自動要約機能付きAIアシスタント向け長期記憶。
- [Motorhead](https://github.com/getmetal/motorhead) - LLM向けメモリ・コンテキスト管理サーバー。
- [LangMem](https://github.com/langchain-ai/langmem) - LLMアプリケーションの長期記憶のためのLangChain製SDK。
- [Cognee](https://github.com/topoteretes/cognee) - ナレッジグラフとベクトルストアを使用したAIエージェント向けメモリ管理。

## エージェント向けRAG

*エージェントの知識を強化する検索拡張生成ツール。*

- [LlamaIndex](https://github.com/run-llama/llama_index) - 高度な検索機能でカスタムデータをLLMに接続するデータフレームワーク。
- [ChromaDB](https://github.com/chroma-core/chroma) - AIアプリケーション向けオープンソースエンベディングデータベース。
- [Weaviate](https://github.com/weaviate/weaviate) - スケーラブルなAIアプリケーション向けオープンソースベクトルデータベース。
- [Qdrant](https://github.com/qdrant/qdrant) - 高性能ベクトル類似検索エンジン。
- [Pinecone](https://www.pinecone.io/) - 高性能AIアプリケーション向けマネージドベクトルデータベース。
- [Milvus](https://github.com/milvus-io/milvus) - スケーラブルな類似検索のために構築されたオープンソースベクトルデータベース。
- [Unstructured](https://github.com/Unstructured-IO/unstructured) - RAGパイプライン向けドキュメントの前処理と取り込みライブラリ。
- [R2R](https://github.com/SciPhi-AI/R2R) - エージェント機能を備えた本番対応RAGエンジン。
- [RAGFlow](https://github.com/infiniflow/ragflow) - 深いドキュメント理解に基づくオープンソースRAGエンジン。
- [LightRAG](https://github.com/HKUDS/LightRAG) - グラフ構造を使用したインデックス作成によるシンプルで高速なRAGエンジン。

## エージェントの監視とオブザーバビリティ

*エージェントの動作を追跡、デバッグ、理解するためのツール。*

- [LangSmith](https://smith.langchain.com/) - LLMアプリケーションのデバッグ、テスト、評価、監視プラットフォーム。
- [LangFuse](https://github.com/langfuse/langfuse) - LLMアプリケーション向けオープンソースオブザーバビリティ・分析ツール。
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - トレーシングと評価を備えたLLMアプリケーション向けオープンソースオブザーバビリティ。
- [Helicone](https://github.com/Helicone/helicone) - ログと分析を備えたオープンソースLLMオブザーバビリティプラットフォーム。
- [Braintrust](https://github.com/braintrustdata/braintrust-sdk) - AI製品の構築、出荷、監視のためのエンタープライズグレードスタック。
- [Weave](https://github.com/wandb/weave) - LLMアプリケーションの追跡と評価のためのWeights & Biasesツールキット。
- [AgentOps](https://github.com/AgentOps-AI/agentops) - AIエージェントの監視、テスト、リプレイ分析のためのPython SDK。
- [OpenLLMetry](https://github.com/traceloop/openllmetry) - OpenTelemetryベースのLLM向けオープンソースオブザーバビリティ。
- [Pydantic Logfire](https://github.com/pydantic/logfire) - PydanticとLLMアプリケーションのファーストクラスサポートを備えたオブザーバビリティプラットフォーム。

## エージェントの評価とテスト

*エージェントの性能を評価・ベンチマークするためのフレームワーク。*

- [SWE-bench](https://github.com/princeton-nlp/SWE-bench) - 実世界のソフトウェアエンジニアリング問題でLMを評価するベンチマーク。
- [GAIA](https://huggingface.co/gaia-benchmark) - 実世界のタスクにおける汎用AIアシスタントのベンチマーク。
- [AgentBench](https://github.com/THUDM/AgentBench) - 多様な環境でLLMをエージェントとして評価するベンチマーク。
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) - 英国AISI（AI安全研究所）による大規模言語モデル評価フレームワーク。
- [RAGAS](https://github.com/explodinggradients/ragas) - RAGパイプラインの評価フレームワーク。
- [DeepEval](https://github.com/confident-ai/deepeval) - 14以上のメトリクスを備えたLLM評価フレームワーク。
- [Promptfoo](https://github.com/promptfoo/promptfoo) - LLM出力のテスト・評価ツール。
- [TauBench](https://github.com/sierra-research/tau-bench) - 実世界ドメインにおけるツール-エージェント-ユーザーインタラクション評価ベンチマーク。
- [Agent-as-a-Judge](https://github.com/metauto-ai/agent-as-a-judge) - エージェントを使用してエージェントの出力を評価する手法。

## エージェントのセキュリティとガードレール

*エージェントを安全、セキュア、制御可能にするためのツール。*

- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - LLM出力に構造、型、品質の保証を追加するフレームワーク。
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - LLMベースアプリにプログラマブルなガードレールを追加するNVIDIA製ツールキット。
- [LLM Guard](https://github.com/protectai/llm-guard) - 入出力スキャンを備えたLLMインタラクション向けセキュリティツールキット。
- [Rebuff](https://github.com/protectai/rebuff) - 自己強化型プロンプトインジェクション検出器。
- [Lakera Guard](https://www.lakera.ai/) - プロンプトインジェクションとデータ漏洩から保護するリアルタイムAIセキュリティ。
- [Invariant Labs](https://github.com/invariantlabs-ai/invariant) - AIエージェントのセキュリティテストと施行。
- [Prompt Armor](https://promptarmor.com/) - プロンプトインジェクション攻撃からの防御。

## エージェントネイティブ開発

*エージェント駆動開発のためにゼロから構築されたツールとプラットフォーム。*

- [E2B](https://github.com/e2b-dev/e2b) - セキュアなサンドボックス環境を備えたAIエージェント向けオープンソースランタイム。
- [Modal](https://modal.com/) - エージェントワークロードの実行に最適なサーバーレスクラウドプラットフォーム。
- [Fly.io](https://fly.io/) - エージェントアプリケーションをグローバルに実行するプラットフォーム。
- [Daytona](https://github.com/daytonaio/daytona) - エージェントサポートを備えたオープンソース開発環境マネージャー。
- [Runloop](https://runloop.ai/) - AIコーディングエージェント専用に構築されたクラウドインフラ。
- [Morph](https://github.com/morphcloud/morph) - AIエージェント環境の作成、スナップショット、管理のためのクラウドプラットフォーム。

## 音声・マルチモーダルエージェント

*聞く、見る、話すことができるエージェントを構築するためのフレームワーク。*

- [Pipecat](https://github.com/pipecat-ai/pipecat) - 音声およびマルチモーダル対話AI向けオープンソースフレームワーク。
- [LiveKit Agents](https://github.com/livekit/agents) - リアルタイムマルチモーダルAIエージェント構築フレームワーク。
- [Vocode](https://github.com/vocodedev/vocode-core) - 音声ベースLLMエージェント構築のためのオープンソースライブラリ。
- [Retell AI](https://www.retell.ai/) - 音声AIエージェントの構築・デプロイプラットフォーム。
- [Vapi](https://vapi.ai/) - 音声AIエージェントの構築、テスト、デプロイプラットフォーム。
- [Bland AI](https://www.bland.ai/) - AI電話発信エージェント構築のためのAPI。
- [OpenAI Realtime API](https://platform.openai.com/docs/guides/realtime) - 音声間インタラクションのための低遅延マルチモーダルAPI。

## エージェントのデプロイとインフラ

*本番環境でエージェントをデプロイ・サービングするためのプラットフォームとツール。*

- [LangServe](https://github.com/langchain-ai/langserve) - LangChainランナブルとチェーンをREST APIとしてデプロイ。
- [BentoML](https://github.com/bentoml/BentoML) - MLモデルとエージェントのサービング、管理、デプロイフレームワーク。
- [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - オンライン推論API構築のためのスケーラブルなモデルサービングライブラリ。
- [LiteLLM](https://github.com/BerriAI/litellm) - OpenAIフォーマットで100以上のLLM APIを呼び出す統一インターフェース。
- [vLLM](https://github.com/vllm-project/vllm) - LLM向け高スループット・メモリ効率推論エンジン。
- [Ollama](https://github.com/ollama/ollama) - 簡単なセットアップでLLMをローカル実行。
- [LM Studio](https://lmstudio.ai/) - OpenAI互換APIを備えたローカルLLM実行デスクトップアプリ。
- [OpenRouter](https://openrouter.ai/) - 複数のLLMプロバイダーにアクセスするための統一API。

## ブラウザ・Webエージェント

*Webブラウザをナビゲート・操作できるエージェント。*

- [Browser Use](https://github.com/browser-use/browser-use) - WebサイトをAIエージェントからアクセス可能にするライブラリ。
- [Playwright MCP](https://github.com/anthropics/anthropic-quickstarts/tree/main/mcp-server-playwright) - Playwrightを利用したブラウザ自動化のためのMCPサーバー。
- [Stagehand](https://github.com/browserbase/stagehand) - Browserbase製AI搭載ブラウザ自動化フレームワーク。
- [Skyvern](https://github.com/Skyvern-AI/skyvern) - LLMとコンピュータビジョンを使用したブラウザベースワークフローの自動化。
- [LaVague](https://github.com/lavague-ai/LaVague) - Webインタラクションを自動化するLarge Action Modelフレームワーク。
- [Browserbase](https://www.browserbase.com/) - AIエージェント向けクラウドブラウザインフラ。
- [MultiOn](https://www.multion.ai/) - ユーザーに代わってWebサイトを操作するAIエージェント。
- [WebVoyager](https://github.com/MinorJerry/WebVoyager) - LMMを使用したエンドツーエンドWebエージェントの構築。

## リサーチエージェント

*リサーチ、分析、情報収集に特化したエージェント。*

- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) - 包括的なオンラインリサーチのための自律型エージェント。
- [STORM](https://github.com/stanford-oval/storm) - リサーチ記事のためのStanford製LLM搭載知識キュレーションシステム。
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG) - リサーチに最適なRAGパイプラインを見つけるAutoMLツール。
- [Tavily](https://tavily.com/) - AIエージェントとRAGアプリケーション向けに最適化された検索API。
- [Exa](https://exa.ai/) - エンベディングベースの検索を備えたAI向け検索エンジン。
- [Perplexity API](https://docs.perplexity.ai/) - AI搭載検索・リサーチ向けAPI。

## ワークフロー・タスク自動化

*AIエージェントを使用した自動化ワークフロー構築プラットフォーム。*

- [n8n](https://github.com/n8n-io/n8n) - AIエージェントノードを備えたワークフロー自動化ツール。
- [Langflow](https://github.com/langflow-ai/langflow) - マルチエージェントとRAGアプリケーション構築のためのビジュアルフレームワーク。
- [Flowise](https://github.com/FlowiseAI/Flowise) - カスタマイズされたLLMフローを構築するドラッグ&ドロップUI。
- [Dify](https://github.com/langgenius/dify) - エージェントワークフローを備えたAIネイティブアプリケーション構築プラットフォーム。
- [Activepieces](https://github.com/activepieces/activepieces) - AI機能を備えたオープンソース自動化ツール。
- [Temporal](https://github.com/temporalio/temporal) - 複雑なエージェントワークフローに最適な耐久実行プラットフォーム。
- [Inngest](https://github.com/inngest/inngest) - 信頼性の高いAIワークフロー実行のためのイベント駆動プラットフォーム。
- [Prefect](https://github.com/PrefectHQ/prefect) - AI/MLサポートを備えたワークフローオーケストレーションフレームワーク。

## エージェント通信プロトコル

*エージェント間およびエージェント-システム間通信の標準とプロトコル。*

- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) - AIモデルをデータソースとツールに接続するためのAnthropic製オープンプロトコル。
- [Agent2Agent (A2A)](https://github.com/google/A2A) - エージェント間通信のためのGoogle製オープンプロトコル。
- [Agent Communication Protocol (ACP)](https://github.com/agntcy/acp-spec) - エージェント通信のためのCisco製プロトコル仕様。
- [Agent Network Protocol (ANP)](https://github.com/agent-network-protocol/agent-network-protocol) - オープンなエージェントネットワーク構築のためのオープンプロトコル。
- [OpenAPI](https://www.openapis.org/) - エージェントが利用可能なREST APIを定義するための標準。

## 学習リソース

*AIエージェント構築のためのチュートリアル、コース、ガイド。*

- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) - Lilian Wengによるエージェントアーキテクチャの包括的ブログ記事。
- [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) - 実用的なAIエージェント構築のためのAnthropicのガイド。
- [The AI Agent Landscape](https://www.langchain.com/stateofaiagents) - エージェントエコシステムのLangChainによる包括的概要。
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course) - AIエージェント構築の無料コース。
- [DeepLearning.AI Agent Courses](https://www.deeplearning.ai/) - 様々なフレームワークでAIエージェントを構築するAndrew Ngのコース。
- [AI Agent Infrastructure](https://a16z.com/ai-agent-infrastructure/) - 新興AIエージェントスタックに関するa16zの分析。

## 研究論文

*AIエージェントのアーキテクチャと手法に関する主要な学術論文。*

- [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) - LMにおける推論と行動の統合に関する基礎論文。
- [Toolformer](https://arxiv.org/abs/2302.04761) - どのツールをいつ、どの引数で呼び出すかをLMに学習させる研究。
- [Reflexion](https://arxiv.org/abs/2303.11366) - 言語的強化学習を用いた言語エージェント。
- [Generative Agents](https://arxiv.org/abs/2304.03442) - 人間の行動のインタラクティブシミュラクラ。
- [Voyager](https://arxiv.org/abs/2305.16291) - LLMを用いたオープンエンド型具現化エージェント。
- [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) - LLMにおける推論の引き出し。
- [Tree of Thoughts](https://arxiv.org/abs/2305.10601) - LLMによる熟慮的問題解決。
- [LATS](https://arxiv.org/abs/2310.04406) - 推論、行動、計画を統合する言語エージェントツリーサーチ。
- [AutoGPT Paper](https://arxiv.org/abs/2306.02224) - 自動エージェントシステムの能力に関する包括的研究。

## コミュニティ

- [r/AI_Agents](https://www.reddit.com/r/AI_Agents/) - AIエージェントに特化したRedditコミュニティ。
- [LangChain Discord](https://discord.gg/langchain) - LangChainコミュニティのDiscordサーバー。
- [AI Agent Dev Discord](https://discord.gg/aiagents) - AIエージェント開発者のコミュニティ。
- [Hugging Face Forum](https://discuss.huggingface.co/) - 機械学習とエージェントに関するディスカッションフォーラム。

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

## コントリビュート

コントリビュートを歓迎します！まず[コントリビュートガイドライン](CONTRIBUTING.md)をお読みください。

## ライセンス

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

法律上可能な範囲で、コントリビューターはこの作品に対するすべての著作権および関連する隣接権を放棄しています。
