# Evaluating Uncensored vs Abliterated Models

A model that answers one blocked prompt is not evaluated. Evaluate the exact model ID on your tasks.

## 1. Build a prompt suite

Include:

- normal user requests;
- previously blocked prompts;
- instruction conflicts;
- tool-use or structured-output prompts;
- bilingual prompts if relevant;
- sensitive-but-lawful prompts with a defined policy.

## 2. Score refusal separately from quality

| Dimension | Scale | What it captures |
|---|---|---|
| Refusal | 0 = refused, 1 = partial, 2 = answered | Whether the model engaged |
| Quality | 1–5 | Accuracy, usefulness, style |
| Side effects | 1–5 | Tone, repetition, tool use |
| Cost | tokens + retries | Cost per successful task |

A model can answer and still produce bad output. Both scores matter.

## 3. Pin the exact model ID

Record:

- model ID;
- date tested;
- input/output rates;
- temperature and settings;
- prompt suite version;
- protocol used.

## 4. Compare uncensored and abliterated

Run the same prompts through:

- standard;
- uncensored;
- abliterated.

If uncensored passes your quality and refusal requirements, it may be the better value. If abliterated is materially better on legitimate tasks, pay for it.

## 5. Check side effects

Watch for:

- more blunt or repetitive tone;
- weaker instruction following;
- different tool-call formatting;
- changes in bilingual output;
- reduced quality on normal tasks.

## 6. Re-test after updates

Model behavior and prices change. Keep a regression suite and rerun it when the catalogue changes.

## 7. Document the decision

Write down:

- selected model ID;
- why it beat the alternatives;
- known side effects;
- fallback model;
- review date.

## Next steps

- [Prompting and refusals](./08-prompting-and-refusals.md)
- [Pricing and cost](./06-pricing-and-cost.md)
- [FAQ](./10-faq.md)
