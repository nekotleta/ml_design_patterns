# Data Representatiom
Working with __inputs__ to create __features__

## For numerical inputs: 
 
* _Linear Scaling_ - improve speed by removing abnormal weight updates in gradient descent [code]. Scale [-1,1] makes error function more spherical. Moreover, scale [-1,1] offers the highest floating point precision. Another important reason for scaling is that some machine learning algorithms and techniques are very sensitive to the relative magnitudes of the different features. Lack of scaling also affects the efficacy of L1 or L2 regularization since the magnitude of weights for a feature depends on the magnitude of values of that feature, and so different features will be affected differently by regularization. 
	* Min-max scaling - [-1, 1]. -1 == min, 1 == max.
	* Clipping - [-1, 1], -1 and 1 - "reasonable" values; outliers are -1 and 1.
	* Z-score normalization - the scaled value is unbounded, but does lie between [–1, 1] the majority of the time (67%, if the underlying distribution is normal).
	* Winsorizing - 10th and 90th percentile then min-max scaling.

Min-max and clipping tend to work best for **uniformly distributed data**, and Z-score tends to work best for **normally distributed data.**

* _Nonlinear Transformation_ - using before Scaling
	*  Logarithm
	*  Sigmoid
	*  Polynomial expansions (square, square root, cube, cube root, and so on)
	*  [Box-cox transformation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.boxcox.html) - lambda controls the “heteroscedasticity"
	*  Histogram equalization - approach is to bucketize the number of views (quantiles, as usual), choosing the bucket boundaries to fit the desired output distribution

## For categorical inputs: 

* _One-hot enconding_
* _Dummy coding_ - compact representation of one-hot encoding (one variant or missing will be all zeros); preferred in statistical models
* _Counting_ - number of occurrences of each vocabulary item (multi-hot encoding if counts are 0 or 1)
* _Relative frequency_ - _counting_ divided





__Pretty links:__
1. https://www.analyticsvidhya.com/blog/2020/08/types-of-categorical-data-encoding/
2. https://scikit-learn.org/stable/auto_examples/preprocessing/plot_all_scaling.html
