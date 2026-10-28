# Experiment 3: Causal Interventions in Register Generalization

## Research Question
How do internal transformer activations influence predictions on unfamiliar linguistic-register combinations?

## Method
We performed activation-patching experiments on a custom 438,272-parameter transformer, examining attention and MLP components across two layers.

## Key Findings
- Tested 12 unfamiliar examples.
- Same-target donor interventions corrected the first predicted word in all 12 examples.
- Sham interventions produced no change.
- Different-target donors generally shifted predictions in the opposite direction.

## Scientific Significance
The results demonstrate donor-dependent causal effects on model predictions.

However, they do not yet establish a register-specific mechanism or identify a neural circuit.

## Limitations
This exploratory investigation uses one model seed, previously exposed examples, and first-token predictions only.

## Relationship to Existing Research
This experiment extends the Register Feature Family project by introducing mechanistic interpretability methods to investigate register-generalization failures.

## Parent Research Project

This exploratory mechanistic investigation builds on:

**[Register Is a Feature Family, Not a Dial?](https://github.com/Rinetta1981/register-feature-family)**

The original study identified failures in generalizing linguistic-register combinations. This follow-up investigates how interventions on internal activations affect model predictions.

The findings are exploratory and do not constitute confirmatory evidence of register-specific internal mechanisms.
