---
title: Enabling evaluations
description: Evaluate random conversations by enabling continuous monitoring.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 4
breadcrumb: [Evaluation in the Virtual Agent's asset record, AI asset inventory, AI assets, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Enabling evaluations

Evaluate random conversations by enabling continuous monitoring.

Role required: admin

Enable evaluations and set the number of evaluations to be performed daily.

## Enable evaluations

1.  Activate Skills:
    1.  Navigate to **Admin** &gt; **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Platform**.
    2.  Turn on the following skills:

        -   Intent Accuracy Chat Eval
        -   Inadequate Slot Filling Chat Eval
        -   Smoothness \(Deadlock avoidance\)
        -   Context Retention
        -   Coherence Chat Evaluation
        -   Truthfulness Hallucination Chat Eval
        -   Conciseness Chat Eval
        -   Chat topic classifier
        **Note:** You can get the filtered list using the filter condition **Conversation Evaluator** under **Features**.

2.  Set the value for the system property **sn\_na\_conv\_eval.maxEvaluateCount**.
    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
    2.  Search for and select the property **sn\_na\_conv\_eval.maxEvaluateCount**.
    3.  Update the **Value** field to set the maximum number of conversations to be evaluated daily.

        ![Update the Value field.](../image/ai-eval-enable-02.png)

    4.  Select **Save**.
3.  Activate the following associated scheduled jobs:
    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
    2.  Apply the filter condition `Application is Conversation Evaluator` and filter out the job Evaluation Value Calcuation - Runs Only once after install.

        ![Apply filter condition.](../image/ai-eval-enable-03.png)

    3.  Activate all the scheduled jobs in the filtered list.
4.  Activate the Execute Evaluation flow in Flow Designer.

    **Note:**

    By default, the Execute Evaluation flow is deactivated. You can use the nightly scheduled job, Execute Evaluations, to evaluate the chats. The nightly job won't dominate over LLM calls from other services, whereas the real-time evaluation through the Execute Evaluation flow might conflict with LLM calls from other applications.

    If you want to evaluate the chats real-time on chat completion, activate the Execute Evaluation flow. Domain separation is not supported.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer** and select **Flows**.
    2.  Select the Execute Evaluation flow.
    3.  Select **Edit flow**.
    4.  Select **Activate**.

        ![Activate the Execute Evaluation flow.](../image/ai-eval-enable-01.png)


**Note:**

-   If you want to configure some of the evaluation parameters based on your requirements, see [Configuring evaluations](ai-eval-config.md).
-   If you want to import historical data to be evaluated, you must run batch evaluations by activating the Execute Batch Evaluation flow. For more information on the batch evaluation workflow, see [Evaluation flow for batch evaluations](../reference/ai-eval-flow-batch.md).

## Evaluation dashboard vs. Conversation Insights

You can use the Evaluation dashboard and the Conversation Insights \(CI\) application together to gain a complete picture of virtual agent effectiveness, from system performance to end-user satisfaction.

For more information about Conversation Insights, see [Conversation Insights](../../conversation-insights/concept/conversation-insights.md).

<table id="table_c5p_4cn_ngc"><thead><tr><th>

Metrics captured by the Evaluation dashboard

</th><th>

Metrics captured by Conversation Insights

</th></tr></thead><tbody><tr><td>

The Evaluation dashboard provides granular diagnostic explanations that help improve virtual agent design, dialog flows, and model accuracy. It evaluates performance along dimensions critical to task success and trustworthiness. For example, "Is the system working properly and performing the expected task?"

 -   Intent Recognition: Whether the virtual agent correctly interprets the user's primary goal.
-   Slot Filling: Accuracy of extracting structured inputs required to complete tasks.
-   Conciseness: Avoidance of verbose or repetitive responses.
-   Coherence: Logical flow and organization of the virtual agent's responses.
-   Truthfulness: Ensures that responses are grounded in context or knowledge sources, not hallucinated.
-   Context Retention: Virtual agent's ability to remember earlier user inputs in the same session.
-   Deadlock Avoidance: Detects loops where the virtual agent gets stuck repeating questions or responses.
-   User Satisfaction \(proxy\): Correlates critical failures \(like intent recognition or slot filling\) with likely negative user perception.

</td><td>

Conversation Insights focuses on measuring customer satisfaction and effort. It uses inferred customer satisfaction \(CSAT\) and supporting signals to show how end users perceive their interaction with the virtual agent. For example "Is the end user happy with the virtual agent's performance?"

 -   Inferred CSAT: Composite score \(1–5\) estimating overall satisfaction with the conversation.
-   Effort Score: Measures how much work the user had to do \(low/medium/high\), based on transfers, escalations, repeated data collection, or wait times.
-   Resolution: Tracks whether the user's issue was fully, partially, or not resolved.
-   Frustration: Detects explicit signs of user frustration such as rude language, sarcasm, or complaints about difficulty.
-   Confusion: Identifies misunderstandings between the user and virtual agent or the live agent.
-   Transfers and Escalations: Flags when a conversation is passed to another agent, team, or supervisor.
-   Empathy: Scores how polite, personable, and supportive the virtual agent or live agent was \(low/medium/high\).
-   Next Steps: Measures how clearly the virtual agent or live agent explained outcomes, instructions, or follow-up actions \(low/medium/high\).

</td></tr></tbody>
</table>Together, the Evaluation dashboard and Conversation Insights provide complementary value for virtual agent implementations.

-   Conversation Insights offers a lightweight, cost-free view of the customer experience across all conversations.
-   The Evaluation dashboard delivers granular, task-focused diagnostics that enable targeted improvements to virtual agent design and performance.
-   Consolidated in AI Agent Analytics and AI Control Tower dashboards, these metrics give users complementary views into virtual agent system health and end-user satisfaction.

