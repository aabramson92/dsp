[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> The code used to analyze the data is as follows:

```
# Import necessary modules
from __future__ import print_function, division

%matplotlib inline

import numpy as np
import nsfg
import first
import thinkstats2
import thinkplot

# Generate the numpy random.random function, PMF, CDF, and plot of the PMF and CDF
rand = np.random.random([1000]) # Solution goes here
rand_pmf = thinkstats2.Pmf(rand, label='PMF') # Solution goes here
rand_cdf = thinkstats2.Cdf(rand, label='CDF') # Solution goes here
thinkplot.Pmf(rand_pmf)
thinkplot.Cdf(rand_cdf)
thinkplot.Config(x_label='Number', y_label='Prob.')
```
The analysis of the data shows that while the distribution of the sample appears to be uniform according to its PMF, the CDF shows some slight variances from this uniformity as some values occur more frequently than others since it does not have a straight line from 0 to 1.
