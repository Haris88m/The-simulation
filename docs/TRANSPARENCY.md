# Transparency and Verification

The project is designed so that creators cannot quietly rewrite unsuccessful forecasts or yesterday's state.

## Public records

The research alpha is intended to publish:

- model versions;
- variable definitions;
- evidence-source registry;
- forecast questions and probabilities;
- resolution rules and outcomes;
- calibration and scoring reports;
- event and checkpoint commitments;
- significant model changes and reasons.

## Signed chain

Each accepted event links to the previous event hash. Checkpoints and branch results are signed. A production deployment should also publish daily Merkle roots or equivalent public commitments in more than one independently archived location.

## Reproducibility

A meaningful checkpoint should be reproducible from:

```text
GENESIS STATE
+ MODEL VERSION
+ EVIDENCE EVENT STREAM
+ PLAYER EVENT STREAM
+ RANDOM STREAM IDENTIFIERS
+ CONFIGURATION
```

## Model changes

A model update must not rewrite forecasts created by an earlier model. The old forecast remains attached to its original model version, evidence cutoff, and probability.

## Failure reports

Unexpected outcomes are not hidden. They become calibration evidence and may also produce ARG events asking players to identify what the model failed to represent.
