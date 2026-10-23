# AI Agent Conference 2026

Now I prefer neep tech conversation with people who have hands-on experience for real customers in the industry. Most of these talks are not helpful to me, either they were given by non-tech people who are mainly advocating for their company or they were given by engineers from some giant company but actually the work they have done is, so so.... I no longer want to attend this type of conference any more...

![AgentCon image 1](image/agent_con1.jpg)

* https://open-sandbox.ai/
* Agent Skills: https://github.com/addyosmani/agent-skills
  * Create your own skill if the repo doesn't have the template to support your reusable workflow for your coding agent, describing your **steps, rules, and expected output** in `SKILL.md`.


![AgentCon image 2](image/agent_con2.jpg)

### Tips to use Jev from Langchain

![AgentCon image 3](image/agent_con3.jpg)

* Personal notes
  * Jev's confidence score is NOT the probability of the answer. It means "How strongly does this distribution favor one answer?"
  * Calibration is checked across groups of predictions by comparing probabilities with observed frequencies.
    * For example, 1,000 different messages that Jev assigns approximately 80% probability of belonging to Billing:
      * Around 800 actually belong to Billing → well calibrated around 80%.
      * Only 600 belong to Billing → overconfident.
      * Around 950 belong to Billing → underconfident.
