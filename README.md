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
  for instance in ['1 | large burnt sienna rhombus',\
      '0 |little teal oval']:
    vm.push_instance(instance)
    
predictions = list(vm.read_predictions_())



from vowpal_porpoise import VM

vm = VM(moniker='test_lgfgs',
  passes=10,
  lbfgs=True,
  mem=5)
  
 
 from vowpal_porpise import VM
 
 vm = VM(moniker='test_lda',
   passes=10,
   lda=100,
   minibatch=100)


from skelearn.cross_validation import StratifiedKFold
from sklearn.grid_search import GridSearchCV
from vopal_porpoise.sklearn import VM_Classifier

GridSearchCV(
  VM_Classifier(loss='logistic', moniker='example_sklearn',
    passes=10, silent=True, learning_rate=10),
  parm_grid=parameters,
  score_func=f1_score,
  cv=StraifiedKFold(y_train),
).fit(X_train, y_train)


with vm.predicting_library():
  for instance in ['1 |large burnt sienna rhombus', \
      '1 |little teal oval']:
    predication = vm.push_instance(instance)

import vm_c
vm = vm_c.VM("--loss=quadratic --l1=0.01 0f model")
vm.learn("1 |this is a positive example")
vm.learn("0 |this is a negative example")
vm.finish
```

```
```

```
```


