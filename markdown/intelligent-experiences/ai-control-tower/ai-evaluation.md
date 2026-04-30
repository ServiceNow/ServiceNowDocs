---
title: Evaluation tab in AI Control Tower
description: The Evaluation tab contains the Evaluation dashboard, which is designed to measure, automate, and improve the quality of interactions with Virtual Agent. This dashboard addresses several key challenges to enhance the end-user experience and overall virtual agent utility.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-08"
reading_time_minutes: 5
keywords: [Now Assist, Gen AI, generative AI, AI Governance, LLM]
breadcrumb: [AI Control Tower Home, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Evaluation tab in AI Control Tower

The **Evaluation** tab contains the Evaluation dashboard, which is designed to measure, automate, and improve the quality of interactions with Virtual Agent. This dashboard addresses several key challenges to enhance the end-user experience and overall virtual agent utility.

## Evaluation dashboard

**Prerequisites**

Role required: sn\_ai\_governance.ai\_steward

You must [Enabling evaluations](ai-eval-enable.md).

Conversations are excluded from auto-evaluation if any of the following conditions are met:

-   HR conversations: Conversations related to Human Resources are filtered out, which means that they aren’t evaluated.
-   Inaccessible or empty Knowledge Base \(KB\) articles: Conversation involving a Genius Result that points to a KB article that is either not accessible via script or is empty. For example, certain restricted HR Knowledge articles.
-   Immediate live agent transfer: A conversation that begins immediately with transfer to a live agent, with no prior interaction with the virtual agent.
-   Short conversations: Conversations having fewer than 180 words before a live agent is invoked. The word count is configurable via the **autoEvalConstants** script Include. The assumption is that conversations below this threshold didn’t contain a meaningful interaction with the Virtual Agent.
-   Custom triggers: Any custom-defined exclusion triggers.

**Evaluation dashboard overview**

The Evaluation dashboard helps in:

-   Establishing a reliable measurement process by enabling the systematic tracking of the end-user experience with the Virtual Agent, providing deeper insights into interactions.
-   Automation of conversation quality evaluation by automating the process of evaluating conversation quality across different user interactions. This automation helps lead to the creation of a trusted, scalable metric for performance tracking.
-   Continuous improvement by supporting the iterative refinement of the virtual agent's performance, enhancing the overall user experience.
-   Scalable monitoring by helping ensure that the process of evaluating and tracking virtual agent quality is both efficient and scalable, promoting quick identification of issues and improvements over time.
-   User feedback integration through a set of optional questions enables you to provide direct feedback on their experience, which is used to improve the quality of future interactions.
-   Service desk manager insights by enabling service desk managers to track and review auto-evaluation scores over time. Managers can also manually add feedback for benchmarking purposes, providing valuable insights into conversation quality and opportunities for improvement.
-   Sustainable evaluation process by continuously improving virtual agent performance through a combined approach of automated evaluation and manual feedback enabling a scalable and sustainable system that evolves over time.

**Important:** Evaluation dashboard doesn't support domain separation.

## Overview tab

The **Overview** tab of the Evaluation dashboard provides a comprehensive view of all metrics and evaluation data.

![Evaluation tab.](../image/ai-eval.png)

The following widgets are available, showing various metrics:

-   Average Auto Eval score for the selected metric: Shows the average auto-evaluation score for the metric selected and its trend over time.

    For more information about each metric, see [Evaluation metrics and calculations](../reference/ai-eval-metrics.md).

-   Average Human Feedback score for the selected metric: Shows the average human-labeled score for the selected metric.

    **Note:** The score is available only if there are sufficient chat records that are manually evaluated. For more information about manually evaluating conversations, see [Human feedback for evaluations](ai-eval-human-fb.md).

-   Evaluation score trend: Tracks the weekly score for the selected metric.

    If you turn on the **View Deviation and Adjusted Scores** toggle, it shows the comparison between the auto-evaluated and user-defined scores by overlaying the upper, lower deviations, and the final adjusted score on the trend chart.

    **Note:** The deviation and adjusted scores are calculated only if you have at least 50 human labels.

    ![Evaluation trend with deviation and adjusted scores.](../image/ai-eval-01.png)

    For more information about how the calculations are made, see [Evaluation metrics and calculations](../reference/ai-eval-metrics.md).

-   Evaluations: Shows the total number of conversations that were evaluated each week.

-   Human feedback section: Contains detailed information about each evaluation. From here, you can manually evaluate conversations. For more information, see [Human feedback for evaluations](ai-eval-human-fb.md).

## Evaluations

Each conversation is evaluated on eight different metrics. For each of these metrics, there’s a separate skill. You can view these skills in Now Assist Skill Kit under **Custom skills**.

For more information about each metric, see [Evaluation metrics and calculations](../reference/ai-eval-metrics.md).

Role required: sn\_skill\_builder.admin

![Custom skills for evaluation.](../image/ai-eval-02.png)

The following Now Assist custom skills are used:

-   Chat Topic Classifier
-   Coherence Chat Evaluation
-   Conciseness Chat Eval
-   Context Retention
-   Inadequate Slot Filling Chat Eval
-   Intent Accuracy Chat Eval
-   Smooth Flowing Conversation Chat Eval
-   Truthfulness Hallucination Chat Eval

The default provider for these skills is Now LLM. You can change the provider to Azure OpenAI, Google Gemini or AWS Claude. Azure OpenAI has been observed to improve results in certain scenarios.

For more information about Now Assist Skill Kit, see [Now Assist Skill Kit](../../now-assist-skill-kit/concept/now-assist-skill-kit-landing.md).

**Process of evaluation**

Flow: Execute Evaluation.

1.  10% of the daily conversations are sampled, checking if the conversation is good enough to be evaluated or not. The evaluation is done by building the transcripts for these conversations and then sending it to the set large language model \(LLM\).
2.  For the conversations that are good enough to be evaluated, the transcripts along with the prompts for different scales are sent to the LLM and the LLM then evaluates the conversations.
3.  After evaluation, the conversation goes through post processing, where the scores and the reason for scores that the LLM has provided are parsed and stored in the Evaluation and Evaluation Metrics tables.

**Note:** Conversation evaluation estimates are considered as of evaluation date and not the conversation created date. For example, if a chat that happened at time t is evaluated at time t+10, the scores from evaluator is aggregated for the week of t+10 and not for the week of t.

For detailed information about the evaluation flow, see [Evaluation flow](../reference/ai-eval-flow.md).

**Related topics**  


[Value tab in the Evaluation dashboard](ai-eval-value.md)

[Evaluation dashboard References](../reference/ai-eval-references.md)

