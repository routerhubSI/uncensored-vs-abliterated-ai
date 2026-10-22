# Glossary

**Abliteration** — A weight-level technique that reduces a model’s refusal direction.

**Abliterated model** — A model whose weights have been modified to reduce refusal behavior.

**Anthropic-compatible** — Uses the Anthropic Messages API shape.

**API gateway** — A service that routes requests to model providers and handles auth, billing and model selection.

**Base URL** — The root URL for API requests. Use the exact value from the RouterHub dashboard.

**Cached input** — Input tokens served from a prompt cache, usually billed at a lower rate.

**Chat Completions** — The OpenAI-style request/response format used by DeepSeek, GLM and Qwen entries here.

**Context window** — The maximum tokens a model can consider in one request. Confirm in the catalogue.

**Model ID** — The exact identifier sent in the `model` field. IDs change when models are renamed or retired.

**OpenAI-compatible** — Uses the OpenAI chat completions shape.

**Pay per token** — Billing based on input, output and cached tokens; no subscription.

**Prompt caching** — Reusing a processed prefix so repeated requests cost less.

**Refusal** — A model’s decision to decline or deflect a request.

**RouterHub** — The prepaid AI API gateway used in this guide.

**Uncensored model** — A model that refuses less often; the method may be abliteration, fine-tuning, merging or prompting.

**Variant** — A specific catalogue entry such as `deepseek-v4.1-flash-uncensored`.

## Related

- [What is uncensored vs abliterated?](./01-what-is-uncensored-vs-abliterated.md)
- [Model ID map](./13-model-id-map.md)
- [FAQ](./10-faq.md)
