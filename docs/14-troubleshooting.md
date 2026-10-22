# Troubleshooting

## `401 Unauthorized`

Missing, revoked or mistyped API key. Re-copy it from the dashboard and confirm the `Authorization: Bearer sk-...` header.

## `404` on every path

Wrong base URL. Copy the exact value shown in the dashboard. Do not add or remove `/v1` unless instructed.

## `404 model_not_found`

The model ID was renamed, retired or typed incorrectly. Copy the current ID from the catalogue. Check:

- `deepseek-v4.1-flash-uncensored`
- `deepseek-v4.1-flash-abliterated`
- `glm-5.3-flash-uncensored`
- `glm-5.3-flash-abliterated`

## `400 Bad Request`

Common causes:

- missing `messages` array;
- invalid role names;
- unsupported field for that entry;
- wrong protocol (Chat vs Messages).

## `429 Too Many Requests`

Rate or balance limit. Check usage and balance, add backoff and reduce concurrency.

```python
import random, time

def backoff(attempt):
    time.sleep(min(30, (2 ** attempt) + random.random()))
```

## Empty or broken response

- Confirm the protocol: DeepSeek/GLM/Qwen entries in this guide use Chat Completions.
- Check whether the model supports streaming or tools.
- Retry with a simple prompt.

## Claude Code ignores the model

Claude Code generally needs an Anthropic Messages-compatible entry. The DeepSeek/GLM/Qwen entries compared here are Chat Completions.

## Model behaves differently than expected

- Confirm the exact model ID.
- Compare uncensored vs abliterated on the same prompts.
- Re-test after catalogue updates.
- Check whether the prompt or the weights are causing the refusal.

## Still stuck?

Collect the request path, status code, error body, model ID, client version and timestamp. Contact [RouterHub support](https://t.me/routerhubsi). Never send your full API key.

## Next steps

- [API quickstart](./09-api-quickstart.md)
- [FAQ](./10-faq.md)
- [Model ID map](./13-model-id-map.md)
