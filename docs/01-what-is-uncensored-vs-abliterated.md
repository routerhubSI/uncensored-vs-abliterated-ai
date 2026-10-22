# What Is Uncensored vs Abliterated?

**Abliterated** and **uncensored** are related labels, but they describe different things.

- **Abliterated AI model** — model weights have been modified to reduce the refusal direction. The intervention is at the model level.
- **Uncensored AI model** — a model that refuses less often. It may be abliterated, fine-tuned, merged or prompt-tuned; “uncensored” describes the outcome, not necessarily the method.

A model can be both. A model can be called uncensored without being abliterated. The exact RouterHub model ID matters more than the label.

## The one-table answer

| Question | Abliterated | Uncensored |
|---|---|---|
| What changes? | Model weights | Model, wrapper or prompt policy |
| What is it? | A technique | A behavior or product category |
| Price pattern on RouterHub | Often higher for the same family | Often lower for the same family |
| Refusal reduction | Weight-level | Depends on the recipe |
| Main risk | Side effects on tone/tools | Unknown recipe; behavior varies |
| How to verify | Test exact model ID | Test exact model ID |

## Why uncensored can be the better value

In the current RouterHub catalogue, several uncensored entries are cheaper than their abliterated counterparts:

- `deepseek-v4.1-flash-uncensored` vs `deepseek-v4.1-flash-abliterated`
- `deepseek-v4-pro-uncensored` vs `deepseek-v4-pro-abliterated`
- `glm-5.3-uncensored` vs `glm-5.3-abliterated`
- `glm-5.3-flash-uncensored` vs `glm-5.3-flash-abliterated`

If a clear system prompt and good context solve the refusal problem, the uncensored entry can deliver the same practical result for less money. That is not a universal rule: Qwen 3.8 Max Uncensored costs more than standard Qwen 3.8 Max, and there is no Qwen abliterated entry in the current catalogue.

## What abliterated does not mean

- It does not guarantee zero refusals.
- It does not guarantee better quality.
- It does not mean the hosted model is a distinct base checkpoint.
- It does not remove your legal or provider obligations.

## What uncensored does not mean

- It does not mean lawless or unrestricted.
- It does not prove which method produced the behavior.
- It does not guarantee stable behavior across model updates.

## Next steps

- [How to choose](./02-how-to-choose.md)
- [Pricing and cost per success](./06-pricing-and-cost.md)
- [Evaluation](./07-evaluation.md)
- [Model ID map](./13-model-id-map.md)
