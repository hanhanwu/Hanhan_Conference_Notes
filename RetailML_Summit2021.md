# Toronto Retail Machine Learning Summit 2021
April 20 ~ 21

## ML-Based Time Series Regression: concepts that can be learned from Demand Forecasting

* This is the talk given by BlueYonder, they focus on retail demand sensing. 
* Their main use cases
  * Replenishment: Order Optimization,  Avoid Out-of-Stock situations and waste
  * Pricing: Demand Shaping, Maximize Revenue/Profit
* [Find the complete PPT here][1]

### Learnings
* Bullwhip Effect: From supplier to customer, the uncertainty decreases
* Hierarchical Learning
  * They suggest to learn the effects at the appropriate hierarchical level (impact level)
    * Doesn't have to be 1 level up  
  * Because there can be autocorrelation in timeseries (ts), dependencies between features, feature-target dependencies, etc. To analyze at the higher level might help consider more factors
  * For example,
    * With "Promotion", we can:
      * Add the promotion flag as a feature
      * Learn at the production level
    * With "Pay Day Effect" , we can:
      * Learn at the location level
* Classical ML vs Deep Learning
  * Deep Learning is better to be used when all the info is available
    * This is why in later talks, companies like Amazon, Coveo who collects the data prefers to use deep learning
  * They later also suggest to use reinforcement learning to take advantage of the mutual impact between Retail side and Manufacturing side
  * The advantage of Classical ML is, they can handle missing info and flaxible for feature engineering using external factors and domain knowledge
* Feature Engineering suggestions
  * Always good to include domain knowledge
  * Seasonality, Trend, Events, Weather, Promotion types, price-demand elasticity features, product attributes and hierarchy (such as those from the product image, NLP), etc.
  * Some external factors can be inlcuded
* Target Correction
  * There are situations such as out-of-stock, markdown sales that makes target correct necessary, in order reduce the bias in demand forecast
  * The way they correct the target, for a specific product-location (SKU) on a given day
    * `demand = sales + markdown_demand = sales + 𝝰 * markdown_sales` 
      * `𝝰` depends on price reduction at hand and corresponding individual (i.e., each SKU-date) elasticity: exact dependency can be determined from observed data by means of supervised machine learning model 
* Their ts preprocessing suggestions
  * binning - to help remove outliers
    * equistatistics binning - to remove skewness (almost same # of observations per bin)
  * smoothing - help reduce variance
    * Instead of using the raw data, they remove high peaks
* [Categorical vs Mean Target Encoding][2]
  * Categorical Encoding: they often use that in retail, and prefer to use it for different individual ts and external features
    * Lower bias, higher variance 
  * Target Mean Encoding: they often used that in manufacturing, and prefer to use it for similar ts without much external features
    * Higher bias, lower variance 
* Autocorrelation
  * They suggest to avoid using target autocorrelation, such as exponential smoothing values. Because it's common that in ts, Yt-1 and Yt look like having autocorrelation, but in fact it's caused by temporal confounding
* Halo Effects
* 

[1]:https://drive.google.com/drive/folders/1qcw0ZQl64KhWmk_g6rbupFRKsV2O7kfC
[2]:https://towardsdatascience.com/why-you-should-try-mean-encoding-17057262cd0

