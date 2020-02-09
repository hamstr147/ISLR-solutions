Exercise 1
==========

*For each part 1 through 4, indicate whether we would generally expect
the performance of a flexible statistical learning method to be better
or worse than an inflexible method. Justify your answer.*

1.  *The sample size* n *is extremely large, and the number of
    predictors* p *is small.* A flexible model would outperform an
    inflexible model as the risk of overfitting with a small number of
    predictors relative to observations is small.

2.  *The number of predictors* p *is extremely large, and the number of
    observations* n *is small.* An inflexible model would perform better
    than an inflexible model as a flexible model is likely to overfit
    the data.

3.  *The relationship between the predictors and response is highly
    non-linear.* A flexible model would outperform an inflexible model
    given a flexible model’s lower bias.

4.  *The variance of the error terms, i.e.*
    *σ*<sup>2</sup> = *V**a**r*(*ϵ*)*, is extremely high.* An inflexible
    model would outperform a flexible model.

Exercise 2
==========

1.  We collect a set of data on the top 500 firms in the US. For each
    firm we record profit, number of employees, industry and the CEO
    salary. We are interested in understanding which factors affect CEO
    salary.

We are interested in inference, this is a regression problem, and n =
500 and p = 3.

1.  We are considering launching a new product and wish to know whether
    it will be a success or a failure. We collect data on 20 similar
    products that were previously launched. For each product we have
    recorded whether it was a success or failure, price charged for the
    product, marketing budget, competition price, and ten other
    variables.

We are interested in prediction, this is a classification problem, and n
= 20 and p = 13.

1.  We are interested in predicting the % change in the US dollar in
    relation to the weekly changes in the world stock markets. Hence we
    collect weekly data for all of 2012. For each week we record the %
    change in the dollar, the % change in the US market, the % change in
    the British market, and the % change in the German market.

We are interested in prediction, this is a regression problem, and n =
52 and p = 3.

\#Exercise 3 b) Bias is high for an inflexible method but reduces as
flexibility increases as more flexible models fit the data more closely.
Variance will be low for an inflexible model but will increase as
flexibility increases as models start to overfit the data. The
irreducible error is a fixed value for a given data set and represents
the lower bound for the test error. For classification problems, the
irreducible error is the proportion of points that lie on the wrong side
of the Bayes decision boundary. The test error cannot go below the
irreducible error but will reduce as flexibility increases, but at a
certain point inflects as the model starts to overfit the data. This is
the point at which the training data goes below the irreducible error
(overfitting). The training error always reduces as flexibility
increases as more flexibility will fit the training data more closely.

\#Exercise 4 a) Describe three real-life applications in which
classification might be useful. Describe the response, as well as the
predictors. Is the goal of each application inference or prediction? -
Whether a stock price moves up or down is an example of a predictive
classification problem. We might use lagged stock prices or financial
results of a company as predictors. - Understanding why a member of the
public votes for the Labour or Conservative parties is an inferential
classification problem. We might take demographic information like
income, gender, religion, profession, and age as predictors. - Medical
diagnosis is a predictive classification problem. We might have
sympotoms patients are suffering from, medical history, age, and
lifestyle indicators like smoker/non-smoker, level of exercise, diet
etc. as predictors.

1.  Describe three real-life applications in which regression might be
    useful. Describe the response, as well as the predictors. Is the
    goal of each application inference or prediction?

-   An estate agent predicting house price movements is an example of
    regression where prediction is the goal. The response would be house
    prices and the predictors might be proximity to transport links,
    crime rates, proximity to good schools, number of rooms and type of
    property.
-   A social scientist understanding the determinants of military
    spending is an example of an inferential regression problem. The
    response would be military spending in inflation-adjusted USD, and
    the predictors might be country characteristics like GDP,
    population, number of countries it shares a border with, whether it
    is in an international dispute and whether it maintains military
    alliances.
