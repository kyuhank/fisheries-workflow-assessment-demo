# Assessment report (`assessment_report`)

Render the saved assessment comparison as a Quarto report. The report describes the fixed assumptions, convergence and bounds without refitting or claiming confidence intervals.

**Path:** Saved assessment comparison → describe cases and checks → assessment report.

**Inputs:** `runs/assessment_summary/output.json` and the report job's saved run record.

**From:** [Compare assessments (`assessment_summary`)](../assessment_summary/README.md).

**Settings:** No job-specific settings (`{}`).

Biomass is reported as B/K and catches in tonnes. Growth and initial depletion are fixed sensitivity assumptions; convergence does not establish real-stock validity or uncertainty.

Supply this job's saved upstream results in a context JSON, then run from the repository root:

```sh
make run JOB=assessment_report CONTEXT=/absolute/context.json OUT=/absolute/result
```

[run.R](run.R) defines `calculate(context)`; the component adapter loads its local R
library and writes `response.json` with `result` and `effects`. See the
[job guide](../README.md) for context fields, runtime selection and saved-result rendering.

[Saved report](https://kyuhank.github.io/fisheries-workflow-demo/example/assessment_report/report.html) · [Run record](https://kyuhank.github.io/fisheries-workflow-demo/example/assessment_report/record.json)
