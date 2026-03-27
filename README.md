# NCD Simulator Package

This repository contains a self-contained static simulator for illustrating a simplified NCD waiver thought experiment. It is designed for communication and sensitivity analysis, not as a rule-level exact pricing or policy engine.

## Main Files
- [index.html](./index.html): default entry page for local viewing and GitHub Pages
- [simulation.html](./simulation.html): compatibility entry that redirects to the main page
- [math_model.md](./math_model.md): mathematical assumptions and model notes
- [vendor-mathjax](./vendor-mathjax): local MathJax runtime used for formula rendering
- [vendor-katex](./vendor-katex): local KaTeX CSS and fonts

## Local Preview
Open [index.html](./index.html) directly in a browser. The simulator is fully static and does not require a backend service.

## GitHub Pages Demo
After GitHub Pages is enabled for this repository, the online demo will be available at:

- Root entry: [https://xiang-shan.github.io/-NCD-/](https://xiang-shan.github.io/-NCD-/)
- Compatibility entry: [https://xiang-shan.github.io/-NCD-/simulation.html](https://xiang-shan.github.io/-NCD-/simulation.html)

## Modeling Scope
The simulator mirrors the current simplified project logic:

- annual claim counts are modeled with a Poisson assumption
- NCD movement is represented as a yearly Markov-style transition
- the tool is intended to support transparent discussion of assumptions and trade-offs

It should be interpreted as an analytical thought experiment rather than a final market rule, unpublished methodology, or production pricing engine.