-   A company forecasting sales is an example of a predictive regression
    problem. They might use lagged sales data, marketing expenditure,
    and economic indicators as predictors, and sales in monetary value
    as a response.

1.  Describe three real-life applications in which cluster analysis
    might be useful. Possible applications of cluster analysis might be:

-   A marketing company segmenting customers;
-   Clustering financial transactions to identify unusual transactions;
-   Recommender systems for an online streaming service.

\#Exercise 5 A very flexible method has low bias and will fit highly
non-linear data well. A less flexible approach might be preferred where
there are very few observations so you may want to minimise the risk of
overfitting, as a high variance method would likely result in a
signficantly different model for unseen data. Less flexible methods like
linear regression are more easily interpretable so might be preferred
for an inference problem, while prediction might lead you to choose a
more flexible model.

\#Exercise 6 A parametric model requires the estimation of a fixed set
of values that define a function that we use to calculate outputs. An
example of this is linear regression, where we estimate coefficients
applied to each predictor (and a constant). A non-parametric method,
like KNN, does not simplify the problem to estimating a small number of
values as they it would not make any assumptions about a specific
functional form. Instead it would fit a model that closely fits the data
while attempting not to overfit. A non-parametric model might perform
better if the distribution of the data is unknown, as it would fit a
wider range of distributions. However, to ensure that the model does not
overfit, we would need a large number of observatins - a small number
might mean a parametric method might perform better.

\#Exercise 7

    #Data
    data.frame(
      X1 = c(0,2,0,0,-1,1),
      X2 = c(3,0,1,1,0,1),
      X3 = c(0,0,3,2,1,1),
      Y = c("Red", "Red", "Red", "Green", "Green", "Red"),
      stringsAsFactors = FALSE
      )

    ##   X1 X2 X3     Y
    ## 1  0  3  0   Red
    ## 2  2  0  0   Red
    ## 3  0  1  3   Red
    ## 4  0  1  2 Green
    ## 5 -1  0  1 Green
    ## 6  1  1  1   Red

    #distance from test point (0,0,0)
    c(3, 2, sqrt(1 + 3^2), sqrt(1 + 2^2), sqrt(1 + 1), sqrt(2 + 1))

    ## [1] 3.000000 2.000000 3.162278 2.236068 1.414214 1.732051

If K = 1, then our prediction would be Green, as this is the closest
single point. If K = 3, then our prediction would be Red, as two of the
three closest points are Red, and just one is Green. If the Bayes’
decision boundary is highly non-linear, we would expect a low K to give
a better prediction, as it would fit the decision boundary more closely
and be less linear than a large K.

\#Exercise 8

First read in the College data set, and make the names of each college
row names:

    college <- read.csv("http://faculty.marshall.usc.edu/gareth-james/ISL/College.csv")
    rownames(college) <- college[, 1]
    college <- college[, -1]

