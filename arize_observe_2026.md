# Arize Observe 2026

## Overall
* Finally attended Robert's talk in person! Robert is the cuttest guy in the universe 💖! How I wish this year there will be more chances to meet him in person ✨.
* Hmmm, this conference is ok, I collected some info might help our work. Sometimes I'm wondering whether some company never tell you the truth or even direct you to the wrong direcion on purpose in this type of conference.

## Commonly Mentioned by Multiple Companies
* ✨ Platform teams care more about pre-deployment testing
  * teams like Wells Fargo, Workday platform teams
  * data privacy
    * e.g. sensitive data leakage
  * security
    * e.g. prompt injection
    * e.g. agent goal drift ro unsafe/unintended paths without human oversight
  * failures
    * e.g. silent propagation of failed API calls across multi-step agentic workflow
  * agent output quality
    * e.g. hallucination
  * costs
    * e.g. infinite execution loops --> significant cost --> erosion of user trust
  * Claude can't help --> scaling challenges
    * they want automated tests rather than using claude to find problems for every agent 
* What to monitor
  * teams like Microsoft, Arize
  * agent perforamnce dashboard
  * security
  * cost
* Multi-agent evaluation is challenging
  * teams like Salesforce, BAND
  * timestamp can be wrong
  * hard to replay the workflow cuz the log doesn't record everything, such as human-in-the-loop can happen in the middle but human-AI interaction is not tracable
* Instant alert is helpful
  * teams like Uber, Microsoft
* Root Cause Analysis
  * Multiple audiences brought up root cause analsis and continuous improvement are what they need

## Worthy To Note
* ✨ Microsoft Foundry
  * Demo: https://ai.azure.com/home
  * This tool builds agent, enables rubrics (metrics) for evaluation and improvememt --> its goal is for building agents with continuous improvement capability
  * To deply the agent to production (non-Azure env), it requires OpenTelementry Agent ID
  * key contact: https://www.linkedin.com/in/sebastiankohlmeier/
  * I tried on VSC, can't really create the agent for me now, but worthy to pay attention to its updates, it just got released in Microsoft Build this week
* Salesforce
  * The director of engineering at Agentforce seems lack of real production experience, he doesn't really know the painpoints in production, although what he talked sounds right, those are general info can be collected from ChatGPT
  * What they care about
    * reliability for both pre-deployment and post-deployment
    * framework + data + metrics
    * able to handle the challenges in multi-agent during the evaluation ✨
* Arize Demo
  * ✨ dynamic prompt for judging is a good idea, comparing with static prompt for llm-as-judge
  * ✨ Harness-as-Judge: use agent to evaluate agent, you just tell what to test, let the harness handles it
    * the idea is very cool, I think they went to far at this moment, currently lots of agents are either not built/deployed, deployed ones still have production concerns, Arize is not showing strong capability to evaluate agents even manually, using another agent system to do evaluation agents, maybe only investors will love the idea...
  * agent fleet evaluation 

