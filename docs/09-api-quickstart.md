# API Quickstart

Every model in this comparison is available through RouterHub with one prepaid key. Confirm the exact model ID and supported protocol in the [live catalogue](https://routerhub.si/models).

## 1. Create an account

Go to [routerhub.si](https://routerhub.si/register?next=onboarding&utm_source=github&utm_medium=docs&utm_campaign=uncensored-vs-abliterated-ai), create an account and copy:

- **API key** — starts with `sk-`.
- **Base URL** — the exact value shown in the dashboard.

```bash
export ROUTERHUB_API_KEY="sk-..."
export ROUTERHUB_BASE_URL="https://.../v1"
```

## 2. Choose a model ID

Examples from this comparison:

```text
deepseek-v4.1-flash-uncensored
deepseek-v4.1-flash-abliterated
glm-5.3-flash-uncensored
glm-5.3-flash-abliterated
```

Do not guess an ID. A `404 model_not_found` usually means the ID was renamed or retired.

## 3. OpenAI-compatible request

```python
import os
from openai import OpenAI

client = OpenAI(
    api_key=os.environ["ROUTERHUB_API_KEY"],
    base_url=os.environ["ROUTERHUB_BASE_URL"],
)

response = client.chat.completions.create(
    model="MODEL_ID_FROM_DASHBOARD",
    messages=[
        {"role": "system", "content": "Answer clearly and state assumptions."},
        {"role": "user", "content": "Compare uncensored and abliterated models for my use case."},
    ],
)
print(response.choices[0].message.content)
```

## 4. cURL

```bash
curl "$ROUTERHUB_BASE_URL/chat/completions" \
  -H "Authorization: Bearer $ROUTERHUB_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "MODEL_ID_FROM_DASHBOARD",
    "messages": [
      {"role": "user", "content": "Reply with OK."}
    ]
  }'
```

## 5. Protocol notes

- DeepSeek, GLM and Qwen entries in this catalogue use **Chat Completions**.
- Claude Code and Anthropic SDKs require **Anthropic Messages**-compatible entries.
- Check each model’s protocol before integrating.

## 6. Common first-run issues

| Symptom | Likely cause | Fix |
|---|---|---|
| `401` | Missing or wrong key | Re-copy the key |
| `404` on every path | Wrong base URL | Copy the exact URL |
| `404 model_not_found` | Old model ID | Copy the current catalogue ID |
| `429` | Rate or balance limit | Check usage and balance |
| Empty response | Unsupported protocol | Confirm Chat vs Messages |

## Next steps

- [Pricing and cost](./06-pricing-and-cost.md)
- [FAQ](./10-faq.md)
- [Troubleshooting](./14-troubleshooting.md)
