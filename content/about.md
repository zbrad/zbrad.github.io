---
title: "About"
url: "/about/"
hidemeta: true
---

**Brad Merrill** — Independent AI Researcher · Local LLM Deployment ·
Distributed Systems · GPU Infrastructure. Greater Seattle Area.

Distributed systems fail in unpredictable ways. Every phase of my career has
been about solving that problem in a different domain — transaction
processing, GPU computing, cloud microservices, and now local AI deployment.
The abstractions shift. The core challenge doesn't.

My current research focuses on the practical challenges of local LLM
deployment — model pruning, retrieval-augmented generation (RAG), and building
continuous deployment pipelines for AI systems. I'm actively working with
SGLang for structured LLM generation, FAISS and cuVS for GPU-accelerated vector
search, the NVIDIA NeMo Agent Toolkit for agentic workflows, and Open WebUI for
local model serving. I'm also exploring small language model research and
applying LLMs to structured reasoning tasks. The through-line is the same
question I've been asking my whole career: how do you build systems that are
reliable, efficient, and deployable at scale?

Running large models locally, efficiently, and reliably — with proper
retrieval augmentation, sensible deployment pipelines, and the ability to
update and prune models without disrupting production — is a distributed
systems problem at its core. The tools have changed dramatically. The
fundamental challenges haven't.

## Current work

I maintain builds of the open-source AI stack tuned for NVIDIA GB10 (DGX Spark) and
RTX 40/50-series GPUs, each on a `tuned-builds` branch of my fork, with shared
build tooling in [tuned-common](https://github.com/zbrad/tuned-common):

- **Frameworks and kernels:** [PyTorch](https://github.com/zbrad/pytorch/blob/tuned-builds/tuned/README.md),
  [FlashAttention](https://github.com/zbrad/flash-attention-vllm/tree/tuned-builds/tuned),
  [FlashInfer](https://github.com/zbrad/flashinfer/blob/tuned-builds/tuned/README.md),
  [NCCL](https://github.com/zbrad/nccl/tree/tuned-builds/tuned)
- **Inference and serving:** [vLLM](https://github.com/zbrad/vllm/blob/tuned-builds/tuned/README.md),
  [llama.cpp](https://github.com/zbrad/llama.cpp/blob/tuned-builds/tuned/README.md),
  [Ollama](https://github.com/zbrad/ollama/tree/tuned-builds/tuned),
  [Open WebUI](https://github.com/zbrad/open-webui/tree/tuned-builds)
- **Vector search:** [FAISS](https://github.com/zbrad/faiss/blob/tuned-builds/tuned/README.md),
  [cuVS](https://github.com/zbrad/cuvs/tree/tuned-builds/tuned), [RAFT](https://github.com/zbrad/raft/tree/tuned-builds/tuned)

## Career

- **2024–present · ZBrad LLC** — Independent AI Researcher. Local LLM
  deployment, model pruning, RAG pipelines, and continuous deployment for AI
  systems, including LLMs for chess move generation and evaluation.
- **2016–2024 · NVIDIA** — Senior Software Engineer. Cloud infrastructure
  across GeForce content pipelines, a GPU-as-a-service streaming platform for
  professional 3D/CAD applications, vGPU licensing and utilization, and
  Kubernetes hosting standards on AWS.
- **2012–2015 · Microsoft** — Senior Technical Program Manager / Senior SDE on
  Azure Service Fabric, shaping the developer model for cloud-native
  microservices with internal teams and early-adoption customers.
- **2009–2012 · Clearwire, then Ericsson** — Development and engineering
  manager for network operations systems: embedded Linux at microwave tower
  sites and network-element ETL into a data warehouse.
- **2007–2009 · InfoSpace** — Senior Development Manager for Dogpile.com
  meta-search.
- **2006–2007 · CDigix** — Director of Development: DRM-protected academic
  media and student music streaming.
- **1996–2006 · Microsoft** — Java and .NET evangelist (helping ISVs build
  compilers for the CLR), SDE on ASP.NET, and TPM on Dynamics.
- **1993–1996 · Sybase** — X/Open XA integration with TP monitors, including
  Tuxedo.
- **1980–1993 · Digital Equipment Corporation** — OS internals, compilers, and
  transaction processing: DECintact, DECdtm, and Reliable Transaction Router,
  deployed at NASDAQ, Bank of New York, the Swiss Stock Exchange and Indian
  Railways.

## Publications

- *C# Essentials*
- *C# Design Patterns and VB.Net Design Patterns*

## Recognition

- Microsoft OneWeek Hackathon — First Place, Consumer Category

Find me on [GitHub](https://github.com/zbrad) and
[LinkedIn](https://www.linkedin.com/in/zbrad).
