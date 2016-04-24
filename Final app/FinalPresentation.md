Developing Data Products : Deploying a Shiny App
========================================================
author: Josue Lavandeira        
date: April 24, 2016 
width: 1200
height: 800

Background
========================================================

In the dataset 'iris' there are many observations which can be clustered in different forms, 
this app uses the reactive clustering method to cluster the observations by the different 
variables in the data. It can create up to 10 clusters and plot them in a matrix, which will 
have as 'x' and 'y' axes, the different variables of the observations.

The application also shows the data contained in each cluster, and additional documentation.


Application goals
========================================================

There are a few goals that this application aims to comply:

- It must be able to create between 1 and 10 clusters of data.
- It must be able to plot these clusters in a single matrix.
- It must be able to show the data contained in the clusters.
- The clustering matrix must show each cluster in a different color.


The 'iris' data
========================================================
We can observe the basic structure of the 'iris' data here:


```r
library(datasets)
str(iris)
```

```
'data.frame':	150 obs. of  5 variables:
 $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
 $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
 $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
 $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
 $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...
```

The 'iris' data
========================================================
Here we may observe the correlations between the 'iris' data variables.


```r
plot(iris)
```

![plot of chunk unnamed-chunk-2](FinalPresentation-figure/unnamed-chunk-2-1.png)
