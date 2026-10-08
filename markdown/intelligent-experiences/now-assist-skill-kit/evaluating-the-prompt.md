---
title: Prompt evaluation guidelines
description: Evaluate a skill prompt during development and again before deployment, using batches of test data and metrics that suit your use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/evaluating-the-prompt.html
release: brazil
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [General guidelines for AI Skill Kit, Exploring AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Prompt evaluation guidelines

Evaluate a skill prompt during development and again before deployment, using batches of test data and metrics that suit your use case.

## Evaluation approach

To determine the effectiveness of your prompt, you should evaluate batches of test data. You should copy the model-generated responses and perform evaluations outside of AI Skill Kit.

## During prompt development

Ongoing, improvised evaluation should take place alongside the development of the prompt. This ongoing evaluation enables you to adapt the prompt based on observed model outputs. Testing a change to a prompt against one or two examples can be tempting. To avoid reacting to noise, look at larger batches, and consider the statistical significance of the performance differences that you observed.

\[Omitted image "nask-prompt-perf-comp.png"\] Alt text: Chart that shows a comparison of prompt performance.

## Final performance evaluation

Before you deploy a skill, you should test the prompt on a representative batch of data that was isolated from the development process, that is, “test” data. You want to use isolated test data because of a phenomenon known as prompt overfitting. Iteratively editing a prompt based on the model outputs generated on the same data that is used for testing can lead to significant overestimates of performance. This result is because the prompt can become overspecialized to the specific examples used in development. Even though the effect is typically less dramatic than what occurs when fitting machine learning model parameters to a test dataset, it’s rooted in the same underlying principles, and should be avoided.

## Evaluation metrics

Selecting the right metrics for evaluation is an important consideration. The following list provides a few approaches, each of which may be more or less appropriate depending on the use case.

-   Classification-based assessment of short generations

    This approach requires labeled records, and it works best when the labels are short, well-defined “right answers,” for example, true or false, multiple-choice, or category selection. In these cases, the model outputs can usually be parsed and formatted, then metrics like precision, recall, F1 scores, and so on can be directly calculated.

-   Assessment of longer generations

    Many generative AI use cases require longer model generations, and there are many possible “right answers.” In these cases, the output can be scored \(by human evaluators\) along several different axes, for example:

    -   Faithfulness

        Is the generated text faithful to the context provided in the skill prompt? \(The opposite of faithfulness is hallucination, which is to say that the model injects out-of-context information.\)

    -   Correctness

        Is the generated text correct relative to the skill instruction?

    -   Helpfulness

        Is the generated text helpful relative to the task that the skill performs? \(Helpfulness is subjective but it’s important to try to measure. Doing so properly requires a solid understanding of the needs of the people who ultimately use the skill.\)

    -   Fluency

        Is the generated text grammatically correct? Does it have any typos, issues with coherency, and so on?

    **Note:** It’s useful to score these properties on a scale, such as 1 through 5, rather than with yes or no.


