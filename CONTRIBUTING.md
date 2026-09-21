# Contributing

Thank you for your interest in contributing to **Accessible Code-Generated Visualizations**.

This repository contains educational materials for creating more accessible
code-generated visualizations in Python and R, with particular attention to
blind and visually impaired learners.

## What contributions are welcome?

Useful contributions include:

- additional accessible graph types
- equivalent examples in Python and R
- improvements to existing notebooks
- clearer accessibility explanations
- improved textual descriptions
- additional non-visual access methods
- sonification examples
- bug fixes
- documentation improvements
- reproducibility improvements

## Contribution principles

Please keep contributions aligned with the main goals of the repository:

1. **Prioritize semantic meaning**  
   Visualizations should clearly communicate what variables, relationships,
   patterns, or computational processes are represented.

2. **Preserve computational context**  
   Examples should make it possible to understand how the graph relates to the
   code, data, parameters, and transformations used to generate it.

3. **Support reproducibility**  
   Code examples should be runnable and should avoid unnecessary external
   dependencies where possible.

4. **Support non-visual exploration**  
   When appropriate, include textual descriptions, structured data access, or
   another non-visual representation.

## Adding a new graph example

When contributing a new graph type, please aim to include:

1. a short explanation of what the graph is used for
2. a short explanation of how to make it more accessible
3. a worked accessible example
4. a reusable template with placeholders
5. a textual interpretation or description of the resulting graph

If both Python and R implementations are appropriate, please try to keep the
examples conceptually equivalent.

## Accessibility expectations

Contributed visualizations should, where appropriate:

- use descriptive titles
- use meaningful axis labels
- include measurement units
- use readable font sizes
- avoid relying on color alone
- use high-contrast or colorblind-friendly palettes
- use redundant encodings such as markers, line styles, labels, or textures
- avoid unnecessary clutter
- make underlying data or source code available

## Python contributions

Place Python notebooks in the `python/` directory.

For new notebook examples:

- use Jupyter notebooks (`.ipynb`)
- keep the code simple and instructional
- use Matplotlib for graph examples unless there is a strong reason to use
  another library
- document any additional dependencies in `requirements.txt`

Do not commit API keys or other credentials.

## R contributions

Place R notebooks in the `R/` directory.

For new R notebook examples:

- use Jupyter notebooks (`.ipynb`) with an R kernel
- use `ggplot2` for graph examples unless there is a strong reason to use
  another plotting library
- keep the implementation simple and instructional
- document any additional R package requirements in the README

## API-based examples

Some examples may rely on external services, such as Gemini.

If you contribute an API-based example:

- never include API keys in code or committed files
- use environment variables or another secure credential mechanism
- clearly document which API key is required
- make it clear which parts of the example require external access

## Style

Please keep code and documentation:

- clear
- concise
- reproducible
- beginner-friendly where possible
- consistent with the surrounding repository structure

Avoid adding unnecessary abstractions or dependencies.

## Pull requests

When submitting a pull request:

1. describe what you changed
2. explain why the change improves the repository
3. mention any new dependencies
4. confirm that notebooks or scripts run successfully in your environment
5. note any accessibility considerations relevant to the change

## Issues

If you find a bug, inaccessible example, broken notebook, unclear explanation,
or reproducibility issue, please open a GitHub issue with enough detail to
reproduce the problem.

## License

By contributing to this repository, you agree that your contribution may be
distributed under the repository's **MIT License**.