Now take a look at some summary statistics, pairwise plots, and boxplots
to explore the data:

    summary(college)

    ##  Private        Apps           Accept          Enroll       Top10perc    
    ##  No :212   Min.   :   81   Min.   :   72   Min.   :  35   Min.   : 1.00  
    ##  Yes:565   1st Qu.:  776   1st Qu.:  604   1st Qu.: 242   1st Qu.:15.00  
    ##            Median : 1558   Median : 1110   Median : 434   Median :23.00  
    ##            Mean   : 3002   Mean   : 2019   Mean   : 780   Mean   :27.56  
    ##            3rd Qu.: 3624   3rd Qu.: 2424   3rd Qu.: 902   3rd Qu.:35.00  
    ##            Max.   :48094   Max.   :26330   Max.   :6392   Max.   :96.00  
    ##    Top25perc      F.Undergrad     P.Undergrad         Outstate    
    ##  Min.   :  9.0   Min.   :  139   Min.   :    1.0   Min.   : 2340  
    ##  1st Qu.: 41.0   1st Qu.:  992   1st Qu.:   95.0   1st Qu.: 7320  
    ##  Median : 54.0   Median : 1707   Median :  353.0   Median : 9990  
    ##  Mean   : 55.8   Mean   : 3700   Mean   :  855.3   Mean   :10441  
    ##  3rd Qu.: 69.0   3rd Qu.: 4005   3rd Qu.:  967.0   3rd Qu.:12925  
    ##  Max.   :100.0   Max.   :31643   Max.   :21836.0   Max.   :21700  
    ##    Room.Board       Books           Personal         PhD        
    ##  Min.   :1780   Min.   :  96.0   Min.   : 250   Min.   :  8.00  
    ##  1st Qu.:3597   1st Qu.: 470.0   1st Qu.: 850   1st Qu.: 62.00  
    ##  Median :4200   Median : 500.0   Median :1200   Median : 75.00  
    ##  Mean   :4358   Mean   : 549.4   Mean   :1341   Mean   : 72.66  
    ##  3rd Qu.:5050   3rd Qu.: 600.0   3rd Qu.:1700   3rd Qu.: 85.00  
    ##  Max.   :8124   Max.   :2340.0   Max.   :6800   Max.   :103.00  
    ##     Terminal       S.F.Ratio      perc.alumni        Expend     
    ##  Min.   : 24.0   Min.   : 2.50   Min.   : 0.00   Min.   : 3186  
    ##  1st Qu.: 71.0   1st Qu.:11.50   1st Qu.:13.00   1st Qu.: 6751  
    ##  Median : 82.0   Median :13.60   Median :21.00   Median : 8377  
    ##  Mean   : 79.7   Mean   :14.09   Mean   :22.74   Mean   : 9660  
    ##  3rd Qu.: 92.0   3rd Qu.:16.50   3rd Qu.:31.00   3rd Qu.:10830  
    ##  Max.   :100.0   Max.   :39.80   Max.   :64.00   Max.   :56233  
    ##    Grad.Rate     
    ##  Min.   : 10.00  
    ##  1st Qu.: 53.00  
    ##  Median : 65.00  
    ##  Mean   : 65.46  
    ##  3rd Qu.: 78.00  
    ##  Max.   :118.00

    pairs(college[, 1:10])

![](ISLR_chap2_files/figure-markdown_strict/unnamed-chunk-3-1.png)

    plot(college$Private, college$Outstate)

![](ISLR_chap2_files/figure-markdown_strict/unnamed-chunk-3-2.png)

