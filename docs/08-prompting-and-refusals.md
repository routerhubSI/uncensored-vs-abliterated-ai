# Prompting and Refusals

Sometimes the cheaper **uncensored** model is enough because the prompt — not the weights — was the problem. Improve the prompt before paying for an abliterated model.

## Use a clear role and task

```text
You are a research assistant helping a developer compare model APIs.
Task: summarize the trade-offs in the provided notes.
Audience: a technical team.
Output: five bullets, then a one-paragraph recommendation.
```

## Give context

A refusal often happens because the model lacks context. Provide:

- the source material;
- the purpose;
- the constraints;
- the expected output;
- what should happen when the request is ambiguous.

## Specify the format

Ask for a table, JSON object, checklist or short answer. Structured output reduces ambiguity and retries.

## Separate refusal from ambiguity

```text
If the request is ambiguous, ask one clarifying question.
If the request is clear and lawful, complete it and state assumptions.
```

## Use a standard fallback

If a model refuses, route to:

1. the standard model;
2. the uncensored entry;
3. the abliterated entry.

Do not jump directly to the most expensive model without testing.

## When prompting is not enough

Use abliterated or a different model when:

- legitimate requests are refused below the prompt layer;
- the model’s tone or safety behavior blocks the workflow;
- your evaluation shows a consistent quality gap.

## Do not use prompts to bypass the law

A prompt does not make illegal activity lawful. Use these models for lawful research, creative work, coding and analysis.

## Next steps

- [How to choose](./02-how-to-choose.md)
- [Safety](./11-safety.md)
- [Evaluation](./07-evaluation.md)
