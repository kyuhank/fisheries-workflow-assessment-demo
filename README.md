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

Run through the coordinator in its recorded container, for example:

```sh
make job JOB=assessment_a1
```

Each job receives a named `context`; its entry point is not standalone. See
`jobs/*/README.md` for input connections. The report reads saved results without
refitting, shows the biomass comparison, and retains fit checks and source records.

[SOURCE.json](SOURCE.json) records the calculation library's baseline origin and
SHA-256. The R library and calculation entry points retain those source bytes;
the report and reader guides have been revised for the public-data example.
