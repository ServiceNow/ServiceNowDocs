---
title: Evaluation metrics for automated evaluation
description: Metrics used to define success for evaluations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/evaluation-metrics-auto-eval-ad.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Testing assistant conversations, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Evaluation metrics for automated evaluation

Metrics used to define success for evaluations.

## Conversation success

Conversation success checks if your assistant interprets what users ask for and gives them the right answer or outcome.

This metric tracks whether your assistant completes user requests successfully, determining what they need and delivering the right response.

This metric requires ground truth, which is the correct answer or outcome for each request.

The metric checks each user request in a conversation to see if it was completed successfully. If a conversation has multiple requests, each one is evaluated separately:

-   Success equals: Assistant delivers the right information or performs the right action for every request \(Score: 1\).
-   Failure equals: Assistant performs the wrong action or delivers the wrong answer for one or more requests \(Score: 0\).

Output from the metric: Shows as '1' for success or '0' for failure in your report \(one score per conversation\).

**Note:** Conversation success can only be measured with ground truth data.

## Skill selection accuracy

Skill selection accuracy checks if your assistant picks the right skill or AI agent from your available options to answer each user question.

Skill selection accuracy measures your assistant's routing decisions. That is, does it choose the right skill from your list \(like topics, AI agents, or catalog items\) based on what users ask? Your skill list is the ground truth for this metric.

This also checks if your assistant correctly makes no selection when a question doesn't match any available skill.

This metric requires ground truth, which determines which skill should be selected for each type of question.

The metric checks each user question to see if your assistant made the right choice, considering:

-   Offered selections: When users make requests, does the assistant offer the right options?
-   With ground truth data: Accuracy = correct selections/total questions evaluated.

**Ground truth**: Your reference list showing the correct skill for each question type, like topics, AI agents, or catalog items.

Output from the metric: Accuracy percentage \(0-100%\).

**Note:** Skill selection accuracy can only be measured with ground truth data.

## Turn count

Counts how many back-and-forth exchanges it takes to complete a user's request. Each time the user sends a message, that's one turn.

The metric counts how many turns your assistant takes to complete a user's request.

Can be used for:

-   Question-and-answer interactions.
-   Structured task flows \(like booking appointments or submitting requests\).
-   Scenarios where there's a clear goal and defined path.

**Note:** This metric is more suitable for goal-driven conversations, not open-ended chats where there's no specific endpoint.

Turn count shows how efficiently your assistant resolves requests. It helps you spot when your assistant might be:

-   Asking redundant questions.
-   Failing to capture information efficiently.
-   Requiring users to repeat themselves.
-   Taking indirect paths to the solution.

Output from the metric:

-   Number of total turns per conversation.
-   Overall average number of turns for all conversations.

**Note:** The lower the count, the better.

## Faithfulness

Checks whether your assistant uses only the information it can access, without fabricating details.

Faithfulness checks if your assistant's responses come from the information it has access to, like knowledge articles, conversation history, or ticket records:

-   A faithful response only includes information supported by these sources.
-   An unfaithful response adds claims or details that aren't in the provided context, even if they're actually true.

**Note:** Faithfulness isn't the same as accuracy. Your assistant can still faithfully use information from a source that's incorrect.

The metric evaluates each claim your assistant makes and checks if it's backed up by available information.

The faithfulness score shows the proportion of claims that are grounded in the context:

-   Higher scores mean most or all claims are supported.
-   Lower scores indicate your assistant is adding unsupported information \(hallucinating\).

Output from the metric: Success displays as 1 and failure displays as 0 \(per reply\) in your report. You can see a score for each reply, plus an overall average score.

## Conversation fluency

Measures whether your assistant's responses are clear, natural, and grammatically correct.

Conversation fluency checks if your assistant sounds natural and is easy to understand. It checks whether responses read smoothly, use correct grammar, and feel like real conversations. This can enable you to catch responses with awkward wording, repetition, or unclear language that could frustrate users.

Each response gets scored on a 3-point scale:

-   Score of 3 \(sounds great\):
    -   Easy to read and understand.
    -   Feels like natural conversation.
    -   Right amount of detail.
    -   No grammar issues.
    -   Replies aren't repetitive or inconsistent.
-   Score of 2 \(minor issues\):
    -   Slightly awkward phrasing.
    -   A bit robotic.
    -   Small grammar issues that don't block understanding.
    -   Replies show some repetition from previous replies.
-   Score of 1 \(hard to follow\):
    -   Confusing or unclear.
    -   Major grammar problems.
    -   Too much repetition.
    -   Doesn't make sense.
    -   Replies show major inconsistencies or contradict previous replies.

You can check fluency for individual responses or across entire conversations.

Output from the metric: Each response gets a numerical score from 1 to 3. You can see a score for each reply, plus an overall average score.

**Related topics**  


[Testing assistant conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/evaluations-ad.md)

[Set up an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/create-auto-evaluation-ad.md)

[Insights into failed scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/severity-insights.md)

