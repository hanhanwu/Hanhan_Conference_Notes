# MLConf 2019

Hey, it's San Francisco! Havn't been here for many years, and till it's very windy here. This is the conference thta focuses on machine learning application, since I'm interested in Applied Data Science, it's a good opportunity to come and see what others are doing in the industry.

## Uber Machine Learning
* The most impressive thing is how they form data scientice teams. They need full stack data scientist, who can build data science model and can also develop machine learning tools & platform. Developers need to have data science knowledge. This make sense. When I was chatting with their director, mentioned the discrepency we have to deal with between DS model and production platform, she said, if we really want to productionize DS model, have to work with developers who have DS knowledge, otherwise no matter how good the knowledge sharing will be, problems will keep happening later and cannot really put DS model into production. 
* They have so many time series problems, besides using <b>sliding window</b>, they also have <b>expanding window</b>, which keeps all the previous data as the training data, so that when new testing data comes in, the training data is also growing.
  * The window size of expanding window really depends, since some time series problem gets better results with most recent data, longer history doesn't always bring better results.
* [Uber Open Source][1]
  * [Uber Open Source GitHub][3]
* [Uber Engineering][2]

## Intention Detection
* There are multiple projects such as those in Airbnb, Pandora will get short messages from users, then the recommendation system will provide suggestions for the users. They type projects often include intention prediction. Since they will be many mismatch in words caused by autofill, typo, wrong speech detection, etc.
* In Airbnb
  * They built the offline model which requires offline scoring once a day...
  * They also do A/B test to compare the model they built with the rule based system
  * Most of their machine learning models only got neural or negative results...
  * I think Airbnb speaker is really honest!
* In Pandora project
  * They divided user queries into:
    * Known item query, such as a specific song
    * Thematic query, such a category of songs
    * Open ended query
  * When providing recommendations for open-ended queries, they categorize music into different categories (bandit), and do multi-bandit (similar to multi-labeling) recommendation.

## Netflix Recommendation System
* When the speaker said, Netflix is everywhere except in China, I just found it's so funny :D
* Of course the main logic is collaborative filtering
* They mentioned [Variational Autoencoders for Collaborative Filtering][4]
  * [Variational Autoencoder][5]
  * "In neural net language, a VAE consists of an encoder, a decoder, and a loss function. In probability model terms, the variational autoencoder refers to approximate inference in a latent Gaussian model where the approximate posterior and model likelihood are parametrized by neural nets (the inference and generative networks)", referenced from [VAE tutorial][6]
* Because Netflix has gigantic amount of data, they suggest to use <b>Incremented trained deep learning model</b>, with a fully trained model, later you just need to add additional nodes and parameters. This solution is to deal with fast changing data and long time trained model. Much better than reconstructed model.

## Uncanny Valley of Machine Learning
* They found, more human labeling not always increase machine learning prediction results. When the labeling reached to a certain amount, not only thr performance dropped but also the decision making time became longer. Therefore, when applying machine learning in some serious situations, such as judiciary cases, it can be dangerous. I like they can not only disclose the problems but also provide suggestions with reasons.
* Suggested Solutions
  * Build simulators for integrated machine learning & human decision making system, to evaluate whether ML will bring more benefits. If not, better not to integrate the system with ML
  * Relabel bad labels, with ML
  * Release ML system that human won't pay attention to. Since it seems that, when human beings know that machine learning has been used into the system, they are more likely to create wrong labels.
  * HCI, DS, AI, UX, Psychology, etc. should work together
  * Pay attention to the policy behind
  * Having metrics that will help false predicted victims
  
## PerceptiLabs - A ML Platform
* I like their UI design, expecially after dragging and running each step, there's a visualized result. They type of step-by step DS visualization can help not only data scientists but also stakeholders/clients to understand how ML models work better.
* [Demo][7]
* [Download the tool][8]


## Summary
* My favorite part of 1-day conference is, you don't need to walk between conference rooms, and will get more chance to chat with different people without moving too much. It's a good learning exprience and networking opportunity.
* Although it's also very tired, since everything to be finished within 1 day is intense.
* Maybe next time, choose the one doesn't need to take the flight!


[1]:https://eng.uber.com/category/articles/open-source-articles/
[2]:https://eng.uber.com/
[3]:https://github.com/uber
[4]:https://arxiv.org/pdf/1802.05814.pdf
[5]:https://github.com/altosaar/variational-autoencoder
[6]:https://jaan.io/what-is-variational-autoencoder-vae-tutorial/
[7]:https://www.youtube.com/channel/UCYAWJ3u8N6E6OI7GjIUe-Iw
[8]:https://perceptilabs.readme.io/docs/download-1
