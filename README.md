# Machine Learning Roadmap — 12-Month Self-Study Curriculum

A structured, project-driven path from Python fundamentals to production-grade LLM systems and multi-agent AI. Each month ends with a capstone project that proves the month's skills were actually learned — not just watched.

**Philosophy:** Progress is measured by the ability to write code and explain concepts without reference material, not by video or chapter completion. Practice immediately after every concept.

---

## Progress Tracker

| Month | Topic | Status |
|-------|-------|--------|
| 1 | Python Foundations | 🟡 In Progress |
| 2 | Data Preprocessing & Feature Engineering | ⬜ Not Started |
| 3 | Software Engineering for ML | ⬜ Not Started |
| 4 | Core Machine Learning | ⬜ Not Started |
| 5 | Ensemble Learning & Advanced ML | ⬜ Not Started |
| 6 | Deep Learning & Neural Networks | ⬜ Not Started |
| 7 | Transformers & Large Language Models | ⬜ Not Started |
| 8 | LLM APIs, Prompting & Context Engineering | ⬜ Not Started |
| 9 | RAG & Vector Databases | ⬜ Not Started |
| 10 | Fine-Tuning & Model Customisation | ⬜ Not Started |
| 11 | AI Agents & Multi-Agent Systems | ⬜ Not Started |
| 12 | MLOps & LLMOps | ⬜ Not Started |

---

## Month 1 — Python Foundations
**Goal:** Write clean, professional Python before touching any ML library.

