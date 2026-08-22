# Voyage AI (voyage-ai)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
