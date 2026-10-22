# DeepSeek: Abliterated vs Uncensored

Published RouterHub rates, USD per million tokens, checked **2026-10-27**.

## DeepSeek V4.1 Flash

| | Abliterated | Uncensored | Standard |
|---|---|---|---|
| **Model ID** | `deepseek-v4.1-flash-abliterated` | `deepseek-v4.1-flash-uncensored` | `deepseek-v4.1-flash` |
| **Input** | $0.30 | $0.15 | $0.10 |
| **Output** | $1.25 | $0.60 | $0.40 |
| **Cached input** | $0.055 | $0.0026906 | $0.0026906 |
| **Protocol** | Chat Completions | Chat Completions | Chat Completions |

**What changes:** The abliterated entry uses weight-level modification. The uncensored entry is the cheaper reduced-refusal option in this family.

**Cost:** Uncensored is **2× cheaper on input**, about **2.08× cheaper on output**, and far cheaper on cached input.

**Choose abliterated if:** you need the weight-level variant and can justify the higher price.

**Choose uncensored if:** prompt-level control works and you want the lower-cost reduced-refusal entry.

## DeepSeek V4 Pro

| | Abliterated | Uncensored | Standard |
|---|---|---|---|
| **Model ID** | `deepseek-v4-pro-abliterated` | `deepseek-v4-pro-uncensored` | `deepseek-v4-pro` |
| **Input** | $0.40 | $0.20 | $0.15 |
| **Output** | $1.60 | $0.40 | $0.30 |
| **Cached input** | $0.04 | $0.0016 | $0.0016 |
| **Protocol** | Chat Completions | Chat Completions | Chat Completions |

**Catalogue note:** DeepSeek V4 Pro Abliterated is described by RouterHub as an operator-named Pro alias retaining the **DeepSeek V4.1 Flash abliterated upstream**, not a distinct Pro checkpoint.

**Cost:** Uncensored Pro is **2× cheaper on input** and **4× cheaper on output** than the abliterated Pro entry.

**Choose abliterated if:** you specifically need the listed Pro abliterated alias.

**Choose uncensored if:** you want the cheaper Pro reduced-refusal option.

## Which DeepSeek entry?

- Cheapest reduced-refusal path: `deepseek-v4.1-flash-uncensored`.
- Weight-level Flash path: `deepseek-v4.1-flash-abliterated`.
- Pro naming: compare `deepseek-v4-pro-uncensored` with `deepseek-v4-pro-abliterated`, but read the catalogue note.
- Standard baseline: `deepseek-v4.1-flash` or `deepseek-v4-pro`.

## Next steps

- [GLM comparisons](./04-glm-comparisons.md)
- [Pricing and cost](./06-pricing-and-cost.md)
- [Evaluation](./07-evaluation.md)
