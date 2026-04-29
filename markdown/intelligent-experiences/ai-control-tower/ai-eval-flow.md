---
title: Evaluation flow
description: The workflow for evaluation execution, which performs evaluations when conversations are completed.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Evaluation dashboard reference, Reference, AI Control Tower, Enable AI experiences]
---

# Evaluation flow

The workflow for evaluation execution, which performs evaluations when conversations are completed.

Conversations are evaluated using the following logic:

1.  Conversation capture:

    All end-user interactions with the virtual agent are logged in the Conversation table \[sys\_cs\_conversation\]. When a user ends the conversation, the record's state is updated to Complete.

2.  Automated flow evaluation trigger:

    Flow name: Execute Evaluation.

    Trigger condition:

    -   Table: Conversation table \[sys\_cs\_conversation\]
    -   State: Complete
    -   Device type: Web Client, Slack, Teams, Bot to Bot, Messenger

**Sequence of execution**:

Action 0: Check evaluations count for today

-   Perform a query on evaluation table and to get record count.
-   If record count is less than Max Number of evaluations per day, continue to Action 1, else end flow.

Action 1: evalExecuteCondition

-   Invokes the evalExecuteCondition.executeEvaluation script Include with conversation reference.
-   Generates a random number \(1–100\). Proceeds only if ≤10 \(10% random sampling\).
-   Outcome: Returns true or false for further processing.

Action 2: Conditional Branch

-   If true: Proceed to the next action.
-   If false: Evaluation stops.

Action 3: Lookup Interaction Table:

Matches the conversation's channel metadata with the interaction table to fetch related records.

Action 4: Application Scope Filter:

If the interaction's application scope doesn’t include `hr`, continue.

Action 5: buildTranscript:

Detailed Transcript Construction:

-   Tags: \[User\]: For user messages, \[Virtual Agent\]: For virtual agent messages.
-   For any referenced Knowledge article:
    -   Pulls the complete article body to replace genius result, tagged with `[Virtual Agent]: Help articles for user query:` and delimited by Article\_Start/Article\_End.
    -   If the Knowledge article is in HR scope/inaccessible, skip evaluation.
    -   If the Knowledge article content is &gt;10,000 words: Truncate at 10,000.
    -   Attached files \(PDF/Word/Txt\): Use genius result instead.
-   For referenced Catalog Items:

    Extracts name, short description, description, annotated as `[Virtual Agent]: Please choose one of the below options:` with citation number.

-   If the first message is to the live agent, or the live agent is invoked within the first 120 words: skip evaluation.

Outputs:

-   ExecuteEvaluation \(true/false\)
-   Chat Transcript
-   Knowledge articles or catalog items referred
-   Sys\_id of first live agent invocation \(if any\)
-   List of skills to invoke \(all evaluation skills for Evaluation dashboard\)
-   Additional evaluation logs

Action 6: Conditional Branch:

If ExecuteEvaluation is true: Continue to Action 7.

Action 7: Chat Classifier Eval

-   Builds the initial transcript from **sys\_cs\_message**.
-   Uses Chat topic classifier to determine:
    -   Should the conversation be evaluated? \(ExecuteEvaluation: true/false\)
    -   Topic Name
    -   Category \(IT/HR\)
-   If ExecuteEvaluation is true: Proceed to Action 6.

Action 8: Create or Update Evaluation Record:

Create a record on Evaluation \[sn\_na\_conv\_eval\_evaluation\] table with:

-   Document Conversation: Conversation reference
-   State: Processing
-   Topic, Category, Knowledge article or catalog references, first live agent sys\_id, type, user who initiated, message log

Action 9: For each skill:

Repeats for each skill flagged in Action 6.

Action 10: invokeApiDefinition

-   Inputs: Skill name, conversation, transcript, evaluation id
-   Calls Now Assist Skill API asynchronously.
-   Post processing available in sys\_generative\_ai\_response\_validator, performs the following parsing:
    -   Score
    -   Reason for Score
    -   Examples for the reasoning
-   Parsed data is created on the Evaluation Metrics \[sn\_na\_conv\_eval\_evaluation\_metrics\] table \(Score, Reasons, Examples, and the entire reasoning for scoring \[Scratchpad\]\).

Action 11: Waits 7 seconds before continuing to the next skill.

Special behavior and edge case handling:

-   Sampling: Only 10% of conversations \(randomly chosen\) are evaluated.
-   Channel Filter: Only Web, Slack, Teams, Bot to Bot, Messenger.
-   Application Scope: Excludes records with `_hr_` in the scope.
-   Knowledge article controls: No evaluation for HR or inaccessible. Knowledge articles, limits on Knowledge article size, and file handling.
-   First live agent invocation: Excludes conversations routed to the live agent at the start or within 120 words.
-   The Request Completion skill is added as part of a business rule where the score is tagged as the lowest between Slot filling and Intent.
-   The reason on the record is added as follows:

    ```
    if (Slot filling score > Intent score) {
    Intent reason is used
    } else if (Slot filling score < Intent score) {
    Slot filling reason is used
    } else {
    Both are used
    }
    
    ```


