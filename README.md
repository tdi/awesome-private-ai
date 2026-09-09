# Awesome Private AI  [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated list of tools, frameworks, and resources for running, building, and deploying AI **privately** — on-prem, air-gapped, or self-hosted.

Private AI enables you to keep your data, models, and infrastructure **under your control**, avoiding unnecessary exposure to third parties. This list covers inference runtimes, model management, privacy tools, and more.

## **Contents**

- [Awesome Private AI  ](#awesome-private-ai--)
  - [**Contents**](#contents)
  - [Inference Runtimes \& Backends](#inference-runtimes--backends)
  - [Model Management \& Serving](#model-management--serving)
  - [Fine-Tuning \& Adapters](#fine-tuning--adapters)
  - [Quantization \& Compression](#quantization--compression)
  - [Vector Databases \& Embeddings](#vector-databases--embeddings)
  - [Agents \& Orchestration](#agents--orchestration)
  - [VS Code Plugins \& Extensions](#vs-code-plugins--extensions)
  - [Privacy, Security \& Governance](#privacy-security--governance)
  - [Observability \& Evaluation](#observability--evaluation)
  - [Models for Private Deployment](#models-for-private-deployment)
  - [UI \& Interaction Layers](#ui--interaction-layers)
  - [Image \& Video Generation](#image--video-generation)
  - [Speech \& Audio](#speech--audio)
  - [Datasets \& Data Prep](#datasets--data-prep)
  - [Learning Resources \& Research](#learning-resources--research)
  - [AI Routers \& API Aggregators](#ai-routers--api-aggregators)
  - [Contributing](#contributing)
  - [License](#license)

## Inference Runtimes & Backends
> Engines and frameworks to run LLMs, vision, and multimodal models locally.

- [vLLM](https://github.com/vllm-project/vllm) - High-throughput, low-latency inference engine for LLMs.
- [sglang](https://github.com/sgl-project/sglang) - Fast serving engine for LLMs and vision-language models, with RadixAttention prefix caching and a structured generation language.
- [mlx-lm](https://github.com/ml-explore/mlx-lm) - Fast, Apple Silicon-optimized LLM inference engine for running models locally and privately.
- [oMLX](https://github.com/jundot/omlx) - macOS-native MLX inference server with paged SSD KV caching and continuous batching. Serves LLM, VLM, embedding, and reranker models over OpenAI- and Anthropic-compatible endpoints for local coding agents on Apple Silicon.
- [Jan](https://jan.ai/) - Privacy-first, offline AI assistant and LLM runtime for local, secure inference.
- [LM Studio](https://lmstudio.ai/) - Cross-platform desktop app for running local LLMs with an easy-to-use interface.
- [Cherry Studio](https://github.com/CherryHQ/cherry-studio) - Powerful and customizable cross-platform desktop app for LLM inference with built in web search, RAG, MCP support, and a quick assistant hotkey to summon your LLM from anywhere. Supports a wide variety of providers and OpenAI compatible endpoints for local inference.
- [LLM-D](https://llm-d.ai/) - Privacy-first, distributed LLM inference engine for scalable, local deployments.
- [Ollama](https://ollama.com) - Local LLM runner with model packaging. Uses llama.cpp backend to serve cautious model defaults.
- [llama.cpp](https://github.com/ggml-org/llama.cpp) - Portable, CPU/GPU-friendly LLM inference, good for GPU + CPU hybrid inference.
- [ik_llama.cpp](https://github.com/ikawrakow/ik_llama.cpp) - Fork of llama.cpp with bleeding edge feature implementations and quantization improvements.
- [llamafile](https://github.com/Mozilla-Ocho/llamafile) - Distribute and run an entire LLM as a single executable file that works across six operating systems, with no install step.
- [LocalAI](https://github.com/mudler/LocalAI) - Drop-in OpenAI-compatible API for local inference across text, image, audio, and embedding models, with no GPU required.
- [KTransformers](https://github.com/kvcache-ai/ktransformers) - Optimized framework for running very large MoE models on limited hardware via GPU/CPU offloading and kernel injection.
- [MLC LLM](https://github.com/mlc-ai/mlc-llm) - Compiler and runtime that deploys LLMs natively to GPUs, phones, and browsers via machine learning compilation.
- [RamaLama](https://github.com/containers/ramalama) - Runs models as OCI containers, pulling from registries you control — a good fit for air-gapped and enterprise workflows.
- [text-generation-inference](https://github.com/huggingface/text-generation-inference) - Optimized serving stack from Hugging Face.
- [GPT4All](https://gpt4all.io) - Local desktop model runner.
- [exo](https://github.com/exo-explore/exo) - Run your own AI cluster at home with everyday devices. Dynamic model partitioning across multiple devices like iPhones, Macs, and Linux machines.
- [exllama3](https://github.com/turboderp-org/exllamav3) - An optimized quantization and inference library for running LLMs locally on modern consumer-class GPUs. Use TabbyAPI for an API server.
- [tabbyAPI](https://github.com/theroyallab/tabbyAPI) - Official API server for running exllamav2 and exllamav3 models. Aims to be a friendly backend with high customizablity and an idiotmatic OAI compatible API for users.
- [YALS (Yet another llamacpp server)](https://github.com/theroyallab/YALS) - TabbyAPI's sister project, adapted for llama.cpp and GGUF models. Built from the ground up using libllama instead of wrapping llama-server.
- [llama-swap](https://github.com/mostlygeek/llama-swap) - Model swapping for llama.cpp (or any local OpenAPI compatible server).


## Model Management & Serving
> Tools for hosting, scaling, and versioning AI models privately.

- [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Scalable Python model serving.
- [Seldon Core](https://github.com/SeldonIO/seldon-core) - Kubernetes-native model deployment.
- [KServe](https://kserve.github.io/website/) - Serverless model inference on Kubernetes.
- [BentoML](https://www.bentoml.com/) - Model packaging & serving framework.
- [Triton Inference Server](https://github.com/triton-inference-server/server) - NVIDIA's multi-framework inference server, supporting TensorRT, PyTorch, ONNX, and vLLM backends behind one endpoint.
- [Xinference](https://github.com/xorbitsai/inference) - Serve and manage LLM, embedding, rerank, image, and audio models in one self-hosted cluster with an OpenAI-compatible API.
- [vLLM Production Stack](https://github.com/vllm-project/production-stack) - End-to-end stack for deploying vLLM in production, including orchestration, monitoring, autoscaling, and best practices for private LLM serving.
- [OME (Open Model Engine)](https://github.com/sgl-project/ome) - Unified, open-source engine for serving, managing, and scaling LLMs and multimodal models privately. Supports sglang, vLLM, and more.


## Fine-Tuning & Adapters
> Private workflows for adapting models to your needs.

- [LoRA](https://arxiv.org/abs/2106.09685) - Low-rank adaptation technique.
- [PEFT](https://github.com/huggingface/peft) - Parameter-efficient fine-tuning.
- [QLoRA](https://arxiv.org/abs/2305.14314) - Memory-efficient LoRA on quantized models.
- [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) - Unified fine-tuning for 100+ models with a web UI, covering SFT, DPO, PPO, and reward modelling on your own hardware.
- [Unsloth](https://github.com/unslothai/unsloth) - Fine-tune and reinforcement-train LLMs 2x faster with substantially less VRAM, on a single local GPU.
- [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) - YAML-driven post-training framework covering full fine-tunes, LoRA, QLoRA, and multi-GPU sharding.
- [TRL](https://github.com/huggingface/trl) - Hugging Face's library for SFT, DPO, GRPO, and reward-model training on top of transformers.
- [ms-swift](https://github.com/modelscope/ms-swift) - Training and deployment toolkit covering 500+ LLMs and 200+ multimodal models, from PEFT through to quantized export.
- [torchtune](https://github.com/pytorch/torchtune) - Native PyTorch library for fine-tuning and experimenting with LLMs, with readable single-file recipes.


## Quantization & Compression
> Shrink models to fit the hardware you actually own.

- [llm-compressor](https://github.com/vllm-project/llm-compressor) - Apply GPTQ, SmoothQuant, SparseGPT, and FP8/INT4 weight-activation quantization, exporting straight to vLLM.
- [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) - 8-bit and 4-bit quantization primitives that underpin QLoRA and much of the local fine-tuning ecosystem.
- [GPTQModel](https://github.com/ModelCloud/GPTQModel) - Actively maintained GPTQ toolkit for producing and running 4-bit quantized models.


## Vector Databases & Embeddings
> Private semantic search & retrieval-augmented generation.

- [Milvus](https://milvus.io) - Scalable vector database.
- [Qdrant](https://github.com/qdrant/qdrant) - High-performance Vector Database and Vector Search Engine.
- [Weaviate](https://weaviate.io) - Open-source semantic search engine.
- [Chroma](https://www.trychroma.com/) - Local-first vector database.
- [FAISS](https://github.com/facebookresearch/faiss) - Facebook AI Similarity Search.
- [pgvector](https://github.com/pgvector/pgvector) - Vector similarity search inside PostgreSQL, keeping embeddings in the database you already self-host.
- [LanceDB](https://github.com/lancedb/lancedb) - Embedded, serverless vector database that stores vectors and metadata as files on your own disk or object store.
- [text-embeddings-inference](https://github.com/huggingface/text-embeddings-inference) - Fast local serving for embedding and reranker models, so retrieval never leaves your network.


## Agents & Orchestration
> Frameworks for chaining private AI tools & agents.

- [AG2](https://github.com/ag2ai/ag2) - Open-source operating system for agentic AI with native Ollama support for local model deployment and multi-agent collaboration.
- [agentgateway](https://github.com/agentgateway/agentgateway) - Gateway for managing and orchestrating AI agents with support for local deployment.
- [LangChain](https://www.langchain.com/) - Agent and LLM orchestration framework.
- [Langflow](https://github.com/langflow-ai/langflow) - Visual workflow builder for creating and deploying AI-powered agents and workflows with built-in API servers.
- [Haystack](https://haystack.deepset.ai) - End-to-end RAG pipelines.
- [Flowise](https://github.com/FlowiseAI/Flowise) - No-code LangChain UI.
- [LlamaIndex](https://www.llamaindex.ai) - Data framework for LLM apps.
- [MetaGPT](https://github.com/FoundationAgents/MetaGPT) - Multi-agent framework for building collaborative AI systems with role-based agents that can work together on complex tasks.
- [Trae Agent](https://github.com/bytedance/trae-agent) - Privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
- [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) - Open-source, privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
- [Herdr](https://herdr.dev/) - Self-hosted runtime and terminal multiplexer for coding agents. Runs the agent CLIs on your own machine or a box you control, grouping them into workspaces you can detach from and reattach to over SSH.
- [Crush](https://github.com/charmbracelet/crush) - Privacy-first, open-source agentic coding and automation platform for local AI workflows.
- [OpenCode AI](https://opencode.ai/) - Open-source agentic coding platform for private, local, and secure AI-powered development workflows.
- [Orkas](https://github.com/Orkas-AI/Orkas) - Open-source, local-first desktop AI workforce whose Commander coordinates specialist agents through one chat; model calls can use a compatible local endpoint.
- [Goose](https://github.com/block/goose) - Local, extensible agent that runs on your machine and works against any LLM backend, including Ollama and other self-hosted endpoints.
- [Aider](https://github.com/Aider-AI/aider) - Terminal-based pair programming agent that edits code in your local git repo, with support for local models via Ollama and OpenAI-compatible servers.
- [PydanticAI](https://github.com/pydantic/pydantic-ai) - Python agent framework by the Pydantic team, model-agnostic with Ollama support for local deployment.
- [dspy](https://github.com/stanfordnlp/dspy) - Modular, open-source agent framework for building composable, private LLM applications and workflows.
- [CUA](https://github.com/trycua/cua) -  enables AI agents to control full operating systems in virtual containers and deploy them locally or to the cloud.
- [Bytebot](https://github.com/bytebot-ai/bytebot) - A desktop agent is an AI that has its own computer. Unlike browser-only agents or traditional RPA tools, Bytebot comes with a full virtual desktop.
- [MFS](https://github.com/zilliztech/mfs) - Exposes your code, docs, chat (Slack/Gmail/Jira), databases and object stores as one file-like, searchable namespace for agents (`ls`/`cat`/`grep` + semantic search); runs fully local with on-device ONNX embeddings on Milvus, no API key.
- [DeepCode](https://github.com/HKUDS/DeepCode) - Open agentic coding framework that turns papers and specs into working code (Paper2Code, Text2Web, Text2Backend), running against local Ollama or vLLM backends.
- [Skales](https://github.com/skalesapp/skales) - Source-available (BSL 1.1) local-first desktop AI agent that runs fully on-device, offline via Ollama or with 15+ providers; your files never leave your machine, no cloud required.


## VS Code Plugins & Extensions
> Privacy-first, open-source agentic coding plugins and extensions for VS Code and other editors.

- [Roo Code](https://github.com/RooCodeInc/Roo-Code) - Privacy-first, open-source agentic coding platform for secure, local AI development (VS Code extension).
- [cline](https://github.com/cline/cline) - Privacy-first, open-source agentic coding platform for local AI workflows and automation (VS Code extension).
- [Continue](https://github.com/continuedev/continue) - Open-source autocomplete and chat assistant for VS Code and JetBrains, configurable against Ollama, llama.cpp, vLLM, and other local endpoints.
- [Tabby](https://github.com/TabbyML/tabby) - Self-hosted AI coding assistant with its own inference server, offering a private alternative to hosted completion services.


## Privacy, Security & Governance
> Keep AI deployments secure and compliant.

- [BlindAI](https://github.com/mithril-security/blindai) - Confidential AI inference using TEEs.
- [OpenFL](https://github.com/securefederatedai/openfl) - Federated learning framework.
- [Flower](https://flower.dev) - Federated learning at scale.
- [Concrete](https://github.com/zama-ai/concrete) - Fully homomorphic encryption for AI.
- [Presidio](https://github.com/microsoft/presidio) - Detect and de-identify PII in text and images before it ever reaches a model.
- [garak](https://github.com/NVIDIA/garak) - LLM vulnerability scanner that probes local models for prompt injection, jailbreaks, and data leakage.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - Add programmable topical and safety rails to LLM applications, running alongside self-hosted models.
- [LLM Guard](https://github.com/protectai/llm-guard) - Input and output scanning toolkit covering prompt injection, PII, toxicity, and secrets leakage.


## Observability & Evaluation
> Measure and monitor private deployments without shipping traces to a vendor.

- [Langfuse](https://github.com/langfuse/langfuse) - Self-hostable LLM observability, tracing, prompt management, and evaluation.
- [promptfoo](https://github.com/promptfoo/promptfoo) - Local-first evaluation and red-teaming for prompts and models, runnable entirely offline in CI.
- [DeepEval](https://github.com/confident-ai/deepeval) - Unit-testing framework for LLM outputs, with metrics that can run against locally hosted judge models.
- [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) - The standard harness for benchmarking language models, supporting local vLLM and Hugging Face backends.
- [Phoenix](https://github.com/Arize-ai/phoenix) - Self-hosted tracing, evaluation, and experiment tracking for LLM applications.
- [OrcaReplay](https://github.com/Continuum-AI-Corp/OrcaReplay) - Records an agent at the HTTP boundary and serves the recording back, so a run reproduces with the model server switched off; traces are files in the project and nothing is uploaded.


## Models for Private Deployment
> Open-weight models and model libraries you can self-host.

- [LLaMA 3](https://ai.meta.com/llama/) - Meta’s open-weight language model.
- [Mistral 7B](https://mistral.ai/news/announcing-mistral-7b/) - Dense 7B parameter model.
- [Qwen 3](https://qwenlm.github.io/blog/qwen3/) - A wide variety of general and specialized models in both dense and "Mixture of Experts" formats.
- [Kimi K2](https://moonshotai.github.io/Kimi-K2/) - Mixture-of-Experts model with 32 billion activated parameters and 1 trillion total parameters.
- [Phi-4](https://huggingface.co/microsoft/phi-4) - Small, high-quality models from Microsoft.
- [Mixtral](https://mistral.ai/news/mixtral-of-experts/) - Mixture-of-experts model.
- [Falcon](https://falconllm.tii.ae) - Open-source model from TII.
- [Gemma3](https://deepmind.google/models/gemma/gemma-3/) - Open source model from Google. 
- [MLX Community](https://huggingface.co/mlx-community) - Community-driven Hugging Face page for open MLX models, optimized for Apple Silicon and private deployment.
- [Bielik](https://huggingface.co/speakleash) - An open source project that provides data, tools and LLMs for the development of the Polish artificial intelligence landscape


## UI & Interaction Layers
> Self-hosted chat & AI frontends.

- [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) - Open-source ChatGPT clone.
- [LibreChat](https://github.com/danny-avila/LibreChat) - Enhanced web UI for LLMs.
- [AnythingLLM](https://anythingllm.com/) - Full-stack private LLM workspace.
- [Open WebUI](https://github.com/open-webui/open-webui) - Commonly recommended Web UI frontend which features built in search, web scrape, RAG, and optional user authentication.
- [Lobe Chat](https://github.com/lobehub/lobe-chat) - Modern self-hosted chat framework with plugin and multimodal support, deployable in one click against local backends.
- [text-generation-webui](https://github.com/oobabooga/text-generation-webui) - Long-standing Gradio web UI for local text generation, supporting llama.cpp, ExLlama, and transformers backends.
- [SillyTavern](https://github.com/SillyTavern/SillyTavern) - Self-hosted, highly customizable frontend for local models, with extensive character, prompt, and context management.
- [Screenpipe](https://github.com/screenpipe/screenpipe) - 24/7 local screen + microphone recording with OCR, audio transcription, and semantic search. Fully offline with Ollama or any local LLM. MCP server for Claude.


## Image & Video Generation
> Run diffusion and video models on your own GPUs.

- [ComfyUI](https://github.com/comfyanonymous/ComfyUI) - Node-based interface and backend for diffusion models, running image, video, and audio pipelines entirely locally.
- [AUTOMATIC1111 Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) - The most widely deployed self-hosted Stable Diffusion interface, with a large extension ecosystem.
- [InvokeAI](https://github.com/invoke-ai/InvokeAI) - Professional-grade local generative image toolkit with a unified canvas and workflow editor.


## Speech & Audio
> Private speech-to-text and text-to-speech.

- [whisper.cpp](https://github.com/ggml-org/whisper.cpp) - C++ port of OpenAI's Whisper automatic speech recognition model, optimized for local, CPU/GPU inference without internet connectivity.
- [Whisper](https://github.com/openai/whisper) - The original open-weight speech recognition model, runnable fully offline.
- [WhisperX](https://github.com/m-bain/whisperX) - Whisper with word-level timestamps, speaker diarization, and much faster batched transcription.
- [RealtimeSTT](https://github.com/KoljaB/RealtimeSTT) - Low-latency local speech-to-text with voice activity detection, for building private voice interfaces.
- [F5-TTS](https://github.com/SWivid/F5-TTS) - Local text-to-speech with voice cloning from a short reference sample.
- [speaches](https://github.com/speaches-ai/speaches) - Self-hosted OpenAI-compatible server for transcription, translation, and speech generation.


## Datasets & Data Prep
> Create and manage private training corpora.

- [OpenWebText](https://skylion007.github.io/OpenWebTextCorpus/) - Open dataset similar to GPT training data.
- [RedPajama](https://www.together.xyz/blog/redpajama) - Open LLM training dataset.
- [Docling](https://github.com/docling-project/docling) - Parse PDF, DOCX, PPTX, and HTML into structured formats for RAG and training, running entirely on your own hardware.
- [MinerU](https://github.com/opendatalab/MinerU) - High-quality PDF-to-Markdown and JSON extraction, including formulas and tables, for building private corpora.
- [Marker](https://github.com/datalab-to/marker) - Fast, accurate document-to-Markdown conversion across PDFs, images, and office formats.
- [Unstructured](https://github.com/Unstructured-IO/unstructured) - Ingestion and preprocessing library for turning messy documents into model-ready chunks.
- [Label Studio](https://github.com/HumanSignal/label-studio) - Self-hosted data labelling platform for text, image, audio, and video annotation.
- [Argilla](https://github.com/argilla-io/argilla) - Collaborative tool for curating, annotating, and quality-checking datasets for fine-tuning and evaluation.


## Learning Resources & Research
> Guides, papers, and tutorials on private AI.

- [LLMs from Scratch](https://github.com/rasbt/LLMs-from-scratch) - Build a GPT-style model step by step in PyTorch, on your own machine.
- [ML Engineering Open Book](https://github.com/stas00/ml-engineering) - Field-tested notes on training and serving large models: hardware, parallelism, throughput, and debugging.
- [LLM Course](https://github.com/mlabonne/llm-course) - Roadmap and notebooks covering LLM fundamentals, fine-tuning, quantization, and deployment.
- [Smol Course](https://github.com/huggingface/smol-course) - Hugging Face's practical course on aligning and fine-tuning small models that fit on local hardware.


## AI Routers & API Aggregators
> Centralized routers and proxy layers for aggregating, governing, and securing your private AI stack. These tools simplify connections to multiple model servers, optimize LLM routing, and provide observability, security, and compliance.

- [Nexus](https://github.com/grafbase/nexus) - Open-source AI router to aggregate Model Context Protocol (MCP) servers, intelligently route requests to the best LLMs, and provide security, governance, observability, and simplified architecture for private AI deployments. [Blog](https://nexusrouter.com/blog/introducing-nexus-the-open-source-ai-router)
- [Bifrost](https://github.com/maximhq/bifrost) - Self-hosted, open-source AI gateway for multi-provider routing, failover, observability, guardrails, and budget controls.
- [LiteLLM](https://github.com/BerriAI/litellm) - Self-hosted proxy exposing 100+ model backends — including Ollama, vLLM, and any OpenAI-compatible server — behind one API, with keys, budgets, routing, and logging.


## Contributing

Contributions welcome! See [Contributing](CONTRIBUTING.md)


## License

Under CC0-1.0 license. see [LICENSE](LICENSE)
