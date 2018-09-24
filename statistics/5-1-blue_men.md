[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> The code to analyze the data is as follows:

```
# Imports all necessary modules
from __future__ import print_function, division

%matplotlib inline

import numpy as np
import nsfg
import first
import analytic
import thinkstats2
import thinkplot
import scipy.stats

# Sets dist equal to a normal distribution with mean 'mu' and standard distribution 'sigma'
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

# Enters the low value for the height and the high value for the height
low = dist.cdf(177.8)
high = dist.cdf(185.4)

# Calculates the CDF for the low and high points, then finds the CDF between those points
low, high, high - low 
```

Calculating the CDF for these heights shows that 34.21% of the male population meets the height requirements for the Blue Man Group.
