# AI NextCon 2020 💡

## 2020-02-12 ~ 2020-02-13 🌺
My ticket has 2 days conference and 2 days workshop. It seems that it's a conference cares about computer vision a lot. But indeed, there are many creatives ideas have been done by computer vision in the industry. I like those algorithms talks, because those speakers talk deeper in machine learning algorithms in an easy-to-understand way, and also help you understand the whole process about how they solve the problems. What's more, most of them are Chinese! 💐

### Simulations - The New Reality of AI
The speaker came from Unity, a game company. He was talking about how do they use AI in the game industry, and why simulation is necessary for AI.

* With reinforcement, they could train the game characters as super human, in order to help game developers to figure out whether the game could make people at different level to have fun.
  * Although I'm wondering, how could they record necessary data for simiulated character at each level, in order to improve the game design. And after that character has become the super human, are they able to roll back, otherwise most of the time, they only know how does super human play the game.
* With simulation, they could change many things in the game, such as background color, mimic player's behavior, etc., so that they could test how the simulated character will react to the changes when playing the game.
* [Unity's ML-Agents][1]


### Patterns & Practices - Lessons Learned From Azure ML Customers
The speaker came from Microsoft Azure. He mentiones 7 patterns in AI problems, I like the suggestion about how Data Engineers, Data Scientists and ML Engineers should work together to make the dymamic machine learning pipeline automatic.

* Data Engineers focus on generating data catalog from the data lake, Data Pipeline
* Data Scientists focus on Model Training Pipeline
* ML Engineers focus on Deployment Pipeline.
* The collaboration forms a cycling process since machine learning should keep improving. I like the part when he mentioned, ML Engineers should send feedkack data to the data lake and will be parsed by the Data Engineers, so that Data Scientists will get insights on how to improve the models.
* Azure FPGA
  * "FPGAs make it possible to achieve low latency for real-time inference (or model scoring) requests. Asynchronous requests (batching) aren't needed. Batching can cause latency, because more data needs to be processed. Implementations of neural processing units don't require batching; therefore the latency can be many times lower, compared to CPU and GPU processors."

### AI to Empower AI (Agent Intelligence) 💖
This is one of my favorite talk, maybe also because the speaker is a lead I admire. The company is called Compass, a real estate company, never thought computer vision can do so much creative work.

* Services they do with computer vision:
  * With computer vision, they help dress up an empty room, so that real estate agents could dress up the room in that way to improve sellings.
  * Image Search
  * Classify images and search for images based on similarity score
    * With [HNSW][2], it provided most accurate results so far
    * With NGT-OONG, it's the fastest algorithm for them so far
      * I found [NGT][3]
  * Filling missing frames in the video to smooth out the slow motion of room exhibition
* Other AI Services:
  * Recommendation & Ranking
  * Similarity, Classification, Ranking
  * Search suggestion
  * Recommend price, in order to reach to the max demand
* Their major clients are real estate agents, then agents' clients
* The way they get agents' feedback is still majorly through product managers communication with the agents, there are some data analysis too.

### AI as a Service, Autonomous Learning
The speaker is the CEO from [RealityEngine.ai][4]. It seems that from her perspective, deep learning can do anything, includeing those what classical machine learning is good at, sounds like you need to learn more about deep learning. The company service suggests you the neural network architecture for you based on your situation (this idea is cool).

* The company majorly is helping you to train with less data.
* Methods to train with less data in NN
  * Data Augmentation
    * Modify eaisting input data and use the results as new input data
      * Such as use rotated images as new image input
    * With the help of GANs (Generative Adversarial Networks) to add more input
  * [Meta Learning][5]
    * Learning to learn
    * Train on meta learner, then used the trainded meta learner to train other models.
  * Transfer Learning
    * Retrain pre-trained model
    * Train a model on a very large dataset -> Then customize to each client by retraining the first layer with client's data
  * Incorpporate Logic Rules in Neural Network
    * This is what this company uses
    * A user searches for neural architecture -> The company suggests the best neural net -> The user tweak it for their own needs
    
### [An Efficient Bandit Algorithm for Real Time Multivariate Optimization][8]
* The speaker came from Amazon research group.
* Optimization is commonly employed to determine the content of web pages, such as to maximize conversions on landing pages or click-through rates on search engine result pages. Here they focus on multivariate optimization of interactive web
pages.
* MULTVARIATE TESTING ALGORITHM
  * Thompson Sampling 
    * Thompson sampling selects a layout proportionally to the probability of that layout being optimal conditioned on previous observations.
  * Hill climbing optimization
    * Add this optimization function in the above Thompson Sampling algorithm.
    * They return the best layout among the S hill climbs, resulting in a maximum of SKN layout evaluations.
* During the evaluation stage, they also used the optimal results from thompson sampling to compare with the best results from A/B tests.

### Getting Data Ready with Delta Lake
* [Databricks Delta Lake][9]
* In a distributed system, to Delete/Update, they all need to create a new table for copying before making changes, then delete the old table and rename the new table. Merge is more complex. But with Delta Lake, just 1 query will make these possible.
* The experience of updating the data is more smooth.
* It also keeps your changes for rollback purpose.

### Modern Speech Recognition, Hybrid vs. End-to-End
* In Facebook, there is video caption, Oculus and Portal phone call commands, so facebook cares about speech recognition.
* Hybrid Approach
  * Accoustic Model
    * Audio input -> Sound units, it tells the sound.
    * Architecture: LSTM, CNN, etc.
  * Pronouncation Model
    * Sound units -> Words
  * Language Model
    * Words -> Phrases
* End-to-End Approach
  * Audio input -> 1 Single NN model -> Output
* In practice so far, hybrid approach is more reliable and competitive, which one to use is application dependent.
* Hybrid vs. End-to-End

| | Hybrid | End-to-End |
| --- | --- | --- |
| Accuracy | Yes | Yes |
| Simplicity | No | Yes |
| Flexibility | Yes | No |
| Debuggability | Yes | No |
| Training Speed | Yes | No |
| Inference Speed | No | Yes |
| Data Requirement | Yes | No |
| Space Requirement | No | Yes |

* When they are doing transformer acoustic model, they use academic benchmark [Librispeech][10]

### [Deepfakes][11]
* There are 2000 faces, so many pairwise models. 1 day can only train 1 pairwise model. So it takes very long time to train the model.
* `wP = TP/(TP + αFP)`, weighted precision is their prefered metrics, `α` normally is larger than 1 and is decided based on distribution or other factors.

### Time Series Forecasting from Statistical Methods to Deep Learning
* Statistical Methods
  * Pros
    * Simple to understand
    * Only need historical data
    * Need deep understanding of data
    * Can handle large amount of data
    * High iterpretability
  * Cons
    * Difficult to consider correlation between series
    * Hard to scale up, not easy for long term sequence
    * Hard to include other features, such as price, category, etc.
    * Feature engineering is needed (I personlly think, feature engineering is necessary in the industry)
* Classical Machine Learning
  * Lag 1 is not what happens in reality, which also makes k-fold difficult.
  * Feature Engineering is needed for hand craft seasonality, trend, categorical features, etc.
* Deep Learning
  * Universal function approximator
  * No extensive feature engineering
  * Not much domain knowledge is required
  * Can deal with unstructured data
  * But there can also be tons of changes in the architecture
* They are using [Dilate Convolution][12], which has similar idea as [WaveNet][13]. The basic idea is, there are multiple layers in the NN, upper layers will skip soe nodes in order ot get long term correlation.
* Statistical Methods vs. Classical Machine Learning vs. Deep Learning

| Time Series Type | Deep Learning | Classical Machine Learning | Statistical Time Series |
| --- | --- | --- | --- |
| Single/Multiple Time Series | Not enough data to train | Might not good | Easy to understand, easy to try |
| Long Time Series/Lots of Correlated Time Series | Able to learn long term dependencies; end-to-end solution | Able to learn coplicated relation, need feature engineering | Some simple solution |
| Lots of time series + other features | No feature engineering, able to learn complicated correlation | Able to learn complicated relation, need feature engineering | Cannot learn non-linear effect, hard to use unstructured data |

## 2020-02-14 💝
As you can see, it's Valentine's day and I was sitting in the workshop whole day. Something was wrong with Google Cloud lab environment, my account was dead, so it took me some time to move everything to my google colab and start over. Fortunately, finally finished the workshop.

* [Tensorflow 2.0 Use Case][6]
  * Feature engineering and neural network when using Tensorflow 2.0
  * A simple Google BigQuery to query the public data
  * How to use Tensorflow [tf.dataset][7] for data processing
  
## 2020-02-15 😊
It's the last day workshop and it's Saturday today. The workshop starts at 9am, not sure why didn't hear the alarms this morning and when I woke up, it was more than 10am. I had an apple for breakfast, then drove to downtown Bellevue, had some nice food and had enough coffee in order to drive back. Filled the gas for my car. Visted a nice book store to check books in penetration testing. Finally drove back. In a word, did everything except attending the workshop. But the workshop today was held by Microsoft, consider all of the workshops that disappointed me a lot came from Microsoft, feeling better about my absence.

[1]:https://github.com/Unity-Technologies/ml-agents
[2]:https://github.com/nmslib/hnswlib
[3]:https://opensource.com/article/19/10/ngt-open-source-library
[4]:https://realityengines.ai/about
[5]:https://lilianweng.github.io/lil-log/2018/11/30/meta-learning.html
[6]:https://github.com/hanhanwu/Hanhan_COLAB_Experiemnts/blob/master/tensorflow2_training_day1.ipynb
[7]:https://www.tensorflow.org/api_docs/python/tf/data/Dataset
[8]:https://arxiv.org/pdf/1810.09558.pdf
[9]:https://delta.io/
[10]:https://github.com/kaldi-asr/kaldi/tree/master/egs/librispeech
[11]:https://github.com/deepfakes/faceswap
[12]:https://towardsdatascience.com/review-dilated-convolution-semantic-segmentation-9d5a5bd768f5
[13]:https://github.com/ibab/tensorflow-wavenet
