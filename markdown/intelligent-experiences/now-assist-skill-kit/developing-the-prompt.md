---
title: Developing the prompt
description: Use the guidelines to help create a prompt for your skill. A specific, clear, contextual prompt provides better results.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [General guidelines for Now Assist Skill Kit, Exploring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Developing the prompt

Use the guidelines to help create a prompt for your skill. A specific, clear, contextual prompt provides better results.

## Prompt development overview

As a prompt engineer, you should make development decisions by looking at the model outputs that are generated in response to a prompt applied to many different inputs. However, there are still certain guidelines that may help users get started with prompt design.

1.  Be specific

    Define your desired outcome clearly. Be specific about the task that you want the model to fulfill. Clearly identify the inputs that you're providing to the model, and specify the output you’re expecting from the model \(including formatting\).

2.  Include the right context

    Provide background information and context relevant for fulfilling the task. This information can generate a more focused response.

3.  Use clear language

    Use precise and unambiguous language while writing the prompt.

4.  Include demonstrations

    If possible, experiment with providing completed examples, or demonstrations, in the prompt after the instructions to illustrate what you want the model to produce. Demonstrations are a powerful way to increase the likelihood of generating a desirable output. However, the performance changes depending on the demonstrations selected.

5.  Start simple and test variations

    Break down complex tasks into smaller and clearer instructions. Have a controlled and iterative approach. Experiment with different structures.


## Other considerations

-   Subtle differences in wording can lead to substantial differences in performance. Trying to reason about how a large language model \(LLM\) may “interpret” the instructions in a prompt only gets you so far. Which specific choice of prompt-wording works best depends on the underlying model and should ideally be chosen based on evidence \(that is, looking at lots of outputs\).
-   In data-constrained settings, you should iteratively develop several candidate prompts using the development data, then measure the performance of each candidate prompt on the test set, choosing the best one.

