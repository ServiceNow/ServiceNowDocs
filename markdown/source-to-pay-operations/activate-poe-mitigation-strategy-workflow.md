---
title: Review the define PO exception mitigation strategy workflow
description: Review the define PO exception mitigation strategy agentic workflow that uses Now Assist agentic support to identify and execute mitigation strategies for purchase order exceptions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist for Purchase Order Management \(POM\), Now Assist for POM, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Review the define PO exception mitigation strategy workflow

Review the define PO exception mitigation strategy agentic workflow that uses Now Assist agentic support to identify and execute mitigation strategies for purchase order exceptions.

## Before you begin

Install the Now Assist for POM plugin \(sn\_poem\_gen\_ai\).

Role required: admin

## About this task

**Important:** This agentic workflow is active by default. All fields are read-only. To modify other fields, clone the workflow. Currently, you can't edit agent prompts or provide feedback for training.

Users with \[sn\_poem\_core.operational\_buyer\] role and the Now Assist Fulfiller \[sn\_poem\_gen\_ai.now\_assist\_fulfiller\] rolec will get mitigation strategies using the Define PO exception mitigation strategy agentic workflow in the Now Assist panel.

This workflow uses the Now Assist agentic support to identify and execute mitigation strategies for purchase order exceptions.

You can add or remove AI agents from this workflow by making a copy and customizing it. For more information, about copying agentic workflows, see [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    The **Manage agentic workflows and AI agents** page appears.

2.  Select **Agentic workflows**.

3.  Open the workflow configuration page by selecting **Define PO exception mitigation strategy**.

    If you want to modify this AI agent, you can refer to [Modify an AI agent](https://www.servicenow.com/docs/access?context=modify-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Adjust the settings for your specific needs, and activate the duplicated version of the agentic workflow.

4.  Select the **Define key requirements** page to review the following fields.

    |Field|Description|
    |-----|-----------|
    |Workflow Name|Define PO exception mitigation strategy.|
    |Workflow description|The Define PO exception mitigation strategy workflow is an AI-powered workflow that resolves purchase order delivery exceptions by analyzing delivery gaps, searching for alternative purchase order lines from different suppliers, and creating optimized change requests that combine supplier-suggested modifications with buyer-approved mitigation plans.|
    |List of steps|Instructions for the LLM service.|

    |Name|Description|Tools and knowledge sources|Model support|Active|
    |----|-----------|---------------------------|-------------|------|
    |Purchase order plan creation AI agent|Analyzes purchase order exceptions and generates actionable mitigation strategies by calculating delivery gap schedules, identifying alternative purchase order lines from different suppliers, presenting options to buyers \(direct edit, system suggestions, or refined search\), and executing combined change requests that integrate both supplier-suggested modifications and buyer-approved mitigation plans.|Create Change Requests, Fetch Exception and Gap Schedule Details, Get Editable Purchase Orders|Available|Active|

<table id="table_bjh_f1q_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

LLM providers

</td><td>

Model providers that this agentic workflow doesn’t support.All model providers are supported by the Define PO exception mitigation strategy workflow.

</td></tr></tbody>
</table>5.  Select **Continue**.

6.  Review how user and data access is defined to confirm that the default settings meet your requirements by selecting **Define security controls**.

    |Field|Description|
    |-----|-----------|
    |Decision type|Allow if|
    |Roles|sn\_poem\_gen\_ai\_now\_assist\_fulfiller|
    |User Authenticated|Not applicable|
    |Active|Active|

    **Note:** This section defines which users can access and interact with this agentic workflow. An access control list \(ACL\) has been automatically generated.

    |Field|Description|
    |-----|-----------|
    |User identity type|Dynamic user|
    |Approved role\(s\)|sn\_poem\_gen\_ai\_now\_assist\_fulfiller|

    **Note:**

    The user identity type that this agentic workflow runs under determines the roles and the data access permissions derived from them.

7.  Select **Continue**.

8.  On the **Add triggers** page, select **Continue**.

9.  Review the information in the **Select channels and status** page.


## What to do next

After reviewing the agentic workflow, you can get started by selecting **Now Assist** button on a purchase order exception record or the exception card on the Purchase order management tab in the Source-to-Pay Workspace.

