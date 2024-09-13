# The AI Conference 2024


## Enabling AI in Industry
* Thoughts on adopting AI
  * Training is important
    * <b>Reapeated & practical training</b> format is more effective, making the training related to people's day time jobs.
  * To drive the trust, need to make people feel they're parnering with you to create solutions
  * Need to make people feel being rewarded rather than feeling afraid of being replaced
  * Need to think about the whole system redesign with adopting the AI solutions
 
* Intuit's GenOS Architucture
  * According to Merrin, it's handling hundreds of use cases now, and it's built in 1.5 years
  * Besides, they also have product monitoring 
 
<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/Intuit_GenOS1.jpeg" width="780" height="600" />
</p>
 
<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/Intuit_GenOS2.jpeg" width="780" height="600" />
</p>


## AI Powered Tools
* 🌺 [Otter.ai][5], I saw lots of people uses this tool to take conference notes in real time, looks quite efficient
* [Llama Index][3] enables querying form large amount of info more efficiently
  * [It has many integrations][4]
* 🌺 [Phoenix][9] traces LLM application runs, to help you understand what's happening below the surface, which can be significant for LLM evaluation
  * Its company Arize has more AI productionization experience in the industry
  * [Check its quickstarts][12] for Tracing, Evaluation, Inferences, Datasets & Expriments
  * By contrast, [LangGraph][11] and [Llama Index's Workflow][13] are event base
* [Llama Index's Workflow][13] allows you to build a workflow that's reusable and modularized
  * [for example][14]
* 🌺 [Stability AI][6], it provides open source image, video, language models (has specific Japanese trained model)
  * [Check its models][7]
  * [Generative models github][8]
* [Andi search][1], search without ad or spam.
  * Hmm, I tried some search, not that accurate....


## Lessons Learned from AI Practitioners 
* If customers need more accurate results, such as BI reports, building AI Assistant is better than building AI Chatbot, because current AI technique is not mature enough to handle
* Learned from Doordash, to evaluate large amount of results from LLM
  * Having a confidence score threshold to automatically pass high confidence results
  * For results didn't pass the threshold, can have human in the loop
* Lessons learned from Square's AI Transformation
  * <b>Before fine tuning or model improvement, show your use case can bring values to the business first</b>
  * Main methods to improve modle performance:
    * prompt engineering
    * input quality
    * evaluation on model accuracy and model realiability
      * having human in the loop to provide feedbacks (thumbs up/down, comments)   
  * At the end of your evals work, focus on the most complex queries' performance
* Lessons learned from OpenAI
  *  


## Startup Tips
* Investors' Focus
  * Showing the AI solution is really making the impact in a certain industry, (such as improved x efficiency)
  * Able to see the evidence that proves the impact is effective
  * How did you lower the cost, or able to spend the foundings effectively
  * Beyond LLM
  * Creativity & the ability to make the product come true
  * Having the roadmap for continuous improvement
  * How's your MLOps, the potential to go big
    * Because AI productionization is rare (balancing scaling and cost is challenging)
  * The creativity in business, marketing, and how you can resonate with people

* My Favorite Demo Format
  1. Share background (explain why)
  2. Describe the user groups (what)
  3. Share impact already made or extimated impact with evidence
  4. Share achieved results, collaboration, current progress


## Future Opportunities
* [Ray Summit][2]
* Join [AI Alliance][10] to get more resources and opportunities.


## Questions to Think 🤔
* Doordash uses LLM ot generate the data, can we also use LLM to generate data? Such as cross selling product pairs?
* How to use AI to streamline the process of changes?

[1]:https://andisearch.com/
[2]:https://raysummit.anyscale.com/flow/anyscale/raysummit2024/landing/page/eventsite
[3]:https://docs.llamaindex.ai/en/stable/getting_started/concepts/
[4]:https://llamahub.ai/
[5]:https://get.otter.ai/interview-transcription/?utm_source=google_ads&utm_medium=search&utm_term=automatic%20note%20taking%20app&utm_campaign=search-prospecting-consumer-nonbrand-transcriptionv2-exact&hsa_acc=6047463090&hsa_cam=20014220152&hsa_grp=149129772198&hsa_ad=657350971384&hsa_src=g&hsa_tgt=kwd-661171101282&hsa_kw=automatic%20note%20taking%20app&hsa_mt=b&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=CjwKCAjwooq3BhB3EiwAYqYoEvS_2E4VZdACghBQNsNVfsA4gvPrT717byHC9azGiL3EB_-5JmwWABoCKrEQAvD_BwE
[6]:https://github.com/Stability-AI
[7]:https://stability.ai/
[8]:https://github.com/Stability-AI/generative-models
[9]:https://github.com/Arize-ai/phoenix
[10]:https://thealliance.ai/
[11]:https://langchain-ai.github.io/langgraph/#example
[12]:https://docs.arize.com/phoenix#quickstarts
[13]:https://docs.llamaindex.ai/en/stable/module_guides/workflow/
[14]:https://docs.llamaindex.ai/en/stable/examples/workflow/react_agent/
