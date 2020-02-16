# AI NextCon 2020 💡

## 2020-02-12 🌺
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

## 2020-02-14 💝
As you can see, it's Valentine's day and I was sitting in the workshop whole day. Something was wrong with Google Cloud lab environment, my account wwas dead, so it took me some time to move everything to move to my google colab and start over. Fortunately, finally finished the workshop.

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
