# Initial experiment protocol

Status: initial plan; implementation has not started.

## Question

Which Bayesian optimization strategies find high-performing candidates with fewer evaluations on a fixed experimental dataset?

## Scope

Start with the Crossed barrel dataset and a small selection of GP and RF configurations from the benchmark paper. Include random search as a comparison, acknowledging that the original study already uses a statistical random baseline.

Use published measurements for retrospective evaluation.

## Basic controls

- Reveal objective values to each model only after it selects the corresponding candidates.
- Fit models and preprocessing using queried observations only.
- Use the same initial candidates and evaluation budget across strategies for each seed.
- Count initial observations toward the budget and avoid repeated queries.
- Record seeds, settings, and any changes from the original method.

## Evaluation

Track the best objective value found versus the number of evaluations. Repeat runs with several seeds to assess variability.

Start with these curves. Add the paper’s acceleration and enhancement metrics after understanding and checking their definitions.



This is a starting plan. It will be refined as implementation clarifies the practical choices and document deviations from the paper.