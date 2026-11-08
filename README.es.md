<div align="center">

<!-- Título y Badges -->
# Awesome Agent Tools

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/AstreoX/awesome-agent-tools/graphs/commit-activity)

**Una lista curada de frameworks, plataformas, herramientas y recursos para construir, orquestar y desplegar agentes de IA.**

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [Español](README.es.md)

<sub>Los agentes de IA son sistemas autónomos impulsados por LLMs que pueden razonar, planificar, usar herramientas y ejecutar acciones para realizar tareas complejas. <br/>Esta lista rastrea el ecosistema de herramientas para agentes, en rápida evolución.</sub>

**[¿Qué es un agente de IA?](#qué-es-un-agente-de-ia) | [Cómo contribuir](CONTRIBUTING.md)**

</div>

---

## Contenidos

- [Frameworks para agentes](#frameworks-para-agentes)
- [Orquestación multi-agente](#orquestación-multi-agente)
- [Agentes de código](#agentes-de-código)
- [Uso de herramientas y llamadas a funciones](#uso-de-herramientas-y-llamadas-a-funciones)
- [Model Context Protocol (MCP)](#model-context-protocol-mcp)
- [Memoria de agentes](#memoria-de-agentes)
- [RAG para agentes](#rag-para-agentes)
- [Monitoreo y observabilidad de agentes](#monitoreo-y-observabilidad-de-agentes)
- [Evaluación y pruebas de agentes](#evaluación-y-pruebas-de-agentes)
- [Seguridad y barreras de protección para agentes](#seguridad-y-barreras-de-protección-para-agentes)
- [Desarrollo nativo para agentes](#desarrollo-nativo-para-agentes)
- [Agentes de voz y multimodales](#agentes-de-voz-y-multimodales)
- [Despliegue e infraestructura para agentes](#despliegue-e-infraestructura-para-agentes)
- [Agentes web y de navegador](#agentes-web-y-de-navegador)
- [Agentes de investigación](#agentes-de-investigación)
- [Automatización de flujos de trabajo y tareas](#automatización-de-flujos-de-trabajo-y-tareas)
- [Protocolos de comunicación entre agentes](#protocolos-de-comunicación-entre-agentes)
- [Recursos de aprendizaje](#recursos-de-aprendizaje)
- [Artículos de investigación](#artículos-de-investigación)
- [Comunidad](#comunidad)

---

## ¿Qué es un agente de IA?

Un agente de IA es un sistema que utiliza un LLM como su motor central de razonamiento y puede:

- **Razonar** sobre problemas y planificar soluciones
- **Actuar** llamando herramientas, APIs o ejecutando código
- **Observar** los resultados de sus acciones
- **Iterar** hasta completar la tarea

Esto distingue a los agentes de los chatbots simples o las aplicaciones LLM de un solo turno.

---

## Frameworks para agentes

*Frameworks de propósito general para construir agentes de IA.*

- [LangChain](https://github.com/langchain-ai/langchain) - Framework para desarrollar aplicaciones impulsadas por LLMs con cadenas y agentes componibles.
- [LangGraph](https://github.com/langchain-ai/langgraph) - Biblioteca para construir aplicaciones con estado y múltiples actores usando LLMs, basada en LangChain.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Framework para orquestar agentes de IA autónomos con roles asignados.
- [AutoGen](https://github.com/microsoft/autogen) - Framework de Microsoft para construir sistemas conversacionales multi-agente.
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) - SDK de Microsoft para integrar LLMs en aplicaciones con arquitectura de plugins.
- [Haystack](https://github.com/deepset-ai/haystack) - Framework NLP de extremo a extremo con capacidades de agentes y arquitectura basada en pipelines.
- [LlamaIndex](https://github.com/run-llama/llama_index) - Framework de datos para aplicaciones LLM con abstracciones de agentes.
- [Smolagents](https://github.com/huggingface/smolagents) - Biblioteca minimalista de Hugging Face para construir agentes potentes con enfoque en código.
- [PydanticAI](https://github.com/pydantic/pydantic-ai) - Framework de agentes del equipo de Pydantic, usando Pydantic para definiciones de herramientas con tipado seguro.
- [Agno](https://github.com/agno-agi/agno) - Framework ligero para construir agentes multimodales con memoria, conocimiento y herramientas.
- [Atomic Agents](https://github.com/BrainBlend-AI/atomic-agents) - Framework modular para construir sistemas de agentes con componentes atómicos y componibles.
- [Letta](https://github.com/letta-ai/letta) - Framework para construir agentes con estado y memoria a largo plazo (anteriormente MemGPT).
- [Mirascope](https://github.com/Mirascope/mirascope) - Toolkit pythónico para construir agentes impulsados por LLMs con una API simple y elegante.
- [ControlFlow](https://github.com/PrefectHQ/ControlFlow) - Framework de Python para construir flujos de trabajo agénticos por Prefect.
- [Claude Agent SDK](https://github.com/anthropics/claude-code/tree/main/packages/claude-agent-sdk) - SDK oficial de Anthropic para construir agentes personalizados impulsados por Claude.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) - SDK de OpenAI para construir aplicaciones agénticas con transferencias y barreras de protección.
- [Google ADK](https://github.com/google/adk-python) - Kit de desarrollo de agentes de Google para construir agentes de IA.
- [Bee Agent Framework](https://github.com/i-am-bee/bee-agent-framework) - Framework de código abierto de IBM para construir, desplegar y servir agentes.
- [Julep](https://github.com/julep-ai/julep) - Plataforma para construir agentes de IA persistentes con memoria a largo plazo y flujos de trabajo complejos.
- [Eliza](https://github.com/elizaOS/eliza) - Framework de simulación multi-agente para crear personajes de IA autónomos.

## Orquestación multi-agente

*Herramientas para gestionar y coordinar múltiples agentes trabajando juntos.*

- [AutoGen](https://github.com/microsoft/autogen) - Framework conversacional multi-agente que soporta diversos patrones de colaboración.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Orquestación multi-agente basada en roles con flujos de proceso secuenciales y jerárquicos.
- [LangGraph](https://github.com/langchain-ai/langgraph) - Framework multi-agente con estado basado en grafos con ciclos y controlabilidad.
- [OpenAI Swarm](https://github.com/openai/swarm) - Framework educativo que explora la orquestación multi-agente ergonómica y ligera.
- [MetaGPT](https://github.com/geekan/MetaGPT) - Framework multi-agente que asigna diferentes roles a GPTs para formar una entidad de software colaborativa.
- [ChatDev](https://github.com/OpenBMB/ChatDev) - Empresa de software virtual impulsada por múltiples agentes inteligentes en diferentes roles.
- [Camel](https://github.com/camel-ai/camel) - Agentes comunicativos para la exploración de la "Mente" en la sociedad de LLMs.
- [Agency Swarm](https://github.com/VRSEN/agency-swarm) - Framework de código abierto para crear enjambres colaborativos de agentes de IA.
- [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one) - Sistema multi-agente generalista de Microsoft para resolver tareas complejas.
- [Langtrace](https://github.com/Scale3-Labs/langtrace) - Observabilidad de código abierto para aplicaciones LLM multi-agente.

## Agentes de código

*Agentes especializados en tareas de ingeniería de software.*

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) - Herramienta de codificación agéntica de Anthropic que opera directamente en la terminal.
- [Cursor](https://cursor.com/) - Editor de código con IA integrada y capacidades de agente.
- [GitHub Copilot](https://github.com/features/copilot) - Programador par con IA con modo agente para edición multi-archivo y comandos de terminal.
- [Cline](https://github.com/cline/cline) - Agente de codificación autónomo en VS Code que puede crear/editar archivos, ejecutar comandos y usar el navegador.
- [Aider](https://github.com/Aider-AI/aider) - Programación en par con IA en la terminal con integración git.
- [Windsurf](https://codeium.com/windsurf) - IDE agéntico de Codeium con flujos Cascade para codificación en múltiples pasos.
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) - Plataforma para agentes de desarrollo de software autónomos (anteriormente OpenDevin).
- [SWE-agent](https://github.com/princeton-nlp/SWE-agent) - Agente que resuelve autónomamente issues de GitHub usando un LM como cerebro.
- [Devika](https://github.com/stitionai/Devika) - Ingeniera de software con IA agéntica que puede entender, planificar y escribir código.
- [GPT Engineer](https://github.com/gpt-engineer-org/gpt-engineer) - Agente que genera bases de código completas a partir de un solo prompt.
- [Codex CLI](https://github.com/openai/codex) - Agente de codificación ligero de OpenAI que se ejecuta en la terminal.
- [Roo Code](https://github.com/RooVetGit/Roo-Code) - Extensión de agente de codificación con IA para VS Code con soporte multi-modelo.
- [Augment Code](https://www.augmentcode.com/) - Agente de codificación con IA con comprensión profunda del código base.
- [Tabnine](https://www.tabnine.com/) - Asistente de codificación con IA con completado de código similar a un agente.
- [Trae](https://www.trae.ai/) - IDE adaptativo con IA de ByteDance con modo Builder para codificación agéntica.
- [Kilo Code](https://github.com/kilocode-ai/kilocode) - Extensión de código abierto para VS Code que lleva agentes de codificación con IA a tu editor.

## Uso de herramientas y llamadas a funciones

*Bibliotecas y frameworks para permitir que los LLMs usen herramientas y llamen funciones.*

- [LangChain Tools](https://python.langchain.com/docs/modules/agents/tools/) - Extensa colección de herramientas preconstruidas y utilidades para crear herramientas.
- [Composio](https://github.com/ComposioHQ/composio) - Plataforma de integración que proporciona más de 250 herramientas para agentes de IA con autenticación gestionada.
- [Toolhouse](https://toolhouse.ai/) - Infraestructura en la nube para equipar LLMs con acciones y conocimiento.
- [ACI.dev](https://github.com/aipoool/aci) - Plataforma de código abierto que proporciona infraestructura unificada de uso de herramientas para agentes de IA.
- [Arcade AI](https://github.com/ArcadeAI/arcade-ai) - Plataforma de uso de herramientas que facilita agregar herramientas a cualquier LLM.
- [Instructor](https://github.com/jxnl/instructor) - Biblioteca de salida estructurada que hace confiable la llamada a funciones.
- [Outlines](https://github.com/dottxt-ai/outlines) - Generación de texto estructurado para un uso confiable de herramientas.
- [NPI](https://github.com/npi-ai/npi) - Plataforma de API para uso de herramientas que permite a los agentes operar diversas herramientas de software.

## Model Context Protocol (MCP)

*Herramientas y servidores que implementan el Model Context Protocol de Anthropic para integración estandarizada de herramientas.*

- [MCP Specification](https://modelcontextprotocol.io/) - La especificación oficial del Model Context Protocol.
- [MCP Servers](https://github.com/modelcontextprotocol/servers) - Implementaciones de referencia oficiales de servidores MCP.
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - SDK oficial de TypeScript para construir clientes y servidores MCP.
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) - SDK oficial de Python para construir clientes y servidores MCP.
- [MCP Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk) - SDK oficial de Kotlin para construir servidores y clientes MCP en JVM.
- [FastMCP](https://github.com/jlowin/fastmcp) - Forma rápida y pythónica de construir servidores y clientes MCP.
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - Lista curada de implementaciones de servidores MCP.
- [mcp-use](https://github.com/pietrozullo/mcp-use) - Biblioteca de código abierto para conectar cualquier LLM con cualquier servidor MCP.
- [Smithery](https://smithery.ai/) - Registro y marketplace para descubrir y desplegar servidores MCP.
- [Glama](https://glama.ai/mcp/servers) - Plataforma de descubrimiento y directorio de servidores MCP.
- [mcpx](https://github.com/ArcadeAI/mcpx) - Ejecutor de servidores MCP con instalación y ejecución en un solo comando.

## Memoria de agentes

*Sistemas para proporcionar a los agentes memoria a corto y largo plazo.*

- [Mem0](https://github.com/mem0ai/mem0) - Capa de memoria auto-mejorable para aplicaciones LLM.
- [Letta](https://github.com/letta-ai/letta) - Agentes con estado y gestión de memoria a largo plazo (anteriormente MemGPT).
- [Zep](https://github.com/getzep/zep) - Memoria a largo plazo para asistentes de IA con resumen automático.
- [Motorhead](https://github.com/getmetal/motorhead) - Servidor de gestión de memoria y contexto para LLMs.
- [LangMem](https://github.com/langchain-ai/langmem) - SDK de LangChain para memoria a largo plazo en aplicaciones LLM.
- [Cognee](https://github.com/topoteretes/cognee) - Gestión de memoria para agentes de IA usando grafos de conocimiento y almacenes vectoriales.

## RAG para agentes

*Herramientas de generación aumentada por recuperación que mejoran el conocimiento de los agentes.*

- [LlamaIndex](https://github.com/run-llama/llama_index) - Framework de datos para conectar datos personalizados a LLMs con recuperación avanzada.
- [ChromaDB](https://github.com/chroma-core/chroma) - Base de datos de embeddings de código abierto para aplicaciones de IA.
- [Weaviate](https://github.com/weaviate/weaviate) - Base de datos vectorial de código abierto para aplicaciones de IA escalables.
- [Qdrant](https://github.com/qdrant/qdrant) - Motor de búsqueda de similitud vectorial de alto rendimiento.
- [Pinecone](https://www.pinecone.io/) - Base de datos vectorial gestionada para aplicaciones de IA de alto rendimiento.
- [Milvus](https://github.com/milvus-io/milvus) - Base de datos vectorial de código abierto diseñada para búsqueda de similitud escalable.
- [Unstructured](https://github.com/Unstructured-IO/unstructured) - Biblioteca para preprocesar e ingerir documentos para pipelines RAG.
- [R2R](https://github.com/SciPhi-AI/R2R) - Motor RAG listo para producción con capacidades de agentes.
- [RAGFlow](https://github.com/infiniflow/ragflow) - Motor RAG de código abierto basado en comprensión profunda de documentos.
- [LightRAG](https://github.com/HKUDS/LightRAG) - Motor RAG simple y rápido que usa estructuras de grafos para indexación.

## Monitoreo y observabilidad de agentes

*Herramientas para rastrear, depurar y comprender el comportamiento de los agentes.*

- [LangSmith](https://smith.langchain.com/) - Plataforma para depurar, probar, evaluar y monitorear aplicaciones LLM.
- [LangFuse](https://github.com/langfuse/langfuse) - Observabilidad y analíticas de código abierto para aplicaciones LLM.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Observabilidad de código abierto para aplicaciones LLM con trazado y evaluación.
- [Helicone](https://github.com/Helicone/helicone) - Plataforma de observabilidad LLM de código abierto con registro y analíticas.
- [Braintrust](https://github.com/braintrustdata/braintrust-sdk) - Stack de nivel empresarial para construir, entregar y monitorear productos de IA.
- [Weave](https://github.com/wandb/weave) - Toolkit de Weights & Biases para rastrear y evaluar aplicaciones LLM.
- [AgentOps](https://github.com/AgentOps-AI/agentops) - SDK de Python para monitoreo, pruebas y analíticas de repetición de agentes de IA.
- [OpenLLMetry](https://github.com/traceloop/openllmetry) - Observabilidad de código abierto para LLMs basada en OpenTelemetry.
- [Pydantic Logfire](https://github.com/pydantic/logfire) - Plataforma de observabilidad con soporte de primera clase para Pydantic y aplicaciones LLM.

## Evaluación y pruebas de agentes

*Frameworks para evaluar y medir el rendimiento de los agentes.*

- [SWE-bench](https://github.com/princeton-nlp/SWE-bench) - Benchmark para evaluar LMs en problemas reales de ingeniería de software.
- [GAIA](https://huggingface.co/gaia-benchmark) - Benchmark para asistentes de IA generales en tareas del mundo real.
- [AgentBench](https://github.com/THUDM/AgentBench) - Benchmark para evaluar LLMs como agentes en diversos entornos.
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) - Framework para evaluaciones de modelos de lenguaje grandes por UK AISI.
- [RAGAS](https://github.com/explodinggradients/ragas) - Framework de evaluación para pipelines RAG.
- [DeepEval](https://github.com/confident-ai/deepeval) - Framework de evaluación de LLMs con más de 14 métricas.
- [Promptfoo](https://github.com/promptfoo/promptfoo) - Herramienta para probar y evaluar salidas de LLMs.
- [TauBench](https://github.com/sierra-research/tau-bench) - Benchmark para evaluar interacciones herramienta-agente-usuario en dominios del mundo real.
- [Agent-as-a-Judge](https://github.com/metauto-ai/agent-as-a-judge) - Uso de agentes para evaluar las salidas de otros agentes.

## Seguridad y barreras de protección para agentes

*Herramientas para hacer que los agentes sean seguros, protegidos y controlables.*

- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Framework para agregar garantías estructurales, de tipo y de calidad a las salidas de LLMs.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - Toolkit de NVIDIA para agregar barreras de protección programables a aplicaciones basadas en LLMs.
- [LLM Guard](https://github.com/protectai/llm-guard) - Toolkit de seguridad para interacciones con LLMs con escaneo de entrada/salida.
- [Rebuff](https://github.com/protectai/rebuff) - Detector auto-reforzante de inyección de prompts.
- [Lakera Guard](https://www.lakera.ai/) - Seguridad de IA en tiempo real para proteger contra inyección de prompts y fuga de datos.
- [Invariant Labs](https://github.com/invariantlabs-ai/invariant) - Pruebas de seguridad y cumplimiento para agentes de IA.
- [Prompt Armor](https://promptarmor.com/) - Protección contra ataques de inyección de prompts.

## Desarrollo nativo para agentes

*Herramientas y plataformas construidas desde cero para el desarrollo impulsado por agentes.*

- [E2B](https://github.com/e2b-dev/e2b) - Entorno de ejecución de código abierto para agentes de IA con entornos aislados y seguros.
- [Modal](https://modal.com/) - Plataforma en la nube serverless ideal para ejecutar cargas de trabajo de agentes.
- [Fly.io](https://fly.io/) - Plataforma para ejecutar aplicaciones de agentes a nivel global.
- [Daytona](https://github.com/daytonaio/daytona) - Gestor de entornos de desarrollo de código abierto con soporte para agentes.
- [Runloop](https://runloop.ai/) - Infraestructura en la nube diseñada específicamente para agentes de codificación con IA.
- [Morph](https://github.com/morphcloud/morph) - Plataforma en la nube para crear, capturar instantáneas y gestionar entornos de agentes de IA.

## Agentes de voz y multimodales

*Frameworks para construir agentes que pueden escuchar, ver y hablar.*

- [Pipecat](https://github.com/pipecat-ai/pipecat) - Framework de código abierto para IA conversacional de voz y multimodal.
- [LiveKit Agents](https://github.com/livekit/agents) - Framework para construir agentes de IA multimodales en tiempo real.
- [Vocode](https://github.com/vocodedev/vocode-core) - Biblioteca de código abierto para construir agentes LLM basados en voz.
- [Retell AI](https://www.retell.ai/) - Plataforma para construir y desplegar agentes de IA de voz.
- [Vapi](https://vapi.ai/) - Plataforma para construir, probar y desplegar agentes de IA de voz.
- [Bland AI](https://www.bland.ai/) - API para construir agentes de IA para llamadas telefónicas.
- [OpenAI Realtime API](https://platform.openai.com/docs/guides/realtime) - API multimodal de baja latencia para interacciones de voz a voz.

## Despliegue e infraestructura para agentes

*Plataformas y herramientas para desplegar y servir agentes en producción.*

- [LangServe](https://github.com/langchain-ai/langserve) - Despliega runnables y cadenas de LangChain como APIs REST.
- [BentoML](https://github.com/bentoml/BentoML) - Framework para servir, gestionar y desplegar modelos de ML y agentes.
- [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Biblioteca de servicio de modelos escalable para construir APIs de inferencia en línea.
- [LiteLLM](https://github.com/BerriAI/litellm) - Interfaz unificada para llamar a más de 100 APIs de LLMs en formato OpenAI.
- [vLLM](https://github.com/vllm-project/vllm) - Motor de inferencia de alto rendimiento y eficiente en memoria para LLMs.
- [Ollama](https://github.com/ollama/ollama) - Ejecuta LLMs localmente con configuración sencilla.
- [LM Studio](https://lmstudio.ai/) - Aplicación de escritorio para ejecutar LLMs locales con una API compatible con OpenAI.
- [OpenRouter](https://openrouter.ai/) - API unificada para acceder a múltiples proveedores de LLMs.

## Agentes web y de navegador

*Agentes que pueden navegar e interactuar con navegadores web.*

- [Browser Use](https://github.com/browser-use/browser-use) - Biblioteca para hacer sitios web accesibles a agentes de IA.
- [Playwright MCP](https://github.com/anthropics/anthropic-quickstarts/tree/main/mcp-server-playwright) - Servidor MCP para automatización de navegadores a través de Playwright.
- [Stagehand](https://github.com/browserbase/stagehand) - Framework de automatización de navegadores impulsado por IA de Browserbase.
- [Skyvern](https://github.com/Skyvern-AI/skyvern) - Automatiza flujos de trabajo basados en navegador usando LLMs y visión por computadora.
- [LaVague](https://github.com/lavague-ai/LaVague) - Framework de modelos de acción grande para automatizar interacciones web.
- [Browserbase](https://www.browserbase.com/) - Infraestructura de navegadores en la nube para agentes de IA.
- [MultiOn](https://www.multion.ai/) - Agente de IA para interactuar con sitios web en nombre de los usuarios.
- [WebVoyager](https://github.com/MinorJerry/WebVoyager) - Construcción de un agente web de extremo a extremo con LMMs.
- [agent-qa](https://vostride.com) - Pruebas de calidad web y móvil en lenguaje natural con memoria persistente memidex, automejora validada y evidencias de ejecución; [FSL-1.1-ALv2](https://vostride.com/license.md) restringe el uso competitivo, con costes de modelos e infraestructura aparte.

## Agentes de investigación

*Agentes especializados en investigación, análisis y recopilación de información.*

- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) - Agente autónomo para investigación en línea exhaustiva.
- [STORM](https://github.com/stanford-oval/storm) - Sistema de curación de conocimiento impulsado por LLMs de Stanford para artículos de investigación.
- [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG) - Herramienta AutoML para encontrar pipelines RAG óptimos para investigación.
- [Tavily](https://tavily.com/) - API de búsqueda optimizada para agentes de IA y aplicaciones RAG.
- [Exa](https://exa.ai/) - Motor de búsqueda diseñado para IA con búsqueda basada en embeddings.
- [Perplexity API](https://docs.perplexity.ai/) - API para búsqueda e investigación impulsada por IA.

## Automatización de flujos de trabajo y tareas

*Plataformas para construir flujos de trabajo automatizados con agentes de IA.*

- [n8n](https://github.com/n8n-io/n8n) - Herramienta de automatización de flujos de trabajo con nodos de agentes de IA.
- [Langflow](https://github.com/langflow-ai/langflow) - Framework visual para construir aplicaciones multi-agente y RAG.
- [Flowise](https://github.com/FlowiseAI/Flowise) - Interfaz de arrastrar y soltar para construir flujos LLM personalizados.
- [Dify](https://github.com/langgenius/dify) - Plataforma para construir aplicaciones nativas de IA con flujos de trabajo de agentes.
- [Activepieces](https://github.com/activepieces/activepieces) - Herramienta de automatización de código abierto con capacidades de IA.
- [Temporal](https://github.com/temporalio/temporal) - Plataforma de ejecución duradera ideal para flujos de trabajo complejos de agentes.
- [Inngest](https://github.com/inngest/inngest) - Plataforma basada en eventos para ejecutar flujos de trabajo de IA confiables.
- [Prefect](https://github.com/PrefectHQ/prefect) - Framework de orquestación de flujos de trabajo con soporte para IA/ML.

## Protocolos de comunicación entre agentes

*Estándares y protocolos para la comunicación entre agentes y entre agentes y sistemas.*

- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) - Protocolo abierto de Anthropic para conectar modelos de IA con fuentes de datos y herramientas.
- [Agent2Agent (A2A)](https://github.com/google/A2A) - Protocolo abierto de Google para comunicación entre agentes.
- [Agent Communication Protocol (ACP)](https://github.com/agntcy/acp-spec) - Especificación de protocolo de Cisco para comunicación entre agentes.
- [Agent Network Protocol (ANP)](https://github.com/agent-network-protocol/agent-network-protocol) - Protocolo abierto para construir una red abierta de agentes.
- [OpenAPI](https://www.openapis.org/) - Estándar para definir APIs REST que los agentes pueden consumir.

## Recursos de aprendizaje

*Tutoriales, cursos y guías para construir agentes de IA.*

- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) - Publicación exhaustiva de Lilian Weng sobre arquitecturas de agentes.
- [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) - Guía de Anthropic para construir agentes de IA prácticos.
- [The AI Agent Landscape](https://www.langchain.com/stateofaiagents) - Panorama completo de LangChain sobre el ecosistema de agentes.
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course) - Curso gratuito sobre cómo construir agentes de IA.
- [DeepLearning.AI Agent Courses](https://www.deeplearning.ai/) - Cursos de Andrew Ng sobre construcción de agentes de IA con diversos frameworks.
- [AI Agent Infrastructure](https://a16z.com/ai-agent-infrastructure/) - Análisis de a16z sobre la emergente pila de infraestructura para agentes de IA.

## Artículos de investigación

*Artículos académicos clave sobre arquitecturas y técnicas de agentes de IA.*

- [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) - Artículo fundacional sobre la combinación de razonamiento y acción en LMs.
- [Toolformer](https://arxiv.org/abs/2302.04761) - Entrenamiento de LMs para decidir qué herramientas llamar, cuándo y con qué argumentos.
- [Reflexion](https://arxiv.org/abs/2303.11366) - Agentes lingüísticos con aprendizaje por refuerzo verbal.
- [Generative Agents](https://arxiv.org/abs/2304.03442) - Simulaciones interactivas de comportamiento humano.
- [Voyager](https://arxiv.org/abs/2305.16291) - Agente incorporado de mundo abierto con LLMs.
- [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) - Provocando razonamiento en LLMs.
- [Tree of Thoughts](https://arxiv.org/abs/2305.10601) - Resolución deliberada de problemas con LLMs.
- [LATS](https://arxiv.org/abs/2310.04406) - Búsqueda en árbol de agentes lingüísticos que unifica razonamiento, acción y planificación.
- [AutoGPT Paper](https://arxiv.org/abs/2306.02224) - Estudio exhaustivo sobre las capacidades de los sistemas de auto-agentes.

## Comunidad

- [r/AI_Agents](https://www.reddit.com/r/AI_Agents/) - Comunidad de Reddit enfocada en agentes de IA.
- [LangChain Discord](https://discord.gg/langchain) - Servidor Discord de la comunidad LangChain.
- [AI Agent Dev Discord](https://discord.gg/aiagents) - Comunidad para desarrolladores de agentes de IA.
- [Hugging Face Forum](https://discuss.huggingface.co/) - Foro de discusión sobre ML y agentes.

---

## Historial de estrellas

<a href="https://star-history.com/#AstreoX/awesome-agent-tools&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date" />
   <img alt="Gráfico de historial de estrellas" src="https://api.star-history.com/svg?repos=AstreoX/awesome-agent-tools&type=Date" />
 </picture>
</a>

---

## Contribuir

¡Las contribuciones son bienvenidas! Lee primero las [directrices de contribución](CONTRIBUTING.md).

## Licencia

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

En la medida de lo posible bajo la ley, los contribuyentes han renunciado a todos los derechos de autor y derechos conexos o vecinos sobre esta obra.
