# UC Berkeley Agentic AI Summit 2026

UC Berkeley is very good at making money. The ticket was $499 ~ $699 per person, there were 2000+ attendees. No breakfast, no coffee at all... They were still selling tickets after selling out and told you to arrive earlier to be able to enter the main stage...

## Opportunities
* Snorkel's open benchmark grants: https://benchmarks.snorkel.ai/, they're especially interested in legal benchmark data


## Open Sources
* Agents' Last Exam: https://agents-last-exam.org/
  * paper: https://arxiv.org/pdf/2606.05405
  * ALE evaluates whether an AI system can complete realistic, multi-step tasks as an autonomous agent. Any agent that can interact with tools (browser, terminal, APIs, files, etc.) can, in principle, be evaluated.
  * Whether it can be used in enterprise agent system depends, if the agent focuses on specific workflow, may not be suitable
* AgentBeats: https://agentbeats.dev/
  * AgentBeats is a platform and evaluation framework for building, running, and sharing agent benchmarks. They provide:
    * Easy instantiation of standardized LLM agents with built-in A2A and MCP support
    * Reproducible multi-agent evaluation in rich simulation environments
    * Multi-level interaction tracking for evaluation insights and leaderboard integration
* CyberGym: https://github.com/sunblaze-ucb/cybergym
  * CyberGym is a large-scale, high-quality cybersecurity evaluation framework designed to rigorously assess the capabilities of AI agents on real-world vulnerability analysis tasks.
* CyberGym E2E: https://github.com/sunblaze-ucb/cybergym-e2e
  * The agent receives only source code, and must find the vulnerability, generate a proof-of-concept (poc.bin), and produce a patch (fix.patch).
* ExploitGym: https://github.com/sunblaze-ucb/exploitgym
  * ExploitGym is a large-scale, realistic benchmark built from real-world vulnerabilities across userspace programs, Google's V8 engine, and the Linux kernel, designed to evaluate AI agents' ability to develop exploits.  


## Notes
* Reliable Agent Systems from Scale AI
<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale1.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale2.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale3.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale4.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale5.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale6.jpg" width="780" height="600" />
</p>

* Enterprise Agent Systems from Scale AI
<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale_e_1.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale_e_2.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale_e_3.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/scale_e_4.jpg" width="780" height="600" />
</p>

* Redis, spec & context helps improve agent systems --> summarize high level stats and what's happening
<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/redis1.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/redis2.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/redis3.jpg" width="780" height="600" />
</p>

* Snorkel Benchmark Creation
<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/snorkel1.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/snorkel2.jpg" width="780" height="600" />
</p>

* Google AI Governance
<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC1.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC2.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC3.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC4.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC5.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC6.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC7.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC8.jpg" width="780" height="600" />
</p>

<p align="left">
<img src="https://github.com/hanhanwu/Hanhan_Conference_Notes/blob/master/image/GC9.jpg" width="780" height="600" />
</p>

* About agents' self improvement
  * let the agent optimize the cost itself by looking at its traces
  * enable agent's auto research to improve agent's performance
* Tips to improve agent perforamnce
  * provide a cheatsheet for LLM
  * tell LLM "Don't overthink"
* Other tips
  * Don't let agents cheat --> build a cage
  * Don't make decisions on sand --> keep a record
