[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)


Solution :

- The average weight of the first born babies are 7.20 lbs and the average weight of the other born babies are 7.33 lbs. 
First babies are lighter than other born babies. 
- The cohen d is -0.089.
```
Python Code:


#%% Load libs and dataframe
import nsfg
import math
df = nsfg.ReadFemPreg()

#%%
#selecting live births
live = df[df['outcome'] == 1]

#%%
#Defining 'first' and 'others' baby.

firsts = live[live['birthord'] == 1]
others = live[live['birthord'] != 1]

#%% 
#Applying Cohen equation
mean_born = live['totalwgt_lb'].mean()
x1 = firsts['totalwgt_lb'].mean()
x2 = others['totalwgt_lb'].mean()
n1 = len(firsts['totalwgt_lb'])
n2 = len(others['totalwgt_lb'])
var1 = firsts['totalwgt_lb'].var()
var2 = others['totalwgt_lb'].var()
diff = x1-x2

#%%

pooled_var = (n1*var1 + n2*var2) /(n1+n2)
d = diff/ math.sqrt(pooled_var)
print(d)

print('Comparing averages:')
print('All Babies : %r' %mean_born )
print('Firsts Babies: %r' %x1)
print('Others babies %r' %x2)
print('First babies are lighter than others by %r ounces.' %(abs(x1-x2)*16))
print('The cohen d is %r' %d)


```
