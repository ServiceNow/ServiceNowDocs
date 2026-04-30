---
title: Evaluation flow for batch evaluations
description: Batch evaluation enables Eval admins to evaluate up to 100 completed virtual agent conversations at once, based on a saved query.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2025-09-03"
reading_time_minutes: 4
breadcrumb: [Evaluation dashboard References, AI Control Tower Reference, AI Control Tower, Enable AI experiences]
---

# Evaluation flow for batch evaluations

Batch evaluation enables Eval admins to evaluate up to 100 completed virtual agent conversations at once, based on a saved query.

Flow name: Execute Batch Evaluation.

The flow creates evaluation records and invokes Now Assist skills for each eligible conversation, mirroring the single-conversation evaluation logic, but at scale. It enforces HR scope exclusions, topic/category validation, transcript construction rules, early live-agent exclusions, and asynchronous scoring through skills.

Batch evaluations are performed using the following logic:

Trigger

-   Table: Evaluation set \[sn\_na\_conv\_eval\_evaluation\_set\]
-   Condition: State changes to In Progress and Evaluation type = Conversation

Inputs

-   Evaluation Set record with:
    -   Query filter: A query that targets conversations to be evaluated \(for example, sys\_cs\_conversation filters\).
    -   Evaluation type: Conversation
    -   State: In Progress \(to start\)
-   LLM/Skills: Chat Topic Classifier, plus the evaluation skills listed after this.

High-level behavior

-   Reads the query filter and randomly samples up to 100 conversations.
-   Skips already-evaluated conversations.
-   Excludes HR-scoped interactions.
-   Uses Chat Topic Classifier to validate evaluation eligibility and extracts Topic and Category.
-   Builds a transcript with controlled inclusion of Knowledge articles and catalog sources, and applies early live agent exclusions.
-   Creates an Evaluation record and asynchronously invokes all selected evaluation skills, writing scores and rationale to metrics.

**Sequence of execution**:

Action 1: If the query filter isn’t empty

-   Purpose: Guard clause.
-   Logic: Look up the Evaluation Set record and check the query filter field.
-   If the query filter is present: Proceed to Action 2.
-   If empty: Stop and optionally log `No query provided.`

Action 2: Randomize conversations

-   Purpose: Select a bounded, random sample of conversations from the provided query.
-   Logic:
    -   Execute the query to get matching conversation records.
    -   Randomly select up to 100 conversations.
        -   If &gt;100 matches, cap at 100.
        -   If &lt;100, select all.
    -   Validate the query; if invalid, return false and an empty or partial array.
-   Outputs:
    -   success: true/false
    -   conversation\_ids: array of sys\_ids \(max 100\)
-   If success = true: Proceed to Action 3; otherwise, stop and log the validation error.

Action 3: Look up the evaluation table to check prior evaluation

-   Purpose: Avoid duplicate evaluations.
-   Logic: For each conversation sys\_id, check sn\_na\_conv\_eval\_evaluation for existing records indicating that it's already evaluated or is in progress \(implementation choice: state not in canceled/failed\).
-   If not previously evaluated: Proceed to Action 4 for that conversation.
-   If already evaluated: Skip this conversation, optionally log `Already evaluated`.

Action 4: Look up the interaction record

-   Purpose: Enforce HR scope exclusion.
-   Logic: Resolve the interaction related to the conversation. If its application scope contains `hr`, skip the conversation.
-   If the scope doesn’t contain `hr`: Proceed to Action 5.

Action 5: buildTranscript

-   Purpose: Construct the final, minute-level transcript and determine downstream skill set and guardrails.
-   Steps:
    -   Aggregate all conversation messages.
    -   Tag user messages as `[User]:` and virtual agent messages as `[Virtual Agent]:`.
    -   Knowledge articles:
        -   If genius results reference Knowledge articles, query the Knowledge article and replace the genius snippet with the entire article body.
        -   Annotate with `[Virtual Agent]: Help articles for user query:` and wrap content within Article\_Start and Article\_End.
        -   Constraints:
            -   If the KB is HR-scoped or inaccessible, don't evaluate \(skip conversation\).
            -   Truncate the article body to a maximum of 10,000 words.
            -   If the KB content source is attached files \(PDF/Word/Txt\), fall back to the genius result instead of full file content.
    -   Catalog Items:
        -   If genius results reference catalog items, query sc\_cat\_item and build a string: catalog name, short description, description.
        -   Annotate with `[Virtual Agent]: Please choose one of the below options:` and include citation order.
    -   Live Agent Exclusions:
        -   If the first user message requests a live agent, skip evaluation.
        -   If a live agent is invoked within the first 120 words, skip evaluation.
-   Outputs:
    -   ExecuteEvaluation: true/false \(post-guardrail outcome\)
    -   Chat transcript
    -   Knowledge articles referred
    -   Catalog items referred
    -   First live agent occurrence: Sys\_id of the conversation message \(if present\)
    -   Skills to invoke:
        -   Coherence Chat Evaluation
        -   Conciseness Chat Eval
        -   Context Retention
        -   Inadequate Slot Filling Chat Eval
        -   Intent Accuracy Chat Eval
        -   Smooth Flowing Conversation Chat Eval
        -   Truthfulness Hallucination Chat Eval
    -   Additional logs
-   If ExecuteEvaluation = true: Proceed to Action 7; otherwise, skip the conversation.

Action 6: If Block

-   Purpose: Branch to record creation.
-   Logic: If ExecuteEvaluation from Action 6 is true, go to Action 8.

Action 7: Chat Classifier Eval

-   Purpose: Validate whether the conversation should be evaluated and extract high-level labels.
-   Logic:
    -   Build a lightweight transcript from sys\_cs\_message for classification input.
    -   Invoke Chat topic classifier skill with the transcript.
    -   Receive:
        -   Execute evaluation: true/false
        -   Topic Name
        -   Category: IT or HR
-   If Execute evaluation = true: Proceed to Action 6.
-   If false: Skip conversation and log the classifier decision.

Action 8: Create or Update evaluation record

-   Purpose: Persist an evaluation entry for this conversation.
-   Table: sn\_na\_conv\_eval\_evaluation
-   Field population:
    -   Document conversation: Conversation reference
    -   State: processing
    -   Topic: from Action 5
    -   Category: from Action 5
    -   KB Referred: from Action 6
    -   Catalog Referred: from Action 6
    -   First live agent occurrence: from Action 6
    -   Type: chat summarization
    -   User: initiating user for the conversation
    -   Message log: Additional logs from Action 6
-   On success: Proceed to Action 9.

Action 9: For Loop over skills

-   Purpose: Execute each selected evaluation skill.
-   For each skill in the list from Action 6:
    -   Action 10: invokeApiDefinition
        -   Inputs: Skill Name, Conversation, Transcript, Evaluation Id
        -   Behavior:
            -   Invoke the Now Assist skill asynchronously.
            -   The post-processor writes results into sys\_generative\_ai\_response\_validator.
            -   Extract JSON response fields:
                -   Score
                -   Reason for Score
                -   Examples supporting the reasoning
            -   Create child metric records in sn\_na\_conv\_eval\_evaluation\_metrics linked to the parent evaluation.
    -   Action 11: Wait

        Pause seven seconds before proceeding to the next skill to manage rate limits or throttling.


**Parent Topic:**[Evaluation dashboard References](ai-eval-references.md)

