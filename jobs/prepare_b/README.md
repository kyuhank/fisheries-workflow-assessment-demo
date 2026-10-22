# Prepare inputs B (`prepare_b`)

Join CPUE index B to annual catches by year and reject an index year without a matching catch.

**Path:** Index B and annual catches → join by year → assessment inputs B.

**Inputs:** The index `series` in `runs/cpue_b/output.json` and annual `catch` in `runs/extract/output.json`.

**From:** [Extract data (`extract`)](https://github.com/kyuhank/fisheries-workflow-cpue-demo/tree/main/jobs/extract), [CPUE analysis B (`cpue_b`)](https://github.com/kyuhank/fisheries-workflow-cpue-demo/tree/main/jobs/cpue_b).

**Settings:** No job-specific settings (`{}`).

Supply this job's saved upstream results in a context JSON, then run from the repository root:

```sh
make run JOB=prepare_b CONTEXT=/absolute/context.json OUT=/absolute/result
```

[run.R](run.R) defines `calculate(context)`; the component adapter loads its local R
library and writes `response.json` with `result` and `effects`. See the
[job guide](../README.md) for context fields, runtime selection and saved-result rendering.

[Saved report](https://kyuhank.github.io/fisheries-workflow-demo/example/prepare_b/report.html) · [Run record](https://kyuhank.github.io/fisheries-workflow-demo/example/prepare_b/record.json)
