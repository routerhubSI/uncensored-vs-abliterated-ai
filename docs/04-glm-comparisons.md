# GLM: Abliterated vs Uncensored

Published RouterHub rates, USD per million tokens, checked **2026-10-27**.

## GLM 5.3

| | Abliterated | Uncensored | Standard |
|---|---|---|---|
| **Model ID** | `glm-5.3-abliterated` | `glm-5.3-uncensored` | `glm-5.3` |
| **Input** | $0.40 | $0.20 | $0.15 |
| **Output** | $1.33333333 | $0.62857143 | $0.47142857 |
| **Cached input** | $0.16 | $0.11659199 | $0.11659199 |
| **Protocol** | Chat Completions | Chat Completions | Chat Completions |

**Cost:** Uncensored is **half the input price** and about **2.12× cheaper on output**. Cached input is closer, but still lower.

**Choose abliterated if:** you need the weight-level GLM variant.

**Choose uncensored if:** you want the lower-cost reduced-refusal GLM entry and prompt-level controls.

## GLM 5.3 Flash

| | Abliterated | Uncensored | Standard |
|---|---|---|---|
| **Model ID** | `glm-5.3-flash-abliterated` | `glm-5.3-flash-uncensored` | `glm-5.3-flash` |
| **Input** | $0.30 | $0.15 | $0.10 |
| **Output** | $1.00 | $0.50 | $0.33333333 |
| **Cached input** | $0.12 | $0.013453 | $0.013453 |
| **Protocol** | Chat Completions | Chat Completions | Chat Completions |

**Cost:** Uncensored Flash is **half the input price**, **half the output price**, and about **8.9× cheaper on cached input**.

**Choose abliterated if:** weight-level refusal reduction is the requirement.

**Choose uncensored if:** cost and prompt-level control matter more.

## Practical comparison

For many applications, the uncensored GLM entries are the better first test because they are cheaper and the catalogue already separates them by exact ID. Move to abliterated only when the uncensored entry still refuses legitimate requests or when your evaluation shows a quality advantage.

Do not assume “abliterated” means better output quality. Test both on your own tasks.

## Next steps

- [Cross-family comparisons](./05-cross-family-comparisons.md)
- [Pricing and cost](./06-pricing-and-cost.md)
- [Evaluation](./07-evaluation.md)
