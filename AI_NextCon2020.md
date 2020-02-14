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

* 



[1]:https://github.com/Unity-Technologies/ml-agents
