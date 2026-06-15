# Voyage AI (voyage-ai)

Voyage AI builds state-of-the-art embedding and reranker models for retrieval-augmented generation (RAG) and semantic search. The platform exposes an OpenAI-style REST API at api.voyageai.com/v1 for text embeddings, multimodal embeddings, contextualized embeddings, and reranking, with Python and TypeScript SDKs. Model families include voyage-3.x and voyage-4.x text embeddings, voyage-code-3, domain-specialised models (voyage-finance-2, voyage-law-2), voyage-multimodal-3, and the voyage-rerank-2 reranker family. Voyage AI was acquired by MongoDB in February 2024 and is integrated into MongoDB Atlas Vector Search; models are also distributed via AWS Marketplace, Azure Marketplace, and Snowflake.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/voyage-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/voyage-ai/refs/heads/main/apis.yml)

## Tags

- Embeddings
- Rerankers
- RAG
- Semantic Search
- AI Models
- Vector Search
- Multimodal

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### Voyage AI Embeddings API

OpenAI-compatible REST endpoint that returns dense vector embeddings for input text. Supports model selection (voyage-3.5, voyage-3-large, voyage-code-3, voyage-finance-2, voyage-law-2, voyage-4 family), configurable output dimensions (256, 512, 1024, 2048), output dtype (float, int8, uint8, binary, ubinary), input_type hints (query or document), and batch sizes up to 1000 inputs per request.

- **Human URL:** [https://docs.voyageai.com/reference/embeddings-api](https://docs.voyageai.com/reference/embeddings-api)
- **Base URL:** `https://api.voyageai.com/v1`

#### Tags

- Embeddings
- Text
- REST

#### Properties

- [Documentation](https://docs.voyageai.com/reference/embeddings-api)
- [OpenAPI](https://docs.voyageai.com/llms.txt) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Voyage AI Rerank API

Reranking endpoint that scores a list of candidate documents against a query and returns relevance scores. Powered by the voyage-rerank-2 model family, used downstream of vector search to improve retrieval precision in RAG pipelines.

- **Human URL:** [https://docs.voyageai.com/reference/reranker-api](https://docs.voyageai.com/reference/reranker-api)
- **Base URL:** `https://api.voyageai.com/v1`

#### Tags

- Rerank
- Retrieval
- RAG

#### Properties

- [Documentation](https://docs.voyageai.com/reference/reranker-api)

### Voyage AI Multimodal Embeddings API

Multimodal embeddings endpoint backed by voyage-multimodal-3 that accepts interleaved text and images in a single request and returns embeddings in a shared vector space, enabling cross-modal retrieval for documents that mix text, screenshots, charts, and figures.

- **Human URL:** [https://docs.voyageai.com/reference/multimodal-embeddings-api](https://docs.voyageai.com/reference/multimodal-embeddings-api)
- **Base URL:** `https://api.voyageai.com/v1`

#### Tags

- Embeddings
- Multimodal
- Vision

#### Properties

- [Documentation](https://docs.voyageai.com/reference/multimodal-embeddings-api)

### Voyage AI Contextualized Embeddings API

Endpoint that embeds chunks while conditioning on surrounding document context, improving recall for long-document RAG workflows where chunk embeddings would otherwise lose document-level signal.

- **Human URL:** [https://docs.voyageai.com/reference/contextualized-embeddings-api](https://docs.voyageai.com/reference/contextualized-embeddings-api)
- **Base URL:** `https://api.voyageai.com/v1`

#### Tags

- Embeddings
- Contextualized
- RAG

#### Properties

- [Documentation](https://docs.voyageai.com/reference/contextualized-embeddings-api)

### Voyage AI Python SDK

Official Python client (voyageai) wrapping the embeddings, multimodal, contextualized, and reranking endpoints with batching, retries, and async support.

- **Human URL:** [https://github.com/voyage-ai/voyageai-python](https://github.com/voyage-ai/voyageai-python)
- **Base URL:** `https://github.com/voyage-ai/voyageai-python`

#### Tags

- SDK
- Python

#### Properties

- [Repository](https://github.com/voyage-ai/voyageai-python)
- [Package](https://pypi.org/project/voyageai/)

### Voyage AI TypeScript SDK

Official TypeScript / JavaScript client for the Voyage AI REST API.

- **Human URL:** [https://github.com/voyage-ai/typescript-sdk](https://github.com/voyage-ai/typescript-sdk)
- **Base URL:** `https://github.com/voyage-ai/typescript-sdk`

#### Tags

- SDK
- TypeScript
- JavaScript

#### Properties

- [Repository](https://github.com/voyage-ai/typescript-sdk)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/voyage-ai)
- [Website](https://www.voyageai.com/)
- [Documentation](https://docs.voyageai.com/)
- [Git Hub](https://github.com/voyage-ai)
- [Pricing](https://docs.voyageai.com/docs/pricing)
- [Parent](https://www.mongodb.com/)
- [Plans](plans/voyage-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/voyage-ai-rate-limits.yml)
- [Fin Ops](finops/voyage-ai-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
