[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> The code for the answer to this question is:

```
# Imports the modules necessary for the analysis
from __future__ import print_function, division

%matplotlib inline

import numpy as np
import nsfg
import first
import thinkstats2
import thinkplot

# Creates a function that will take an actual PMF and create its observation-biased PMF
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf

# Reads the data from the pregnancy data file, selecting the column for number of kids in the household
resp = nsfg.ReadFemResp()

# Calculates actual and biased PMF
actual_dist = thinkstats2.Pmf(resp.numkdhh, label='actual')
biased_dist = BiasPmf(actual_dist, label='biased')

# Plots a histogram of the two PMFs
thinkplot.Pmfs([actual_dist, biased_dist])
thinkplot.Config(x_label='Number kids', y_label='PMF') # Solution goes here

# Calculates the mean of the actual and biased PMFs and prints them
actual_mean = actual_dist.Mean()
print('Actual distribution mean: ', actual_mean)
biased_mean = biased_dist.Mean()
print('Biased distribution mean: ', biased_mean)# Solution goes here
