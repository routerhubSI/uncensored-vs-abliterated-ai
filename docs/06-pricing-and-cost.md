# Pricing and Cost Per Successful Task

Published RouterHub rates, USD per million tokens, checked **2026-10-27**.

Prices are not the whole decision. A cheaper entry that needs two retries can cost more than a stronger entry that succeeds once.

## Current comparison table

| Model | API ID | Input | Output | Cached input |
|---|---|---:|---:|---:|
| DeepSeek V4.1 Flash | `deepseek-v4.1-flash` | $0.10 | $0.40 | $0.0026906 |
| DeepSeek V4.1 Flash Abliterated | `deepseek-v4.1-flash-abliterated` | $0.30 | $1.25 | $0.055 |
| DeepSeek V4.1 Flash Uncensored | `deepseek-v4.1-flash-uncensored` | $0.15 | $0.60 | $0.0026906 |
| DeepSeek V4 Pro | `deepseek-v4-pro` | $0.15 | $0.30 | $0.0016 |
| DeepSeek V4 Pro Abliterated | `deepseek-v4-pro-abliterated` | $0.40 | $1.60 | $0.04 |
| DeepSeek V4 Pro Uncensored | `deepseek-v4-pro-uncensored` | $0.20 | $0.40 | $0.0016 |
| GLM 5.3 | `glm-5.3` | $0.15 | $0.47142857 | $0.11659199 |
| GLM 5.3 Abliterated | `glm-5.3-abliterated` | $0.40 | $1.33333333 | $0.16 |
| GLM 5.3 Uncensored | `glm-5.3-uncensored` | $0.20 | $0.62857143 | $0.11659199 |
| GLM 5.3 Flash | `glm-5.3-flash` | $0.10 | $0.33333333 | $0.013453 |
| GLM 5.3 Flash Abliterated | `glm-5.3-flash-abliterated` | $0.30 | $1.00 | $0.12 |
| GLM 5.3 Flash Uncensored | `glm-5.3-flash-uncensored` | $0.15 | $0.50 | $0.013453 |
| Qwen 3.8 Max | `qwen3.8-max` | $0.20 | $0.60 | $0.025 |
| Qwen 3.8 Max Uncensored | `qwen3.8-max-uncensored` | $0.25 | $0.75 | $0.03125 |

## Cost formula

```text
cost = input_tokens × input_rate
     + output_tokens × output_rate
     + cached_tokens × cached_rate
```

Use per-million rates consistently.

## Cost per successful task

```text
cost_per_success = total cost / successful tasks
```

Include:

- retries;
- failed attempts;
- prompt tokens;
- output tokens;
- cached input;
- any downstream review time.

## What the prices suggest

- **Uncensored is usually cheaper than abliterated** in the DeepSeek and GLM pairs listed here.
- **Standard entries are usually cheapest** in the same family.
- **Qwen 3.8 Max Uncensored is an exception:** it is 25% more expensive than standard Qwen in this catalogue.
- **Cached input changes the math:** DeepSeek uncensored has a very low cached-input rate, which matters for repeated system prompts and long contexts.

## When paying more can be rational

- The cheaper entry refuses legitimate requests.
- The cheaper entry fails tool calls or structured output.
- The cheaper entry needs more retries.
- A specific weight-level variant has measurably better quality for your task.

## Next steps

- [Evaluation](./07-evaluation.md)
- [Prompting and refusals](./08-prompting-and-refusals.md)
- [Model ID map](./13-model-id-map.md)
