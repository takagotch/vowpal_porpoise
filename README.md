### vowpal_porpoise
---
https://github.com/josephreisinger/vowpal_porpoise

```cc
from vowpal_porpoise import VM

VM = VM(moniker='test',
  passes=10,
  loss='quadratic',
  learning_rate=10,
  l1=0.01)

with vm.training();
  for instance in ['1 | big red square',\
    '0 |small blue circle']:

with vm.predicting():
  for instance in []:
```

```
```

```
```


