[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> The code used to answer the question posed is as follows:
```
# Imports all necessary modules for the analysis
from __future__ import print_function, division

%matplotlib inline

import numpy as np
import nsfg
import first

# Imports the pregnancy data used and filters it to only include live births
preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

# Separates the births into two groups, one of first babies and another without first babies
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

# Defines the function that finds the Cohen's d effect for the difference between the averages of two groups
def CohenEffectSize(group1, group2):
    """Computes Cohen's effect size for two groups.
    
    group1: Series or DataFrame
    group2: Series or DataFrame
    
    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d

# Calculates Cohen's d effect for the difference in weight between first babies and other babies
weight_cohen_d = CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

# Calculates Cohen's d effect for the difference in pregnancy length between first babies and other babies
weight_cohen_d = CohenEffectSize(firsts.prglngth, others.prglngth)
```
The result of this code shows that the size of Cohen's d effect for the difference in weight between first babies and other babies is -0.0887, which means that the mean of the weight of first babies is 0.0887 standard deviations smaller than that of other babies. This result shows that the difference in weight between first babies and other babies is very small.

However, the absolute Cohen's d effect for the difference in weight between first babies and other babies is greater than that for the difference in lengths of pregnancies between first babies and other babies, which is 0.0289.
