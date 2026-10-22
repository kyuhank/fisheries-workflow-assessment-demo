# Assessment B1 (`assessment_b1`)

Fit the toy Schaefer model to index B with fixed intrinsic growth r = 0.25 and initial biomass equal to K. RTMB estimates one log(K) parameter; catchability q is profiled.

**Path:** Annual index and catches → fixed-growth Schaefer fit → biomass trajectory.

**Inputs:** Joined index and catch `rows` in `runs/prepare_b/output.json`.

**From:** [Prepare inputs B (`prepare_b`)](https://github.com/kyuhank/fisheries-workflow-assessment-demo/tree/main/jobs/prepare_b).

**Settings:** Fixed `r = 0.25`.

Biomass is reported as B/K and catches in tonnes. Growth and initial depletion are fixed sensitivity assumptions; convergence does not establish real-stock validity or uncertainty.

Supply this job's saved upstream results in a context JSON, then run from the repository root:

```sh
make run JOB=assessment_b1 CONTEXT=/absolute/context.json OUT=/absolute/result
```

[run.R](run.R) defines `calculate(context)`; the component adapter loads its local R
library and writes `response.json` with `result` and `effects`. See the
[job guide](../README.md) for context fields, runtime selection and saved-result rendering.

[Saved report](https://kyuhank.github.io/fisheries-workflow-demo/example/assessment_b1/report.html) · [Run record](https://kyuhank.github.io/fisheries-workflow-demo/example/assessment_b1/record.json)
