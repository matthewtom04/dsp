[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)




```python
import scipy.stats

## Set up the normal distribution with mean and standard deviation of male height
mu = 178
sigma = 7.7
distribution = scipy.stats.norm(loc=mu, scale=sigma)

minimum_height = (5*12+10)*2.54        # Convert minimum height 5'10" to cm
maximum_height = (6*12+1)*2.54         # Max height 6'1" to cm

lower_bound = distribution.cdf(minimum_height)
upper_bound = distribution.cdf(maximum_height)
print upper_bound-lower_bound
```

>> So about **34.27%** of US male population are within the height range

