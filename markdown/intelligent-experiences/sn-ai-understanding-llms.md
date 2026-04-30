---
title: Understanding large language models \(LLMs\)
description: Large language models are generative, not retrieval-based. They create responses dynamically using probability, which means you can’t expect identical outputs every time. This variability is a feature, not a bug, because it allows for flexibility, creativity, and adaptability.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-20"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI implementation, Enable AI experiences]
---

# Understanding large language models \(LLMs\)

Large language models are generative, not retrieval-based. They create responses dynamically using probability, which means you can’t expect identical outputs every time. This variability is a feature, not a bug, because it allows for flexibility, creativity, and adaptability.

## How LLMs work

Large language models \(LLMs\), like ChatGPT or Copilot, are advanced AI systems that are trained on massive amounts of text to understand and generate human-like language. They build a statistical model of language, so they don’t store fixed answers like an encyclopedia. When you ask a question, the model generates an answer one word \(or token\) at a time, choosing the next most likely word based on probabilities learned during training. This prediction process makes them powerful, but it's also why they are non-deterministic. This means the system does not always produce the exact same result \(output\) for the same prompt \(input\).

## Why results may vary

Even if you provide the same question or prompt twice, the response can differ. Here’s why:

-   **Probabilistic sampling**

    The model doesn’t always pick the single most likely word. It samples from several likely options. This introduces variation.

-   **Temperature settings**

    Temperature controls randomness, and this internal parameter varies among LLM models. A higher temperature delivers more creative responses, while lower temperatures tend to be more repetitive.

-   **Multiple valid answers**

    Many questions have more than one correct way to explain something. The model may choose different phrasing or emphasis each time.

-   **Context sensitivity**

    Tiny changes in punctuation or prior conversation can shift the output.

-   **System-level factors**

    Hardware concurrency, floating-point math, and backend updates can introduce slight variations, even when everything else is fixed.


For example, think of it like rolling dice to pick words. When you ask a question, the model doesn’t follow a fixed script. Instead, it looks at many possible next words and picks one based on probabilities—like rolling weighted dice. The dice are weighted toward the most likely words, but there’s still a chance for variation. If you roll again \(ask the same question\), you might get a slightly different sequence, even though the rules didn’t change. This randomness is intentional. It makes the model flexible and creative, rather than rigid and repetitive.

For more information about supported LLM models, see [Large language models on the ServiceNow AI Platform](../../general/concept/exploring-large-language-models.md).

## Variations in search

The ServiceNow AI Platform® offers a variety of search tools, which may return different answers for the same or similar searches. This disparity in results is expected. For more information, see the following topics:

-   [Discrepancies when using different AI search tools](../../general/concept/aisearch-differences.md)
-   [Search result disparities between AI Search and Now Assist search features](https://www.servicenow.com/docs/access?context=search-disparities-ai-search-now-assist&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

