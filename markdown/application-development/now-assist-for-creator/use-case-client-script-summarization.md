---
title: Use case: Summarize a client script using Now Assist
description: Understand and edit client scripts.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Use case, Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Use case: Summarize a client script using Now Assist

Understand and edit client scripts.

## Scenario

A developer at a financial services company has joined a team responsible for managing an existing IT operations portal created with UI Builder. This portal consists of multiple pages that contain client scripts written by a previous developer who is no longer with the organization. Before making any modifications, the new developer needs to understand the functionality of each client script and the specific events that trigger them.

## Problem

The client scripts are lengthy and undocumented, making it time-consuming for the developer to read through each one to understand its purpose. Misinterpreting a script before making changes could introduce bugs or break key portal functionality. Manually reviewing and documenting each script would take hours and slow down the team’s ability to deliver updates.

## Solution

With Client script summarization, the developer can select any client script in the **Data and scripts** panel and request an instant AI-generated explanation. Now Assist provides both a high-level summary and a detailed breakdown of the script’s logic and trigger conditions, enabling the developer to quickly assess the script’s purpose and decide whether changes are safe to make.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](../task/install-ui-generation.md) and [Grant UI Builder admin role](../task/grant-ui-builder-admin-role.md).

## Configuration steps

Perform the following steps to use the Client script summarization skill:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Open the IT operations portal experience.
3.  Select the page that includes the client script for review.
4.  In the **Data and scripts** panel, open the relevant client script.

    The **Explain Code** panel appears.

    **Note:** The **Explain Code** panel appears only if you're assigned the ui\_builder\_admin role and if the Client script summarization skill is enabled.

5.  Select **Explain this code**.
6.  Review the concise summary and detailed explanation, including trigger conditions.
7.  If you make changes to the script, select **Explain again** to regenerate the summary for the updated version.

    **Note:** If you update a script after reviewing the explanation, the **Explain Code** panel will notify you of the code changes. Always select **Explain again** to understand the latest version of the script.


## Outcome

The developer quickly comprehends the purpose and functionality of the client scripts, whereas manually reading and interpreting the code would take several hours. This knowledge enables the developer to confidently plan and implement updates without the risk of introducing unintended regressions.

**Parent Topic:**[UI Generation use cases](../task/ui-generation-use-cases.md)

**Related topics**  


[Client script summarization](client-script-summarization.md)

[Summarize a client script using Now Assist](../task/client-script-summarization-generation.md)

