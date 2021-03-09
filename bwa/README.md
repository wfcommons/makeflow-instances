<a href="https://wfcommons.org" target="_blank"><img src="https://wfcommons.org/images/wfcommons-horizontal.png" width="350" /></a>

<img src="http://ccl.cse.nd.edu/software/makeflow/MakeflowLogoSmall.png" width=160 />

# Execution Traces for BWA Workflow

## Workflow Description

[BWA](http://bio-bwa.sourceforge.net) is a software package for mapping
low-divergent sequences against a large reference genome, such as the
human genome. The test case implemented as a
[Makeflow workflow](https://github.com/cooperative-computing-lab/makeflow-examples/tree/master/bwa)
aim to run BWA tasks against large reference databases in a reasonable
amount of time. This test case is composed of five different tasks:

  1. `fastq_reduce` - subsample the reference file into parts.
  2. `bwa_index` - produce index from reference file.
  3. `bwa` - search for the queries in a shared reference database.
  4. `cat_bwa` - merge results from each BWA execution.
  5. `cat` - merge error messages from each BWA execution.

The figure below shows an overview of the BWA workflow structure:

<img src="docs/images/bwa.png?raw=true" width="500">

## Execution Traces

Execution traces are formatted according to the
[WfCommons JSON format](https://github.com/wfcommons/workflow-schema) for
describing workflow executions. Execution traces from different computing
platforms are organized into sub-folders.

Trace files are named using the following convention:
`bwa-<COMPUTE_PLATFORM>-<WF_SIZE>-<RUN_ID>.json`, where:

- `<COMPUTE_PLATFORM>`: The compute platform where the actual Makeflow workflow
  was executed (e.g., `chameleon`).
- `<WF_SIZE>`: The size of the workflow (small, medium, large), which depends
  on the query size and number of sequences per split.
- `<RUN_ID>`: The workflow execution identification.

### Workflow Structure

The BWA workflow structure is only dependent on the _workflow size_
(`<WF_SIZE>`), which defines the number of `bwa` tasks – it depends on the
query size and number of sequences per split (as defined in the
[workflow GitHub repository](https://github.com/cooperative-computing-lab/makeflow-examples/tree/master/bwa)).
The workflow has also three additional tasks: `bwa_index`, `fastq_reduce`,
`cat_bwa`, and `cat`.
