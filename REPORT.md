# Experiment 3: Causal Interventions in Register Generalization

## Research Question

How do internal transformer activations influence predictions
on unfamiliar linguistic-register combinations?

## Model

- Custom 438,272-parameter transformer
- Two transformer layers
- Training seed: 0
- Original project: Register Feature Family

## Method

We selected 12 previously exposed out-of-distribution
examples with incorrect first-token predictions.

For each example, we replaced internal activations with
activations from familiar donor examples.

We compared attention and MLP components across two layers.

Controls included:
- Same-input (sham) interventions
- Donors with different expected first tokens

## Results

| Layer | Component | Mean change | Correct first word |
|---|---|---:|---:|
| 0 | attention | +13.712 | 100% |
| 0 | mlp | +8.399 | 100% |
| 1 | attention | +8.022 | 100% |
| 1 | mlp | +8.540 | 100% |

Sham interventions produced zero change.

Different-target donors generally moved the prediction
margin in the opposite direction.

## Interpretation

Donor-dependent interventions causally influenced
the model's first-token predictions.

However, these results do not establish a specific
mechanism for register-generalization failure.

## Limitations

- Exploratory analysis of 12 selected examples
- Only one trained model seed
- Previously exposed test examples
- Donors selected partly by expected target token
- First-token predictions only
- No identification of individual attention heads or circuits
- No independent replication or confidence intervals

## Conclusion

The experiment demonstrates reproducible intervention
effects in the tested model run.

Further controlled experiments are needed to distinguish
register-specific mechanisms from donor-answer transfer.

## Related Research

https://github.com/Rinetta1981/register-feature-family
