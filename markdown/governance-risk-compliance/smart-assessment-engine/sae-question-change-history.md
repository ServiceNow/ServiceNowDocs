---
title: Question change history
description: Review a log of every response, justification, and flag state change made to a question throughout the lifecycle of an assessment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-question-change-history.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-09-03"
reading_time_minutes: 3
keywords: [change history, question history, audit, activity]
breadcrumb: [Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Question change history

Review a log of every response, justification, and flag state change made to a question throughout the lifecycle of an assessment.

## Change history overview

Question change history tracks changes to a question's response, justification, and flag state. Changes are tracked regardless of whether the assessment is open, closed, or cancelled. Each entry records a timestamp, who made the change, what changed, and the previous and new values.

**Note:** This feature is available starting with Zurich Patch 10.

Each question card includes a change history icon. Selecting it opens the **Change history** panel. The panel logs changes to three parts of a question: the response, the justification, and the flag state. Changes are tracked for the entire lifecycle of the assessment.

When you first open the change history panel, or move to a different question, it automatically shows the latest changes for that question. If a change is made to the current question while the panel remains open, select the refresh icon in the panel header to load the latest entries.

**Note:**

-   The change history panel logs activity starting from when this feature became available on your instance. Responses, justifications, and flag changes made before that aren't migrated into the change history; that data remains in the platform's System Audit \[sys\_audit\] table.
-   Attachment-type questions, and any question with the ask for attachment option enabled, don't have their attachment changes tracked.

## How changes are grouped

To avoid logging every intermediate keystroke, the system merges consecutive response and justification changes made by the same user into a single entry when the changes occur within 300 seconds by default:

-   If the same user changes the same field within the window, the entry updates instead of creating a new one, and its timestamp updates to the latest change.
-   The system merges changes only when both the field and source match the most recent entry. Sources include manual and automated. If you change a different field or use a different source on the same question, the merge stops and a new entry begins, even within the merge window.
-   If a different user changes the same field during that window, a separate entry is created. Changes made by different users are never merged, regardless of the time between them.
-   If a user reverts a field to its pre-edit value within the window, the entries covering that back-and-forth are removed, since they represent no net change.

Flag state changes are never merged, even when the same user makes multiple flag changes seconds apart. Every flag transition is logged as its own entry because each state — Unflagged, Flagged, and Resolved — is meaningful on its own. For more information about flag states, see [Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md).

**Note:**

-   The default merge window is 300 seconds. An Assessment admin can change this value in the `sn_smart_asmt.activity_merge_window_in_seconds` system property.
-   Reducing the value produces more granular history; increasing it produces fewer, larger entries. A change to this property applies only to activity recorded after the change is made.

## Who made the change

The actor on an entry identifies who made the change:

-   **User**

    The username of the person who made the change.

-   **System**

    Attributed to System for the following cases:

    -   Automated and non-editable response: each change to a question whose response is automated and non-editable is attributed to System. These questions display a **Last responded by System** indicator.
    -   Automated and editable response: the default automated response set when the assessment instance is created is attributed to System. Any subsequent change made by a user is attributed to that user.
    -   Changes made through asynchronous or system-initiated operations, such as the Copy Response API, are also attributed to System

## Question type display

Before and after values are shown in a format suited to the question type: for example, comma-separated values for multi-select questions, or the configured display field value for reference questions. Justification changes are tracked the same way as text responses. If a response is changed so that a justification is no longer required for the question, the justification value is cleared at the time the assessment is submitted. Until submission, the value is preserved in the system and continues to appear in the change history. This change is attributed to the user who submits the assessment.

