# Cross-Family Comparisons

Published RouterHub rates, USD per million tokens, checked **2026-10-27**.

## DeepSeek V4.1 Flash Abliterated vs GLM 5.3 Flash Abliterated

| | DeepSeek | GLM |
|---|---|---|
| **Model ID** | `deepseek-v4.1-flash-abliterated` | `glm-5.3-flash-abliterated` |
| **Input** | $0.30 | $0.30 |
| **Output** | $1.25 | $1.00 |
| **Cached input** | $0.055 | $0.12 |

Same input price. GLM is cheaper on output; DeepSeek is cheaper on cached input. Choose on task quality and cache behavior.

## DeepSeek V4.1 Flash Uncensored vs GLM 5.3 Flash Uncensored

| | DeepSeek | GLM |
|---|---|---|
| **Model ID** | `deepseek-v4.1-flash-uncensored` | `glm-5.3-flash-uncensored` |
| **Input** | $0.15 | $0.15 |
| **Output** | $0.60 | $0.50 |
| **Cached input** | $0.0026906 | $0.013453 |

Same input price. GLM is cheaper on output; DeepSeek is much cheaper on cached input.

## DeepSeek V4.1 Flash Uncensored vs GLM 5.3 Uncensored

| | DeepSeek | GLM |
|---|---|---|
| **Model ID** | `deepseek-v4.1-flash-uncensored` | `glm-5.3-uncensored` |
| **Input** | $0.15 | $0.20 |
| **Output** | $0.60 | $0.62857143 |
| **Cached input** | $0.0026906 | $0.11659199 |

DeepSeek is cheaper on every published rate, with the largest difference on cached input.

## DeepSeek V4 Pro Uncensored vs GLM 5.3 Uncensored

| | DeepSeek V4 Pro | GLM 5.3 |
|---|---|---|
| **Model ID** | `deepseek-v4-pro-uncensored` | `glm-5.3-uncensored` |
| **Input** | $0.20 | $0.20 |
| **Output** | $0.40 | $0.62857143 |
| **Cached input** | $0.0016 | $0.11659199 |

Same input price. DeepSeek is cheaper on output and cached input.

## Qwen 3.8 Max Uncensored

| | Standard | Uncensored |
|---|---|---|
| **Model ID** | `qwen3.8-max` | `qwen3.8-max-uncensored` |
| **Input** | $0.20 | $0.25 |
| **Output** | $0.60 | $0.75 |
| **Cached input** | $0.025 | $0.03125 |

Uncensored Qwen is **25% more expensive** on all three rates. No Qwen abliterated entry appears in the current catalogue.

## What this means

- **Cheapest uncensored comparison:** start with DeepSeek V4.1 Flash Uncensored.
- **Weight-level option:** DeepSeek V4.1 Flash Abliterated or GLM 5.3 Flash Abliterated.
- **Qwen:** compare only standard vs uncensored; there is no abliterated Qwen ID listed.
- **Do not choose on price alone:** test quality, refusals, tool use and protocol support.

## Next steps

- [Pricing and cost](./06-pricing-and-cost.md)
- [Evaluation](./07-evaluation.md)
- [Model ID map](./13-model-id-map.md)
