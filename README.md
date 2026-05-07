# BoostedBuidlingProcessForADG

[![pypi badge](https://img.shields.io/badge/PyPi-0.1.0-blue.svg)](https://pypi.org/project/bbp4adg/#description)
[![License badge](https://img.shields.io/badge/License-MIT-blue.svg)](https://shields.io/)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md)

Implementation of a novel machine learning method from my research in this field.
This method currently supports binary classification tasks only.

The method is described in detail in the accompanying MSc dissertation:
**"Boosted Building Processes for Learning Argumentation Graphs from Data for Enhanced Interpretability and Accuracy"**, Technological University Dublin, 2024.
Catalogue record: <https://library.tudublin.ie/record=b5773155>

> 📚 **If you use this work in your research, please [cite it](#citation).**

## Table of Contents

- [Quick Start](#quick-start)
  - [Install](#install)
  - [Import and Initialize](#import-and-initialize)
  - [Start Training](#start-training)
  - [Evaluate on a Test Set](#evaluate-on-a-test-set)
- [ToDos](#todos)
- [How to Contribute](#how-to-contribute)
- [Citation](#citation)
- [License](#license)

## Quick Start

### Install

```sh
pip install bbp4adg
```

### Import and Initialize

```py
# from exports import BBP, ADG
from bbp4adg import BBP, ADG

adg = BBP(threshold=delta)
```

### Start Training

```py
# Or use adg = ADG(threshold=delta) for the original ADG.
model, perf = adg.fit(X, y)

print('arguments count:', len(model.arguments))
print(model.arguments)
print('relations count:', len(model.relations))
print(model.relations)
print('accuracy:', perf)
```

### Evaluate on a Test Set

```py
print('test accuracy:', adg.score(X_test, y_test))
```

## ToDos

1. More comments
2. Doc tests
3. More semantics than grounded

## How to Contribute

Issues and PRs are welcome.
Please read the [contributing document](https://github.com/S2thend/BoostedBuidlingProcessForADG/blob/main/CONTRIBUTING.md).

## Citation

If you use this work in your research, please cite the dissertation:

**APA (7th edition)**

> Cai, B. (2024). *Boosted building processes for learning argumentation graphs from data for enhanced interpretability and accuracy* [Master's dissertation, Technological University Dublin]. TU Dublin Library Catalogue. https://library.tudublin.ie/record=b5773155

**IEEE**

> B. Cai, "Boosted building processes for learning argumentation graphs from data for enhanced interpretability and accuracy," M.S. dissertation, Technological Univ. Dublin, Dublin, Ireland, 2024. [Online]. Available: https://library.tudublin.ie/record=b5773155

**BibTeX**

```bibtex
@mastersthesis{cai2024boosted,
  author  = {Cai, Borui},
  title   = {Boosted Building Processes for Learning Argumentation Graphs from Data for Enhanced Interpretability and Accuracy},
  school  = {Technological University Dublin},
  year    = {2024},
  address = {Dublin, Ireland},
  type    = {{MSc} dissertation},
  url     = {https://library.tudublin.ie/record=b5773155}
}
```

## License

Released under the [MIT License](LICENSE).
