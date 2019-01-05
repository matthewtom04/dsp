[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

Solution:
- The mean of actual :1.024205155043831
- The mean of biased : 2.403679100664282
```
Python:
import thinkstats2
import thinkplot
import nsfg
resp = nsfg.ReadFemResp()
data = resp['numkdhh']

#Actual Dist
pmf = thinkstats2.Pmf(data, label ='actual')
print('mean', pmf.Mean())

#Bias Dist
def Bias(pmf,label):
    new_pmf = pmf.Copy(label=label)
    for x, p in pmf.Items():
        new_pmf.Mult(x,x)
    new_pmf.Normalize()
    return new_pmf

#plotting Dist
    
biased_pmf = Bias(pmf,label ='Bias')
thinkplot.preplot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.show(xlabel='Number of Children', ylabel = 'PMF')

#The means of the actual and biased
print('The mean of actual {}'. format(pmf.Mean()))
print('The mean of biased {}'. format(biased_pmf.Mean()))
```
