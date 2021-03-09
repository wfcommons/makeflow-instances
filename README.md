![Build](https://github.com/wfcommons/makeflow-traces/workflows/Build/badge.svg)

<a href="https://wfcommons.org" target="_blank"><img src="https://wfcommons.org/images/wfcommons-horizontal.png" width="350" /></a>

<img src="http://ccl.cse.nd.edu/software/makeflow/MakeflowLogoSmall.png" width=160 />

# Makeflow Workflow Execution Traces

This repository contains workflow execution traces generated from
[Makeflow](http://ccl.cse.nd.edu/software/makeflow/) workflow
executions. The traces hosted in this repository use the
[WfCommons JSON format](https://github.com/wfcommons/workflow-schema)
for describing workflow executions.

#### Repository Structure

Workflow execution traces are organized into sub-folders within this
repository. Each sub-folder represents a _workflow application_, which
itself contains sub-folders for workflow executions in different
_computing platforms_.

#### Workflow Simulator

The execution traces provided in this repository are compatible to any
[simulator framework](https://wfcommons.org/simulators) that
implements the
[WfCommons JSON format](https://github.com/wfcommons/workflow-schema).

## Summary of Workflow Execution Traces

| Application | Science Domain | Category | Computing Platforms | # Execution Traces |
| --- | --- | --- | --- | --- |
| BLAST | Bioinformatics | Compute-intensive | 1 | 15 |
| BWA | Bioinformatics | Data-intensive | 1 | 15 |
