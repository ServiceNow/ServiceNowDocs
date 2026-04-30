---
title: Use Recommendation of similar control objectives skill to generate suggestions
description: The "Recommendation of similar control objectives" skill generates recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library. This enables identification of redundant control objectives, making it easier to maintain a clean and efficient compliance library.
locale: en-US
release: yokohama
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# Use Recommendation of similar control objectives skill to generate suggestions

The "Recommendation of similar control objectives" skill generates recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library. This enables identification of redundant control objectives, making it easier to maintain a clean and efficient compliance library.

## Before you begin

Role required: sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

The "Recommendation of similar control objectives" skill generates recommendations based on the similarity parameters configured \(names and description\). The Gen AI searches for similar names and descriptions, which serve as inputs for providing recommendations.

**Important:** Be sure to check AI-generated recommendations for accuracy.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Control objectives** &gt; **All Control objectives**.

2.  Open the control objective which you want to rationalize.

3.  On the Overview tab, select **Rationalize**.

    A new page **Create New Rationalization process** is displayed.

    **Note:**

    -   A new rationalize process can also be created by opening compliance workspace list and selecting rationalization process.
    -   If a rationalization process is already available for a control objective, the user is directed to the rationalize tab for that specific control objective.
4.  On the form, fill in the fields.

<table id="table_nv5_hpp_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the rationalization process.

</td></tr><tr><td>

Owner

</td><td>

User that owns the policy.

</td></tr><tr><td>

Rationalization table

</td><td>

The record type on which rationalization is being done.**Note:** Currently rationalization is only available on control objective.

</td></tr><tr><td>

Rationalization record

</td><td>

The record on which the rationalization is being done.

</td></tr><tr><td>

Additional comments

</td><td>

Additional information about the rationalization process.

</td></tr></tbody>
</table>5.  Select **Save**.

    A new button **Analyze** appears on the screen.

6.  Select **Analyze**.

    -   A confirmation message that recommendations are being generated is displayed.
    -   Once the recommendations are ready a new **Rationalize** tab will appear, try reloading the page after some time.
    -   The rationalize process state is moved from **Initiate** to **Analyze**.

## What to do next

Accept or dismiss the generated recommendations. For more information, see [Act on the recommendations for similar control objectives](../../grc-policy-and-compliance/concept/take-actions-on-the-recommendations-for-similar-control-objectives.md).

**Note:**

You can configure UI form actions in addition to "Accept as duplicate", "Dismiss" and "Retain as primary" as declarative actions for recommendations. Declarative actions help you to modify the list actions and related list actions. For more information about creating declarative actions and how to use them, see.

