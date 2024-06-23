**THIS REPOSITORY HAS BEEN ARCHIVED**

Please, see the new instances using [WfFormat](https://github.com/wfcommons/WfFormat) in the new [WfInstances](https://github.com/wfcommons/WfInstances) repository.

---

![Build](https://github.com/wfcommons/makeflow-instances/workflows/Build/badge.svg)
[![DOI](https://zenodo.org/badge/324824708.svg)](https://zenodo.org/badge/latestdoi/324824708)

<a href="https://wfcommons.org" target="_blank"><img src="https://wfcommons.org/images/wfcommons-horizontal.png" width="350" /></a>

<img src="http://ccl.cse.nd.edu/software/makeflow/MakeflowLogoSmall.png" width=160 />

# Makeflow Workflow Execution Instances

This repository contains workflow execution instances generated from
[Makeflow](http://ccl.cse.nd.edu/software/makeflow/) workflow
executions. The instances hosted in this repository use the
[WfCommons JSON format](https://github.com/wfcommons/workflow-schema)
for describing workflow executions.

#### Repository Structure

Workflow execution instances are organized into sub-folders within this
repository. Each sub-folder represents a _workflow application_, which
itself contains sub-folders for workflow executions in different
_computing platforms_.

#### Workflow Simulator

The execution instances provided in this repository are compatible to any
[simulator framework](https://wfcommons.org/simulation) that
implements the
[WfCommons JSON format](https://github.com/wfcommons/workflow-schema).

## Summary of Workflow Execution Instances

| Application | Science Domain | Category | Computing Platforms | # Execution Instances |
| --- | --- | --- | --- | --- |
| BLAST | Bioinformatics | Compute-intensive | 1 | 15 |
| BWA | Bioinformatics | Data-intensive | 1 | 15 |