- **Core Syntax** — variables, operators, type system, strings, f-strings; control flow (if/else, for/while, comprehensions); error handling (try/except, custom exceptions, finally, raise)
- **Data Structures** — lists, dicts, sets, tuples; `collections` (defaultdict, Counter, deque, namedtuple); `itertools`/`functools` (chain, product, partial, reduce)
- **Functions** — *args/**kwargs, closures, decorators, lambda; type hints and mypy; pathlib; re
- **OOP** — classes, inheritance, dunder methods, dataclasses; ABCs, mixins, composition vs inheritance
- **Async & Concurrency** — asyncio basics (async/await, event loop, coroutines); threading vs multiprocessing
- **Tooling** — VS Code, venv/conda, pip, Jupyter; black/ruff/flake8; logging module; file I/O (CSV, JSON, text)

**Project:** CLI data parser that reads messy input files, validates data types, handles errors gracefully, and outputs structured JSON with logging.

---

## Month 2 — Data Preprocessing & Feature Engineering
**Goal:** Take raw, messy data and turn it into a model-ready feature matrix.

- **NumPy** — arrays, vectorised ops, broadcasting, masking, fancy indexing; linear algebra ops (dot, linalg, decompositions)
- **Pandas & Polars** — DataFrames, groupby, merge, pivot, time-series indexing, apply; Polars lazy evaluation and expression API; when to use each
- **Data Cleaning** — missing value imputation (mean, median, KNN, forward fill); outlier detection (IQR, Z-score); duplicates, dtype casting, memory optimisation
- **Feature Engineering** — encoding (one-hot, label, target, frequency); binning, log-transforms, Box-Cox, interaction terms; date/time cyclical encoding, lag features
- **Scaling** — StandardScaler, MinMaxScaler, RobustScaler; scaling leakage and why you fit only on training data
- **EDA Tools** — matplotlib, seaborn, plotly; pandas-profiling / ydata-profiling
- **SQL** — SELECT/WHERE/GROUP BY/HAVING/JOINs; CTEs, subqueries, window functions; PySpark basics
- **Data Validation** — Pandera schema validation; Great Expectations

**Project:** Full preprocessing and validation pipeline on a Kaggle tabular dataset — EDA report, cleaning, feature engineering, and a Pandera schema.

---

## Month 3 — Software Engineering for ML
**Goal:** Write ML code that is testable, reproducible, and production-ready.

- **Git & GitHub** — branching strategies, PRs, rebasing, gitignore for ML repos; pre-commit hooks; conventional commits, semver
- **APIs** — REST fundamentals; requests library, retries with tenacity; Redis basics
- **FastAPI** — routing, Pydantic models, async endpoints, dependency injection; background tasks, middleware, CORS, OpenAPI docs
- **Packaging** — modules, packages, pyproject.toml; Makefile patterns; READMEs and docstrings
- **Testing** — pytest, fixtures, mock, parametrize; testing data transformation functions; coverage with pytest-cov
- **Docker & Infrastructure** — Dockerfile, Docker Compose; Kubernetes awareness (conceptual)
- **Design Patterns for ML** — Factory, Strategy, Repository; hydra/pydantic-settings; separation of concerns

**Project:** A Dockerised, tested FastAPI service that loads a model artifact, validates input with Pydantic, runs inference, and returns structured JSON.

---

## Month 4 — Core Machine Learning
**Goal:** Understand the foundations rigorously — maths, algorithms, and evaluation.

- **Math Foundations** — linear algebra (vectors, matrices, eigenvalues, SVD); calculus (derivatives, chain rule, gradients); probability (Bayes, MLE, MAP); statistics (hypothesis testing, p-values, confidence intervals)
- **Fundamentals** — bias-variance tradeoff; cross-validation (k-fold, stratified, time-series); evaluation metrics (accuracy, precision, recall, F1, ROC-AUC, PR-AUC)
- **Model Calibration** — Platt scaling, isotonic regression, CalibratedClassifierCV; reliability diagrams, ECE
- **Supervised Learning** — linear/logistic regression, regularisation; SVMs; k-NN; Naive Bayes
- **Tree Models** — CART, information gain, Gini impurity, pruning; feature importance
- **Unsupervised Learning** — K-means, DBSCAN, PCA, t-SNE/UMAP
- **Anomaly Detection** — Isolation Forest, LOF, One-Class SVM
- **Bayesian ML (Primer)** — Bayesian vs frequentist; Gaussian Processes; PyMC basics; uncertainty quantification
- **Imbalanced Data** — SMOTE, ADASYN, class weights, threshold moving
- **Scikit-learn Ecosystem** — Pipeline, ColumnTransformer, GridSearchCV/RandomizedSearchCV, joblib
- **A/B Testing Fundamentals** — hypothesis framing, sample size, sequential testing, bandits
- **AI Ethics, Fairness & Bias** *(introduced here, woven throughout the rest of the roadmap)* — sources of bias, fairness metrics, Fairlearn/AI Fairness 360, model cards

**Project:** End-to-end classification pipeline on a healthcare or finance dataset, including calibration analysis, fairness audit, and a written model card.

---

## Month 5 — Ensemble Learning & Advanced ML
**Goal:** Push tabular ML to its performance ceiling and understand why ensembles win.

- **Bagging** — Random Forest, Extra Trees, voting classifiers
- **Boosting** — gradient boosting from scratch; XGBoost, LightGBM, CatBoost
- **Stacking & Blending** — meta-learners, avoiding leakage, calibrating stacked outputs
- **Hyperparameter Tuning** — Optuna, Bayesian optimisation, hyperopt
- **Interpretability** — SHAP, LIME, permutation importance, RFE, mutual information, counterfactual explanations
- **Time Series** — ARIMA/SARIMA/Holt-Winters; feature-based forecasting; N-BEATS, N-HiTS, TFT; MAPE/SMAPE/MASE; statsmodels/prophet/neuralforecast/darts
- **Recommender Systems** — collaborative & content-based filtering, hybrid systems, cold-start; NDCG, MAP, precision@k/recall@k

**Project:** Kaggle-style tabular competition — beat a strong XGBoost baseline with a stacked ensemble, including a SHAP report and Optuna tuning logs.

---

## Month 6 — Deep Learning & Neural Networks
**Goal:** Build, train, and debug neural networks from scratch using PyTorch.

- **PyTorch Fundamentals** — tensors, autograd, Dataset/DataLoader, custom training loops
- **Foundations** — perceptrons, activations (ReLU/GELU/Swish/Sigmoid); backprop and chain rule (derive manually at least once); SGD/momentum/Adam/RMSProp/AdamW
- **Regularisation & Training** — dropout, batch/layer norm, weight decay; gradient clipping; LR scheduling; mixed precision; early stopping
- **CNNs** — convolution/pooling/stride/padding; VGG, ResNet, EfficientNet; transfer learning
- **RNNs, LSTMs & GRUs** — sequence modelling, vanishing gradients, LSTM gates, BPTT
- **Autoencoders & Generative Models** — standard AE, VAE (reparametrisation, KL divergence), GANs (minimax, mode collapse)
- **Graph Neural Networks** — message passing; GCN, GraphSAGE, GAT; PyTorch Geometric
- **Speech & Audio ML** — waveforms, spectrograms, MFCCs; Whisper; TTS overview; librosa
- **Distributed Training** — DataParallel vs DDP; model parallelism (conceptual); gradient checkpointing
- **Experiment Tracking** — Weights & Biases, MLflow
- **Advanced Computer Vision** — object detection (anchors, IoU, NMS); YOLO; segmentation (FCN/DeepLab, Mask R-CNN); Detectron2/Ultralytics

**Project:** Image or audio classifier trained with a full PyTorch training loop, tracked end-to-end with W&B including hyperparameter sweeps.

---

## Month 7 — Transformers & Large Language Models
**Goal:** Understand how modern LLMs work — from attention to architecture to evaluation.

- **Attention Mechanism** — self-attention (Q/K/V), multi-head attention, positional encoding (sinusoidal, RoPE, ALiBi)
- **Transformer Architecture** — encoder-decoder paradigms; BERT vs GPT; pre-norm vs post-norm; Flash Attention; Mixture of Experts
- **Hugging Face Ecosystem** — transformers (AutoModel/AutoTokenizer/pipeline), Model Hub, datasets, accelerate
- **Key Models** — BERT/RoBERTa, GPT-2/3, Llama 2/3/Mistral, Gemma/Phi, Claude/Gemini (awareness)
- **Tokenisation** — BPE, WordPiece, SentencePiece; vocabulary tradeoffs; tokeniser quirks
- **NLP Tasks & Fine-Tuning** — classification, NER, summarisation, QA, translation; Trainer API; task-specific heads
- **Model Evaluation Benchmarks** — MMLU, HumanEval/MBPP, HellaSwag/ARC/TruthfulQA, MT-Bench/Chatbot Arena
- **Multimodal AI & Diffusion Models** — CLIP/BLIP/LLaVA; DDPM theory; Stable Diffusion, ControlNet, LoRA for images; diffusers library

**Project:** Intent classification system using a pre-trained BERT-family transformer, evaluated against benchmark baselines with a confusion matrix and error analysis.

---

## Month 8 — LLM APIs, Prompting & Context Engineering
**Goal:** Build reliable, production-grade applications on top of frontier LLMs.

- **OpenAI API** — chat completions, function calling, vision inputs, streaming, token management
- **Anthropic API** — Messages API, tool use, extended thinking, prompt caching
- **Google Gemini API** — model tiers, long context, multimodal inputs
- **Prompt Engineering** — chain-of-thought, few-shot prompting, role prompting/XML structuring, prompt injection defences
- **Context Engineering** — context window/token budgeting, KV-cache awareness, prompt compression, semantic caching
- **Structured Outputs** — JSON mode, Pydantic + instructor, schema enforcement and retries
- **Guardrails & Safety** — output validation (Guardrails AI, NeMo Guardrails), moderation, fallback/circuit-breaker patterns
- **LLM Evaluation (Prompt-Level)** — systematic A/B testing, LLM-as-judge, promptfoo/braintrust
- **FastAPI + LLM** — streaming endpoints (SSE), retry/rate limiting, multi-model routing

**Project:** Multi-model chat API that classifies incoming prompts by task type and routes to the optimal model, with streaming, structured output, and fallback logic.

---

## Month 9 — RAG & Vector Databases
**Goal:** Build retrieval systems that make LLMs accurate on custom knowledge.

- **Embeddings** — OpenAI text-embedding models, sentence-transformers; similarity metrics; ANN (HNSW, IVF, FAISS)
- **Vector Databases** — Pinecone, Weaviate, Qdrant, pgvector; indexing strategy tradeoffs
- **RAG Pipeline** — document ingestion (PDF/DOCX/HTML/markdown); multimodal ingestion (Unstructured.io, Docling); chunking strategies; metadata filtering; hybrid search (dense + BM25)
- **Frameworks** — LangChain (loaders, retrieval chains, memory, LCEL); LlamaIndex (VectorStoreIndex, query engines, rerankers); dedicated reranking (Cohere Rerank, cross-encoders)
- **Knowledge Graphs as RAG Enhancement** — Neo4j basics, GraphRAG, when to use graph over pure vector
- **Evaluation** — RAGAS (faithfulness, answer relevance, context recall/precision); golden Q&A datasets
- **Advanced RAG** — query rewriting (HyDE, step-back prompting), contextual compression, multi-hop retrieval, agentic RAG

**Project:** Production RAG system for a custom knowledge base (PDFs + web pages) with hybrid search, reranking, a RAGAS evaluation suite, and a FastAPI endpoint.

---

## Month 10 — Fine-Tuning & Model Customisation
**Goal:** Adapt open-source LLMs to specific domains and serve them efficiently.

- **Full Fine-Tuning** — dataset curation, LR schedules, catastrophic forgetting, when it's worth the cost
- **LoRA & QLoRA** — low-rank adapter theory; quantisation (INT8/INT4/NF4); GPTQ, AWQ, GGUF; PEFT library
- **Instruction Tuning & Alignment** — RLHF concepts, DPO, synthetic preference data
- **Synthetic Data for Fine-Tuning** — using frontier models to generate training data; data flywheel; filtering/dedup
- **Model Merging** — SLERP, TIES/DARE, mergekit
- **Fast Fine-Tuning Frameworks** — Unsloth, Axolotl
- **Evaluation** — perplexity, BLEU/ROUGE/BERTScore, MT-Bench, domain-specific evals
- **Serving Fine-Tuned Models** — continuous batching, quantised inference (llama.cpp, Ollama), speculative decoding, vLLM, ONNX
- **RL for ML (Foundations)** — MDPs, Q-learning, policy gradients, actor-critic; RLHF/RLAIF connections

**Project:** Fine-tune a 7B open-weight model on a domain-specific dataset using QLoRA, evaluate with domain evals + MT-Bench, and serve it via a vLLM API endpoint.

---

## Month 11 — AI Agents & Multi-Agent Systems
**Goal:** Build agents that reason, use tools, and collaborate to complete complex tasks.

- **Agent Fundamentals** — ReAct loop, tool calling, memory types (working/episodic/semantic/procedural), long-term memory
- **Tool Design** — reliable tool schemas, error handling in tools, computer use/browser automation, structured output enforcement
- **Frameworks** — LangGraph, AutoGen, CrewAI; state machines vs graph-based orchestration
- **Multi-Agent Systems** — role specialisation, supervisor patterns, parallelism, debate patterns
- **MCP (Model Context Protocol)** — server/client architecture, building an MCP server, MCP vs direct tool calling
- **Agent Cost Management** — token budgeting, loop detection, early stopping, cost-aware routing
- **Safety & Evaluation** — AgentBench/GAIA, guardrails, prompt injection defences, human-in-the-loop, OpenAI Assistants/Responses API

**Project:** Multi-agent research assistant — one planner agent, one web-search agent, one writer agent — coordinated with LangGraph, evaluated on a task benchmark.

---

## Month 12 — MLOps & LLMOps
**Goal:** Deploy, monitor, and maintain ML and LLM systems in production reliably.

- **ML Pipelines** — Prefect, Airflow, ZenML, DVC
- **Feature Stores** — Feast, Tecton; why feature stores matter (training-serving skew)
- **CI/CD for ML** — GitHub Actions, DVC + CI, automated retraining on drift
- **Model Deployment Strategies** — shadow deployment, canary releases, blue/green, A/B testing in production
- **Monitoring** — data drift (EvidentlyAI), concept drift, LLM output monitoring, alerting (PagerDuty/Slack)
- **LLMOps Stack** — LangSmith, Helicone, Langfuse
- **Real-Time ML** — Kafka basics, Flink/Kafka Streams, low-latency serving, online learning
- **Model Compression** — knowledge distillation, pruning, distill vs quantise vs prune decision framework
- **Cloud Deployment** — EC2/GCE, S3/GCS, serverless GPU (Modal/Replicate/RunPod), SageMaker/Vertex AI, autoscaling, Terraform, secrets management, networking, IAM
- **Data Privacy, Compliance & Security** — GDPR for ML, PII handling, differential privacy, federated learning, threat modelling (model inversion, membership inference, adversarial examples)

**Capstone Project:** Deploy a full RAG + multi-agent system to production with a CI/CD pipeline (GitHub Actions + DVC), a monitoring dashboard (Evidently + Langfuse), real-time feature serving, canary deployment, and a public API with rate limiting, auth, and cost tracking.

---

## Structural Themes (Woven Throughout, Not Confined to One Month)

| Theme | Where It Appears |
|-------|-------------------|
| AI Ethics & Fairness | Month 4 (intro) → Month 10 (data) → Month 12 (governance) |
| Data Privacy & Compliance | Month 3 (basics) → Month 12 (production) |
| Interpretability | Month 4 (calibration) → Month 5 (SHAP/LIME) → Month 7 (probing) |
| Cost Awareness | Month 8 (tokens) → Month 11 (agent budgets) → Month 12 (cloud bills) |
| Security | Month 3 (secrets) → Month 8 (injection) → Month 12 (IAM) |
| Evaluation Mindset | Every month — never build without knowing how to measure |

---

## Repo Structure

```
.
├── month-01-python-foundations/
├── month-02-data-preprocessing/
├── month-03-swe-for-ml/
├── month-04-core-ml/
├── month-05-ensemble-learning/
├── month-06-deep-learning/
├── month-07-transformers-llms/
├── month-08-llm-apis-prompting/
├── month-09-rag-vector-db/
├── month-10-fine-tuning/
├── month-11-ai-agents/
├── month-12-mlops-llmops/
└── README.md
```

Each folder contains that month's practice scripts, notebooks, and the capstone project for that month.

---

*Roadmap version: Revised 2025 | Total duration: 12 months | Focus: Industry-ready ML engineer*
