# How to Choose: Uncensored or Abliterated?

Start with the task, not the label.

## 1. Is the refusal at the prompt layer or the model layer?

Use **uncensored** when:

- a clear system prompt, role and output format solve the interaction;
- cost matters;
- the cheaper uncensored entry passes your quality tests;
- you are willing to test the exact model ID.

Use **abliterated** when:

- the model refuses legitimate requests even with a clean prompt;
- you need a weight-level intervention;
- you can accept possible side effects in tone, tool use or instruction following.

## 2. Compare the exact IDs

Use the model ID, not the family name. Example:

- `deepseek-v4.1-flash-uncensored`
- `deepseek-v4.1-flash-abliterated`
- `glm-5.3-flash-uncensored`
- `glm-5.3-flash-abliterated`

Availability and prices change. Check the [live catalogue](https://routerhub.si/models).

## 3. Compare cost per successful task

A cheap model that fails twice can cost more than a stronger model that succeeds once.

```text
cost_per_success = total cost / successful tasks
```

Include retries, prompt tokens, output tokens and cached input.

## 4. Compare behavior

Test:

- normal tasks;
- previously blocked prompts;
- instruction conflicts;
- tool calls and structured output;
- bilingual prompts if relevant;
- tone and repetition.

## 5. Keep a fallback

If the selected entry is unavailable or behaves badly, use a standard model or another family. Do not hard-code one model ID without a fallback.

## Decision guide

| Situation | Start with |
|---|---|
| Cost-sensitive and prompts behave well | Uncensored |
| Legitimate requests still refused | Abliterated |
| Coding or tool use | Test both; check tool behavior |
| Need exact API ID and price | [Model ID map](./13-model-id-map.md) |
| Need to measure quality | [Evaluation](./07-evaluation.md) |

## Next steps

- [DeepSeek comparisons](./03-deepseek-comparisons.md)
- [GLM comparisons](./04-glm-comparisons.md)
- [Cross-family comparisons](./05-cross-family-comparisons.md)
