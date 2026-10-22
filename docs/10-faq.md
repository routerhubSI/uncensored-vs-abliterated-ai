# Uncensored vs Abliterated FAQ

## What is the difference between uncensored and abliterated?

**Abliterated** is a weight-level technique. **Uncensored** is the broader outcome: a model that refuses less often. A model can be both.

## Which is better?

Neither label wins universally. In the current RouterHub catalogue, uncensored entries are often cheaper. Abliterated entries use a weight-level intervention. Test the exact model ID.

## Why is uncensored cheaper?

Pricing is set per model entry. Several uncensored DeepSeek and GLM entries are cheaper than their abliterated counterparts. Qwen 3.8 Max Uncensored is an exception: it costs more than standard Qwen 3.8 Max.

## Is uncensored as good as abliterated?

It can be, if prompt-level controls and your quality tests pass. Abliterated may be more reliable when refusals happen below the prompt layer, but it can have side effects.

## Does abliterated guarantee no refusals?

No. It reduces the refusal direction; it does not eliminate every refusal.

## Which DeepSeek model should I use?

- Cheapest reduced-refusal option: `deepseek-v4.1-flash-uncensored`.
- Weight-level option: `deepseek-v4.1-flash-abliterated`.
- Pro options: `deepseek-v4-pro-uncensored` and `deepseek-v4-pro-abliterated`; read the catalogue note about the Pro abliterated alias.

## Which GLM model should I use?

Compare `glm-5.3-uncensored`, `glm-5.3-flash-uncensored`, `glm-5.3-abliterated` and `glm-5.3-flash-abliterated`. Flash and uncensored entries are generally cheaper.

## Is there a Qwen abliterated model?

No Qwen abliterated entry appears in the current RouterHub catalogue. Compare `qwen3.8-max` with `qwen3.8-max-uncensored`.

## Can I use one API key for all models?

Yes, RouterHub is a prepaid gateway. Confirm each model’s protocol and availability in the dashboard.

## Can I use these with Claude Code or Cursor?

Use a model entry that supports the protocol the client needs. DeepSeek, GLM and Qwen entries here use Chat Completions; Claude Code generally needs Anthropic Messages.

## How do I evaluate them?

Use normal tasks, previously blocked prompts, tool-use prompts and quality checks. Score refusal and quality separately, then calculate cost per successful task.

## Where can I get support?

Use the [Telegram channel](https://t.me/routerhubsi) for updates and support.

## Next steps

- [What is uncensored vs abliterated?](./01-what-is-uncensored-vs-abliterated.md)
- [How to choose](./02-how-to-choose.md)
- [Pricing](./06-pricing-and-cost.md)
