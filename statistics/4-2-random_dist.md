[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)


Solution:
The plot is normally distributed.


Python:
import numpy as np
import thinkstats2
import thinkplot

#generating the 1000 random numbers between 0-1
rand = np.random.random(1000)
pmf = thinkstats2.Pmf(rand, label = 'PMF')
cdf = thinkstats2.Cdf(rand, label = 'CDF')


width = 0.4 / 16

# plot PMFs 
thinkplot.Pmf(pmf, linewidth=0.1)
thinkplot.Config(xlabel='Random variate', ylabel='PMF')

# plot CDF
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='Random variate', ylabel='CDF')
