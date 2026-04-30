---
title: Human feedback for evaluations
description: Expand the Human feedback section to see details on evaluations and their satisfaction scores.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-08-13"
reading_time_minutes: 1
breadcrumb: [Evaluation tab, AI Control Tower Home, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Human feedback for evaluations

Expand the Human feedback section to see details on evaluations and their satisfaction scores.

Role required: interaction\_admin

**Note:** To label a record or label a conversation, you must have access to the transcript, and only users with the interaction\_admin role have access to the transcript.

![Human feedback section.](../image/ai-eval-user.png)

The Evaluations section shows all the chats that were auto-evaluated by the large language model \(LLM\). You have the option to manually evaluate conversations to compare the AI evaluations against your own interpretation of how the agent conversation was.

|Field|Description|
|-----|-----------|
|Number|Evaluation number assigned to each chat conversation. Select the evaluation number to see the respective chat and its evaluations.|
|State|State of the evaluation.|
|Auto Eval user satisfaction Score|Satisfaction score calculated automatically by the LLM.|
|Human User Satisfaction Score|Satisfaction score calculated based on the user evaluation of the chat.|
|Gap|Difference between the human and auto-evaluated satisfaction scores.|

## Manually evaluate a chat

You can manually evaluate each chat to compare it with the AI evaluation.

1.  Select the evaluation that you want to score manually.
2.  Toggle the **View Auto Eval Scores** switch on to see the AI evaluation for each category.
3.  For each category, select your answer for how accurately you feel that the agent responded.

    ![Evaluation details.](../image/ai-eval-chat.png)

4.  Toggle the **Other Metrics** switch on for a more detailed evaluation.
5.  After completing, select **Submit**.

The **Human user Satisfaction Score** value gets calculated based on your response to the questions. You can see your responses for each evaluation by selecting it and then selecting **View Human Scores**. The **Export** option enables you to export the data in your preferred format.

You can also randomly label evaluations by selecting **Label random scores**. When selected, a list of 10 random, unevaluated conversations from the past 10 days are loaded for manual labeling.

