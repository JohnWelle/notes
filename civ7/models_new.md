# Models

Models are structured representations of our current understanding of some game mechanic, system, or decision process.

A model should:

- Represent a real game-world problem.
- Produce useful conclusions, predictions, or decisions.
- Be testable against observations from actual gameplay.

Models are intentionally defined using lightweight markdown and supporting assets. No formal schema currently exists. We leverage LLM capabilities to infer meaning rather than using a strict schema. How well this works in practice should be covered bytest cases as well.

## Model Creation Flow

1. Define a use case.
2. Define or reuse taxonomy references if needed.
3. Create the model.
4. Define validation criteria.
5. Test against real game observations.
6. Refine or discard.

## Acceptance Criteria

A model should satisfy at least one:

- Explains a game mechanic.
- Predicts an outcome.
- Assists decision making.
- Reduces repeated analysis effort.

## Related Files

- models_taxonomy.json
- rules.md
- state.md
- decisions.md
