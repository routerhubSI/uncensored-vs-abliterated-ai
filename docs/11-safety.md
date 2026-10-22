# Safety and Responsible Use

Uncensored and abliterated models reduce refusal behavior. They do not remove responsibility.

## Lawful use

Use the models for lawful purposes. A reduced-refusal model is not permission to produce illegal content, infringe rights, harass people, distribute malware or bypass security controls.

## Provider terms

RouterHub and the upstream model providers set their own policies. Using a gateway does not override those terms.

## Evaluate before deploying

Test:

- normal tasks;
- previously blocked prompts;
- instruction conflicts and prompt injection;
- tool use and code generation;
- bilingual output;
- sensitive topics with a defined policy.

Measure refusal, quality, side effects and cost per successful task.

## Guardrails

- Input checks for prohibited content and prompt injection.
- Output checks for policy violations and unsafe code.
- Allowlists for tools and external actions.
- Human approval for irreversible actions.
- Rate limits and budgets.
- Logging for incident review.

## Data and privacy

- Send only data you are allowed to process.
- Avoid secrets and sensitive personal data in prompts.
- Use separate API keys or budgets for projects.
- Check retention and logging practices.

## A practical rule

> Use reduced-refusal models to reduce unnecessary friction, not to remove accountability.

If you cannot explain why a request is lawful and appropriate for your audience, do not send it.

## Next steps

- [Evaluation](./07-evaluation.md)
- [Prompting](./08-prompting-and-refusals.md)
- [FAQ](./10-faq.md)