Now create a new categorical variable called `Elite` by binning the
`Top10perc` variable. Then call `summary` to see how many elite colleges
there are and plot against `Outstate`.

    #Create Elite variable
    Elite <- rep("No", nrow(college))
    Elite[college$Top10perc > 50] <- "Yes"
    Elite <- as.factor(Elite)
    college <- data.frame(college, Elite)

    #Explore the new variable
    summary(college)

    ##  Private        Apps           Accept          Enroll       Top10perc    
    ##  No :212   Min.   :   81   Min.   :   72   Min.   :  35   Min.   : 1.00  
    ##  Yes:565   1st Qu.:  776   1st Qu.:  604   1st Qu.: 242   1st Qu.:15.00  
    ##            Median : 1558   Median : 1110   Median : 434   Median :23.00  
    ##            Mean   : 3002   Mean   : 2019   Mean   : 780   Mean   :27.56  
    ##            3rd Qu.: 3624   3rd Qu.: 2424   3rd Qu.: 902   3rd Qu.:35.00  
    ##            Max.   :48094   Max.   :26330   Max.   :6392   Max.   :96.00  
    ##    Top25perc      F.Undergrad     P.Undergrad         Outstate    
    ##  Min.   :  9.0   Min.   :  139   Min.   :    1.0   Min.   : 2340  
    ##  1st Qu.: 41.0   1st Qu.:  992   1st Qu.:   95.0   1st Qu.: 7320  
    ##  Median : 54.0   Median : 1707   Median :  353.0   Median : 9990  
    ##  Mean   : 55.8   Mean   : 3700   Mean   :  855.3   Mean   :10441  
    ##  3rd Qu.: 69.0   3rd Qu.: 4005   3rd Qu.:  967.0   3rd Qu.:12925  
    ##  Max.   :100.0   Max.   :31643   Max.   :21836.0   Max.   :21700  
    ##    Room.Board       Books           Personal         PhD        
    ##  Min.   :1780   Min.   :  96.0   Min.   : 250   Min.   :  8.00  
    ##  1st Qu.:3597   1st Qu.: 470.0   1st Qu.: 850   1st Qu.: 62.00  
    ##  Median :4200   Median : 500.0   Median :1200   Median : 75.00  
    ##  Mean   :4358   Mean   : 549.4   Mean   :1341   Mean   : 72.66  
    ##  3rd Qu.:5050   3rd Qu.: 600.0   3rd Qu.:1700   3rd Qu.: 85.00  
    ##  Max.   :8124   Max.   :2340.0   Max.   :6800   Max.   :103.00  
    ##     Terminal       S.F.Ratio      perc.alumni        Expend     
    ##  Min.   : 24.0   Min.   : 2.50   Min.   : 0.00   Min.   : 3186  
    ##  1st Qu.: 71.0   1st Qu.:11.50   1st Qu.:13.00   1st Qu.: 6751  
    ##  Median : 82.0   Median :13.60   Median :21.00   Median : 8377  
    ##  Mean   : 79.7   Mean   :14.09   Mean   :22.74   Mean   : 9660  
    ##  3rd Qu.: 92.0   3rd Qu.:16.50   3rd Qu.:31.00   3rd Qu.:10830  
    ##  Max.   :100.0   Max.   :39.80   Max.   :64.00   Max.   :56233  
    ##    Grad.Rate      Elite    
    ##  Min.   : 10.00   No :699  
    ##  1st Qu.: 53.00   Yes: 78  
    ##  Median : 65.00            
    ##  Mean   : 65.46            
    ##  3rd Qu.: 78.00            
    ##  Max.   :118.00

    plot(college$Private, college$Outstate)

![](ISLR_chap2_files/figure-markdown_strict/unnamed-chunk-4-1.png)

Now create histograms for quantitative variables in the dataset:

    par(mfrow=c(2,2))
    hist(college$Apps, breaks = 20)
    hist(college$Accept, breaks = 20)
    hist(college$Enroll, breaks = 30)
    hist(college$Room.Board, breaks = 50)

![](ISLR_chap2_files/figure-markdown_strict/unnamed-chunk-5-1.png)

Explore the data

    par(mfrow=c(2,2))
    plot(college$Expend, college$App)
    plot(college$S.F.Ratio, college$App)
    plot(college$P.Undergrad, college$Grad.Rate)
    plot(college$Expend, college$Grad.Rate)

![](ISLR_chap2_files/figure-markdown_strict/unnamed-chunk-6-1.png)

    plot(college$Private, college$perc.alumni)

![](ISLR_chap2_files/figure-markdown_strict/unnamed-chunk-7-1.png)

\#Exercise 9

Load in the Auto data set:

    auto <- read.csv("http://faculty.marshall.usc.edu/gareth-james/ISL/Auto.csv", header = TRUE, na.strings = "?")
    auto <- na.omit(auto)

