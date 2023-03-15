# TCC *vs* LCC

Explain under which circumstances *Tight Class Cohesion* (TCC) and *Loose Class Cohesion* (LCC) metrics produce the same value for a given Java class. Build an example of such as class and include the code below or find one example in an open-source project from Github and include the link to the class below. Could LCC be lower than TCC for any given class? Explain.

## Answer
LCC or Loose Class Cohesion is a metrics related to indirect cohesion of classes which can be like a class Toto have a depency on a class Tata which have a dependecy on another class Titi. In this case, the first class Toto have a (loose) dependency on class Titi. 
TCC or Tight Class Cohesion is a metric related to direct cohesion/dependency between 2 classes. 
If this metrics is above 70%, then it's means that they might not be split in another subcomponents. Therefore, if this metrics is below 50% then it's means that thoses classes do different work.
There is some cases when TCC and LCC produce the same value. 
