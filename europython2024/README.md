# Sciline: Assemble task graphs using type-hint-driven dependency injection

## Abstract

Writing, testing, and maintaining complex data analysis workflows is hard.
Boiler-plate code may hide the actual analysis, making it hard to understand.
The code may be hard to test, leading to bugs.

Workflow management systems like [AiiDA](https://www.aiida.net/) or [Snakemake](https://snakemake.readthedocs.io/en/stable/)
can help with this by using a set of calculations or rules declaring their inputs and outputs.
They then automatically assemble a task graph, and run the tasks in the correct order to compute the desired outputs.
Tasks may be complex, with many internal computation steps, but splitting them may not be feasible, e.g., due to overhead.
[Sciline](https://scipp.github.io/sciline) can be a solution here.
It is a pure Python package with no dependencies, and it does not require invasive changes to your existing Python code.

Sciline takes a *declarative* approach, inspired by [dependency injection](https://en.wikipedia.org/wiki/Dependency_injection) frameworks.
By relying on Python's type-hinting, a [domain-specific language](https://en.wikipedia.org/wiki/Domain-specific_language) is used to describe the workflow.
This enforces a clear expression of intent, aiding readability and enabling automatic assembly of a task graph that can compute desired outputs.
The task graphs Sciline assembles can then be executed, e.g., using [Dask](https://dask.org/).

## Description
This presentation will be in the form of a live demo of Sciline. Sciline is an open-source project developed by the European Spallation Source under the BSD-3 licence. It is installable on Linux, Mac and Windows via pip and conda, and the documentation is hosted at https://scipp.github.io/sciline . The source code can be found at https://github.com/scipp/sciline . Co-authors: Jan-Lukas Wynen, Johannes Kasimir, Neil Vaytet, Simon Heybrock, Sunyoung Yoo.
