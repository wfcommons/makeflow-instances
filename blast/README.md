<a href="https://workflowhub.org" target="_blank"><img src="https://workflowhub.org/assets/images/logo-horizontal.png" width="300" /></a>

<img src="http://ccl.cse.nd.edu/software/makeflow/MakeflowLogoSmall.png" width=160 />

# Execution Traces for BLAST Workflow

## Workflow Description

[BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) is a toolkit for finding
regions of similarity between biological sequences. The program compares
nucleotide or protein sequences to sequence databases and calculates the
statistical significance. The test case implemented as a
[Makeflow workflow](https://github.com/cooperative-computing-lab/makeflow-examples/tree/master/blast)
aim to run BLAST tasks against large reference databases in a reasonable
amount of time. This test case is composed of four different tasks:

  1. `split_fasta` - split the reference file into pieces.
  2. `blastall` - run the BLAST program.
  3. `cat_blast` - merge results from each BLAST execution.
  4. `cat` - merge error messages from each BLAST execution.

The figure below shows an overview of the BLAST workflow structure:

<img src="docs/images/blast.png?raw=true" width="500">

## Execution Traces

Execution traces are formatted according to the
[WorkflowHub JSON format](https://github.com/workflowhub/workflow-schema) for
describing workflow executions. Execution traces from different computing
platforms are organized into sub-folders.

Trace files are named using the following convention:
`blast-<COMPUTE_PLATFORM>-<WF_SIZE>-<RUN_ID>.json`, where:

- `<COMPUTE_PLATFORM>`: The compute platform where the actual Makeflow workflow
  was executed (e.g., `chameleon`).
- `<WF_SIZE>`: The size of the workflow (small, medium, large), which depends
  on the query size and number of sequences per split.
- `<RUN_ID>`: The workflow execution identification.

### Workflow Structure

The BLAST workflow structure is only dependent on the _workflow size_
(`<WF_SIZE>`), which defines the number of `blastall` tasks – it depends on the
query size and number of sequences per split (as defined in the
[workflow GitHub repository](https://github.com/cooperative-computing-lab/makeflow-examples/tree/master/blast)).
The workflow has also three additional tasks: `split_fasta`, `cat_blast`,
and `cat`.
