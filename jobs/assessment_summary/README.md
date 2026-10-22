# Compare assessments (`assessment_summary`)

Compare the four fixed-growth Schaefer sensitivity cases, their biomass trajectories and fit diagnostics.

**Path:** Four fitted cases → compare trajectories → sensitivity summary.

**Inputs:** The fitted `series`, r, K, convergence and bounds in all four assessment outputs.

**From:** [Assessment A1 (`assessment_a1`)](../assessment_a1/README.md), [Assessment A2 (`assessment_a2`)](../assessment_a2/README.md), [Assessment B1 (`assessment_b1`)](../assessment_b1/README.md), [Assessment B2 (`assessment_b2`)](../assessment_b2/README.md).

**Settings:** No job-specific settings (`{}`).

Biomass is reported as B/K and catches in tonnes. Growth and initial depletion are fixed sensitivity assumptions; convergence does not establish real-stock validity or uncertainty.

Supply this job's saved upstream results in a context JSON, then run from the repository root:

```sh
make run JOB=assessment_summary CONTEXT=/absolute/context.json OUT=/absolute/result
```

[run.R](run.R) defines `calculate(context)`; the component adapter loads its local R
library and writes `response.json` with `result` and `effects`. See the
[job guide](../README.md) for context fields, runtime selection and saved-result rendering.

[Saved report](https://kyuhank.github.io/fisheries-workflow-demo/example/assessment_summary/report.html) · [Run record](https://kyuhank.github.io/fisheries-workflow-demo/example/assessment_summary/record.json)
