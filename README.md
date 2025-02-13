# Konwinski Prize Strategy Guide
*Unofficial* guidance for competitors in the $1 Million USD Konwinski coding agent challenge.

Contest details: [kprize.ai](https://kprize.ai)

**Work In Progress :)** [Questions](https://github.com/raymyers/konwinski-prize-strategy-guide/issues/1) and PRs welcome.

## Getting Started

Download the contest [data](https://www.kaggle.com/competitions/konwinski-prize/data) and checkout Tong Hui Kang's [starter notebook](https://www.kaggle.com/competitions/konwinski-prize/discussion/553294) and [running note](https://www.kaggle.com/code/huikang/starter-notebook-select-patch-verify/comments#3082193).

Then you might like to start with a simple existing agent such as [Agentless](https://github.com/OpenAutoCoder/Agentless/tree/main) and work on plugging it into a model. No closed models or external API calls are allowed.

The best Open Weight coding model is currently DeepSeeker v3, but the runtime environment is probably too limited for it. We will update this when it's more clear of what models are viable. The starter above uses [Qwen2.5-Coder-32B-Instruct](https://github.com/QwenLM/Qwen2.5-Coder).

## Learning Path

Start by making sure you understand these terms.
### Background

* Large Language Models (LLMs) such as GPT-4, Claude 3.5 Sonnet, Llama 3.3
* Context window - the number of [tokens](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/understanding-tokens) that can be processed in one prompt response
* [Chain of thought](https://www.promptingguide.ai/techniques/cot)
* [ReAct](https://www.promptingguide.ai/techniques/react) (LLM tool use)
* [Retrieval Augmented Generation](https://en.wikipedia.org/wiki/Retrieval-augmented_generation)
* Fine-tuning
* [SWE-bench](https://www.swebench.com) - A benchmark on an agent's ability to complete realistic tasks on an entire code repository, taken from GitHub issues
* [SWE-bench+](https://arxiv.org/pdf/2410.06992) - A more rigorous evaluation dataset SWE-Bench+ without suspicious patches and solution leakages.
* [SWE-agent](https://swe-agent.com) - One of the first Open Source agents to perform well on SWE-bench, has a simple architecture that can be studied

### Agent design

* [Building effective agents](https://www.anthropic.com/research/building-effective-agents) by Anthropic
* [Don't sleep on single agent systems](https://www.all-hands.dev/blog/dont-sleep-on-single-agent-systems) by Graham Neubig, All Hands AI
* [How aider scored SOTA 26.3% on SWE Bench Lite](https://aider.chat/2024/05/22/swe-bench-lite.html) by Paul Gaithier, Aider
* [My mental model for building and using LLM-based applications](https://sourcegraph.com/blog/llm-mental-models) by Quinn Slack, Source Graph

### Fine-tuning and data

This competition is limited to Open Weight models, which are currently considered somewhat weak for this kind of agent. Fine-tuning may be a good idea.

* [Scaling data collection for training software engineering agents](https://nebius.com/blog/posts/scaling-data-collection-for-training-swe-agents) by Nebius, dataset of SWE-agent trajectories.
* [Smaller, Weaker, Yet Better: Training LLM Reasoners via Compute-Optimal Sampling](https://arxiv.org/pdf/2408.16737) by Hritik Bansal et al (October 2024).
* [Training Software Engineering Agents and Verifiers with SWE-Gym](https://arxiv.org/abs/2412.21139) by Jiayi Pan et al (December 2024).
