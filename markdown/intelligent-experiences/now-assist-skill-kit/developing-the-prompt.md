---
title: Prompt development guidelines
description: Write a skill prompt that is specific, clear, and grounded in context so that the model is more likely to return the output that you expect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skill-kit/developing-the-prompt.html
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [General guidelines for AI Skill Kit, Exploring AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Prompt development guidelines

Write a skill prompt that is specific, clear, and grounded in context so that the model is more likely to return the output that you expect.

## Prompt design guidelines

Base prompt development decisions on the model outputs that a prompt generates across many different inputs. The following guidelines can help you get started with prompt design.

1.  Be specific

    Define your desired outcome clearly. Be specific about the task that you want the model to fulfill. Clearly identify the inputs that you're providing to the model, and specify the output you’re expecting from the model \(including formatting\).

2.  Include the right context

    Provide background information and context relevant for fulfilling the task. This information can generate a more focused response.

3.  Use clear language

    Use precise and unambiguous language while writing the prompt.

4.  Include demonstrations

    If possible, experiment with providing completed examples, or demonstrations, in the prompt after the instructions to illustrate what you want the model to produce. Demonstrations can increase the likelihood of generating a desirable output. However, the performance changes depending on the demonstrations selected.

5.  Start simple and test variations

    Break down complex tasks into smaller and clearer instructions. Have a controlled and iterative approach. Experiment with different structures.


## Other considerations

-   Subtle differences in wording can lead to substantial differences in performance. Trying to reason about how a large language model \(LLM\) may “interpret” the instructions in a prompt only gets you so far. Which specific choice of prompt wording works best depends on the underlying model and should ideally be chosen based on evidence \(that is, looking at lots of outputs\).
-   In data-constrained settings, iteratively develop several candidate prompts using the development data, then measure the performance of each candidate prompt on the test set, choosing the best one.