The variables `origin` and `name` are qualitative. All other variables
are quantitative.

    summary(auto)

    ##       mpg          cylinders      displacement     horsepower   
    ##  Min.   : 9.00   Min.   :3.000   Min.   : 68.0   Min.   : 46.0  
    ##  1st Qu.:17.00   1st Qu.:4.000   1st Qu.:105.0   1st Qu.: 75.0  
    ##  Median :22.75   Median :4.000   Median :151.0   Median : 93.5  
    ##  Mean   :23.45   Mean   :5.472   Mean   :194.4   Mean   :104.5  
    ##  3rd Qu.:29.00   3rd Qu.:8.000   3rd Qu.:275.8   3rd Qu.:126.0  
    ##  Max.   :46.60   Max.   :8.000   Max.   :455.0   Max.   :230.0  
    ##                                                                 
    ##      weight      acceleration        year           origin     
    ##  Min.   :1613   Min.   : 8.00   Min.   :70.00   Min.   :1.000  
    ##  1st Qu.:2225   1st Qu.:13.78   1st Qu.:73.00   1st Qu.:1.000  
    ##  Median :2804   Median :15.50   Median :76.00   Median :1.000  
    ##  Mean   :2978   Mean   :15.54   Mean   :75.98   Mean   :1.577  
    ##  3rd Qu.:3615   3rd Qu.:17.02   3rd Qu.:79.00   3rd Qu.:2.000  
    ##  Max.   :5140   Max.   :24.80   Max.   :82.00   Max.   :3.000  
    ##                                                                
    ##                  name    
    ##  amc matador       :  5  
    ##  ford pinto        :  5  
    ##  toyota corolla    :  5  
    ##  amc gremlin       :  4  
    ##  amc hornet        :  4  
    ##  chevrolet chevette:  4  
    ##  (Other)           :365

We can quickly check the spread and average of each variable by
inspecting the range, mean and standard deviation:

    print("Range")

    ## [1] "Range"

    sapply(auto[, 1:7], range)

    ##       mpg cylinders displacement horsepower weight acceleration year
    ## [1,]  9.0         3           68         46   1613          8.0   70
    ## [2,] 46.6         8          455        230   5140         24.8   82

    print("Mean")

    ## [1] "Mean"

    sapply(auto[, 1:7], mean)

    ##          mpg    cylinders displacement   horsepower       weight 
    ##    23.445918     5.471939   194.411990   104.469388  2977.584184 
    ## acceleration         year 
    ##    15.541327    75.979592

    print("Standard deviation")

    ## [1] "Standard deviation"

    sapply(auto[, 1:7], sd)

    ##          mpg    cylinders displacement   horsepower       weight 
    ##     7.805007     1.705783   104.644004    38.491160   849.402560 
    ## acceleration         year 
    ##     2.758864     3.683737

Take a subset of the data by removing the 10th to 85th observations and
inspect the ranges, means and standard deviations of each variable:

    auto_subset <- auto[-c(10:85),]

    print("Range")

    ## [1] "Range"

    sapply(auto_subset[1:7], range)

    ##       mpg cylinders displacement horsepower weight acceleration year
    ## [1,] 11.0         3           68         46   1649          8.5   70
    ## [2,] 46.6         8          455        230   4997         24.8   82

    print("Mean")

    ## [1] "Mean"

    sapply(auto_subset[1:7], mean)

    ##          mpg    cylinders displacement   horsepower       weight 
    ##    24.404430     5.373418   187.240506   100.721519  2935.971519 
    ## acceleration         year 
    ##    15.726899    77.145570

    print("Standard deviation")

    ## [1] "Standard deviation"

    sapply(auto_subset[1:7], sd)

    ##          mpg    cylinders displacement   horsepower       weight 
    ##     7.867283     1.654179    99.678367    35.708853   811.300208 
    ## acceleration         year 
    ##     2.693721     3.106217

\#Exercise 10

Call the `MASS` library to load the `Boston` data set. The Boston data
set has 506 observations (neighbourhoods) and 14 features (housing
values and other variables).

    library(MASS)

Make some pairwise comparisons to inspect relationships between
variables in the data:

    pairs(Boston)

![](ISLR_chap2_files/figure-markdown_strict/unnamed-chunk-13-1.png)

The following predictors appear to be correlated with crime rate: lstat,

    sum(Boston$chas)/nrow(Boston)

    ## [1] 0.06916996
