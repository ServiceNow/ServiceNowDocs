---
title: Generate recommendation for similar control objective
description: Generate recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library. This enables identification of redundant control objectives, making it easier to maintain a clean and efficient compliance library.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Generate recommendation for similar control objective

Generate recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library. This enables identification of redundant control objectives, making it easier to maintain a clean and efficient compliance library.

## Before you begin

Role required: sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user

For more information on related roles, see [Roles installed with GRC: Policy and Compliance Management](../reference/r_InstallWPolAndCompl.md#).

## About this task

The recommendations are suggested based on the similarity parameters configured which are the names and description. The Gen AI searches for similar names and descriptions, which serve as inputs for providing recommendations.

**Important:** Be sure to check AI-generated recommendations for accuracy.

## Procedure

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**.

2.  Select ![](../../assessment-engine/image/list-icon.png).

3.  Navigate to **Compliance library** &gt; **Control objectives**.

4.  Open the control objective which you want to rationalize.

5.  On the Overview tab, select **Rationalize**.

    A new page **Create New Rationalization process** is displayed.

    **Note:**

    -   A new rationalize process can also be created by opening Compliance workspace list and selecting rationalization process.
    -   If a rationalization process is already available for a control objective, the user is directed to the rationalize tab for that specific control objective.
6.  On the form, fill in the fields.

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
</table>7.  Select **Save**.

    A new button **Analyze** appears on the screen.

8.  Select **Analyze**.

    -   A confirmation message that recommendations are being generated is displayed.
    -   Once the recommendations are ready a new **Rationalize** tab will appear, try reloading the page after some time.
    -   The rationalize process state is moved from **Initiate** to **Analyze**.

## What to do next

Accept or dismiss the generated recommendations. For more information, see [Act on the recommendations for similar control objectives](take-actions-on-the-recommendations-for-similar-control-objectives.md).

**Note:**

You can configure UI form actions in addition to "Accept as duplicate", "Dismiss" and "Retain as primary" as declarative actions for recommendations. Declarative actions help you to modify the list actions and related list actions. For more information about creating declarative actions and how to use them, see.

