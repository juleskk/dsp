[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

#Problem

#Solving

First, convert to metric units. 

5'10" = 177.8 cm

6'1" = 185.4 cm

```
shortest = dist.cdf(177.8)
tallest = dist.cdf(185.4)
tallest - shortest

```

#Solution
34.2%
