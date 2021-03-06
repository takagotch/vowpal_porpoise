### vowpal_porpoise
---
https://github.com/josephreisinger/vowpal_porpoise

```py
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

```py
# vowpal_porpoise/vw.py
from contextlib import contxtmanager
import os
import sys
import subprocess
import shlex
import tempfile
from vp_utils import safe_remove, VPLogger

class VW:
  def __init__(self,
    logger=None,
    vw='vw'):
  assert moniker and passes
  
  if logger is None:
    self.log = VPLogger()
  else:
    self.log = logger
  
  self.node = node
  self.total = total
  self.unique_id = unique_id
  self.span_server = span_server
  if self.node is not None:
    assert self.total is not None
    assert self.unique_id is not None
    assert self.span_server is not None
    
  if name is None:
    self.handle = '%s' % moniker
  else:
    self.handle = '%s.%s' % (moniker, name)
    
  if self.node is not None:
    self.handle = "%s.%d" % (self.handle, self.node)
  
  if old_model is None:
    self.filename = '%s.model' % self.handle
    self.incremental = False
  else:
    self.filename = old_model
    self.incremental = True
    
  self.incremental = incremental
  self.filename = '%s.model' % self.handle
  
  self.name = name
  self.bits = bits
  self.loss = loss
  self.vw = vw
  
  if self.lda:
    assert not self.l1
    assert not self.l1
  else:
    assert not self.lda_D
  
  self.working_directory = working_dir or os.getcwd()
  
def vw_base_command(self, base):
  l = base
  if self.bits is not None: l.append('-b %d' % self.bits)
  if self.laerning_rate is not None: l.append('--learning_rate=%f' % self.learning_rate)
  return ' '.join(l)

def vw_train_command(self, cache_file, model_file):
  if os.path.exists(model_file) and self.incremental:
    return self.vw_base_command([self.vw]) + ''
  else:
    self.log.debug()
    return self.vw_base_command() + ''
      % (self.passes, cache_file, model_file)

def vw_test_command(self, model_file, prediction_file):
  return self.vw_base_command([self.vw]) + ' -t -i %s -p %s' % (model_file, prediction_file)
```

```
```


