# Konwinski Prize Strategy Guide
*Unofficial* guidance for competitors in the $1 Million USD Konwinski coding agent challenge.

Contest details: [kprize.ai](https://kprize.ai)

**Work In Progress :)** [Questions](https://github.com/raymyers/konwinski-prize-strategy-guide/issues/1) and PRs welcome.

## Learning Path

Start by making sure you understand these terms.

* Large Language Models (LLMs) such as GPT-4, Claude 3.5 Sonnet, Llama 3.3
* Context window - the number of [tokens](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/understanding-tokens) that can be processed in one prompt response
* [Chain of thought](https://www.promptingguide.ai/techniques/cot)
* [ReAct](https://www.promptingguide.ai/techniques/react) (LLM tool use)
* [Retrieval Augmented Generation](https://en.wikipedia.org/wiki/Retrieval-augmented_generation)
* [SWE-bench](https://www.swebench.com) - A benchmark on an agent's ability to complete realistic tasks on an entire code repository, taken from GitHub issues
* [SWE-agent](https://swe-agent.com) - One of the first Open Source agents to perform well on SWE-bench, has a simple architecture that can be studied

## Blogs on design

* [Building effective agents](https://www.anthropic.com/research/building-effective-agents) by Anthropic
* [Don't sleep on single agent systems](https://www.all-hands.dev/blog/dont-sleep-on-single-agent-systems) by Graham Neubig, All Hands AI
* [How aider scored SOTA 26.3% on SWE Bench Lite](https://aider.chat/2024/05/22/swe-bench-lite.html) by Paul Gaithier, Aider
* [My mental model for building and using LLM-based applications](https://sourcegraph.com/blog/llm-mental-models) by Quinn Slack, Source Graph
