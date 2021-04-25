# Toronto Retail Machine Learning Summit 2021

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
  * 2 similar products A, B. Prod A might normally have lower prices and more stable demand than prod B. Then Prod B has a promotion people decided to choose prod B instead of A during the promotion time.
  * They suggest to consider to have Product Relationship as features for long time forecasting. This is also the drawback of NN, since NN treats different products nindependently.
  * They also built a matrix to measure the effects between each product pair.
* Order Optimization
  * They sugest to plot the full PDF of demand forecasts
    * Choose high quantile for ordering might lead to over-stock
    * Choose low quantile for ordering might lead to under-stock
* Simpson's Paradox
  * Bad overall but good in every group
* Causal Inference
  * Confounding: Causal effect of X on Y confounded by common cause Z  
  * Purpose: it's the prediction of individual causal effect using observational data
  * Approach 1: predict P(X|Z), propensity score
  * Approach 2: `P(Y|do(X)) = sum(P(Y|X,Z)*P(Z)) = sum(P(X,Y,Z=z)/P(X|Z=z)`
  * Approach 3: Check prediction differences by having X and without X


## [In-session Personalization][4]
* This talk was given by Coveo. They are among the top 3 AI research in ecommerce.

### Learnings
* They are trying to predict what does the user want (user intention) within a website sesion.
* They have built "product2vec", it's product embeddings which is similar to the idea of word2vec
  * Similar products are closer together
  * This allows them to build the multi-dimensional product space where they can find the interactions between products in an unsupervised way
  * When there is user interaction, they can narrow down the product search space
* Suggestions in learning low-count products
  * New products can be lack of user interactions and therefore to be lack of data
  * They learn new products by mapping them to popular products
    * using the product similarities in the product space
  * They keep track of super wrong predictions to look for further improvement
    * To track those cases, they use methods such as cosine distance between y_pred and y_true
* Researches about how much info within a session could help user intention pprediction   
  * User behaviours such as number of mouse clicks, etc.
  * The legnth of a session
    * If a user left the session too long when he returns back it will be a new session, the former session contains little info. And sometimes they will learn sessions close-by together when some of them have little info
* [Their code][3] and [data][5]
  * Each observation is a sequence of info within a session
  * How to build prod2vec space
  * How to improve model performance on low_count product
  * Query scoping using MLP

## Personalization in Retail
* The talk was given by Amazon, the concept was simple, and sounded more like seeling this tool called "AWS Personalize"....
* [About AWS Personlaize][6], the main methods are:
  * collaborative filtering
  * context based filtering which allows you to apply business rules for the filtering
* [Retail Demo Store][7] and [All the workshops' code][8]



[1]:https://drive.google.com/drive/folders/1qcw0ZQl64KhWmk_g6rbupFRKsV2O7kfC
[2]:https://towardsdatascience.com/why-you-should-try-mean-encoding-17057262cd0
[3]:https://github.com/jacopotagliabue/retail-personalization-workshop/blob/main/ml_retail_workshop_for_personalization.ipynb
[4]:https://github.com/jacopotagliabue/retail-personalization-workshop
[5]:https://github.com/coveooss/SIGIR-ecom-data-challenge
[6]:https://aws.amazon.com/blogs/machine-learning/selecting-the-right-metadata-to-build-high-performing-recommendation-models-with-amazon-personalize/
[7]:https://github.com/aws-samples/retail-demo-store
[8]:https://github.com/aws-samples/retail-demo-store/tree/master/workshop
