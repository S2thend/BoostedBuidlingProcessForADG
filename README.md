# BoostedBuidlingProcessForADG
[![pypi badge](https://img.shields.io/badge/PyPi-0.1.0-blue.svg)](https://pypi.org/project/bbp4adg/#description)
[![License badge](https://img.shields.io/badge/License-MIT-<COLOR>.svg)](https://shields.io/)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md)

Implementation of A novel machine learning method for my researches in this field.

This method is only for binary classification tasks up until current version.

## Quick Start

### install
```sh
pip install bbp4adg
```

### import and initialize:
```py
# from exports import BBP, ADG
from bbp4adg import BBP, ADG

adg = BBP(threshold=delta)
```

### start training
```py
# Or adg = ADG(threshold=delta) for original adg
model, perf =adg.fit(X,y)
print('arguments count:', len(model.arguments)) 
print(model.arguments)
print('relations count:', len(model.relations))
print(model.relations)
print("accuracy:", perf)
```

### evaluate on test set
```py
print("test accuracy:", adg.score(X_test,y_test))
```

## ToDos
1. more comments
2. doc tests
3. more semantics than grounded

## How to contribute
Issues and PRs are welcomed.

Please read the [contributing document](https://github.com/S2thend/BoostedBuidlingProcessForADG/blob/main/CONTRIBUTING.md).