# Fisheries workflow assessment example

These eight jobs join annual CPUE indices to catches, fit four fixed-growth
Schaefer cases, then compare and report their biomass trajectories. The
[coordinator](https://github.com/kyuhank/fisheries-workflow-demo) loads an exact
source revision and preserves the producing inputs and code bytes.

The current public-data example combines a selected Fiji fleet CPUE index with
South Pacific albacore catches. That local index is not a validated stock-wide
abundance measure. Initial biomass, fixed growth and the simple Schaefer model
are teaching assumptions; case differences are not an uncertainty interval or
stock-management advice.

Run a supplied context with host R (jsonlite), Make and Docker:

```sh
make runtime JOB=assessment_a1
make run JOB=assessment_a1 CONTEXT="$PWD/examples/context.json" OUT=/absolute/new-result
```

The repository's Makefile launches the job in its selected image. Numerical code is
in [R/assessment.R](R/assessment.R) and [jobs/](jobs/README.md). `response.json` contains the
result and declared workflow effects; runtime and execution JSON files identify
the image and software actually used. See the [job guide](jobs/README.md) for
input fields and rendering saved results. The small synthetic example illustrates
the adapter interface; use recorded upstream outputs for an actual workflow.

[SOURCE.json](SOURCE.json) records the calculation library's baseline origin and
SHA-256. The R library and calculation entry points retain those source bytes;
the report and reader guides have been revised for the public-data example.
