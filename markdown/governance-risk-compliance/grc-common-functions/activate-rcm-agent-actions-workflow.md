---
title: Activate the generate regulatory action plan agentic workflow
description: Configure and activate the generate regulatory action plan agentic workflow. This workflow uses AI agents to transform regulatory insights into actionable compliance strategies by analyzing impacted areas and historical alerts, then generating structured tasks with clear ownership and timelines.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-11-10"
reading_time_minutes: 4
keywords: [Regulatory alerts, Agentic workflow, Security controls, Triggers, Channels]
breadcrumb: [Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Activate the generate regulatory action plan agentic workflow

Configure and activate the generate regulatory action plan agentic workflow. This workflow uses AI agents to transform regulatory insights into actionable compliance strategies by analyzing impacted areas and historical alerts, then generating structured tasks with clear ownership and timelines.

## Before you begin

Install the Now Assist for IRM plugin \(sn\_irm\_gen\_ai\).

The regulatory alert recommendation skill and a regulatory alert with impacted areas defined are required to generate an action plan. For more information, see [AI-generated recommendations for a regulatory alert skill](../../grc-rcm/concept/recommendations-for-a-regulatory-alert.md).

Role required: sn\_nowassist\_admin.nsa\_admin or sn\_aia.admin

## About this task

**Important:** This agentic workflow is active by default. All fields are read-only except for the Triggers and Channels and status sections. To modify other fields, clone the workflow. Currently, you can't edit agent prompts or provide feedback for training.

If you have the RCM user \[sn\_grc\_reg\_change.user\] role and the sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user role, you can generate regulatory action plans using the generate regulatory action plan agentic workflow in the Now Assist panel.

This workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change. The regulatory alert must be in the In Progress state and have impacted areas before generating an action plan.

You can add or remove AI agents from this workflow by making a copy and customizing it. For more information, about copying agentic workflows, see [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:**

You can perform the following actions on Now Assist workflows if you have the sn\_generative\_ai.nsa\_admin role:

-   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   [Delete an agentic workflow](https://www.servicenow.com/docs/access?context=delete-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  In the Recent agentic workflows and AI agents activity section, open the workflows configuration page by selecting **Generate regulatory action plan**.

3.  Select the Define key requirements section to review the following fields and confirm that the get regulatory analysis workflow meets your requirements.

    |Field|Description|
    |-----|-----------|
    |Workflow Name|Generate regulatory action plan.|
    |Workflow description|This agentic workflow supports regulatory change management users in handling regulatory alerts. The workflow helps users implement regulatory change and action tasks by analyzing similar past alerts and identifying the impacted areas.|
    |List of steps|Instructions for the LLM service.|

    |Name|Description|Tools and knowledge sources|Model support|Active|
    |----|-----------|---------------------------|-------------|------|
    |Regulatory change task planning agent|Regulatory change task planning agent identifies the optimal steps for working on a regulatory alert by referencing the past similar regulatory alert details and impacted areas of the current regulatory alert.|Get action plan from similar historical alerts and Create final action plan|Available|Active|

<table id="table_bjh_f1q_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

LLM providers

</td><td>

Model providers that this agentic workflow doesn’t support.All model providers are supported by the get regulatory analysis agentic workflow.

</td></tr></tbody>
</table>4.  Review how user and data access is defined to confirm that the default settings meet your requirements by selecting **Define security controls**.

    |Field|Description|
    |-----|-----------|
    |Decision type|Allow if|
    |Roles|sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user|
    |User Authenticated|Not applicable|
    |Active|Active|

    **Note:** This section defines which users can access and interact with this agentic workflow. An access control list \(ACL\) has been automatically generated.

<table id="table_sjz_rdq_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User identity type

</td><td>

Dynamic user

</td></tr><tr><td>

Approved role\(s\)

</td><td>

-   sn\_grc\_reg\_change.user
-   sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user


</td></tr></tbody>
</table>    **Note:**

    The user identity type that this agentic workflow runs under determines the roles and the data access permissions derived from them. Remember, when agentic workflows can access data, they can also share that data with the human user who interacts with them. [Learn more about access control list rules](https://www.servicenow.com/docs/csh?topicname=access-control-rules&version=latest).

5.  Select **Add triggers** and configure conditions that start the workflow, such as when a new regulatory alert is created.

    Triggers can include record conditions, schedules, or inbound email.

    For more information, see [Add a trigger to an agentic workflow](https://www.servicenow.com/docs/access?context=add-trigger-aw&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

6.  Define where alerts and summaries are delivered \(for example, the Now Assist panel or Regulatory alert record\) by selecting **Channels and status**.

    For more information, see [Select channels and access for an agentic workflow](https://www.servicenow.com/docs/access?context=channels-access-aw&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

7.  Select **Save and test**.


## What to do next

Use the Testing playground to [test your new agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) using example utterances.

Verify that tasks are generated and grouped by impacted areas. If the activation fails, check the roles and skill configuration.

After confirming that the workflow performs as expected, you can get started by selecting **Generate action plan** from the Ask Now Assist action menu on a regulatory alert page or by selecting **Generate Regulatory Action Plan** from the Now Assist panel. The regulatory alert must be in the In Progress state and have impacted areas before generating an action plan.

If you have not already set up the Now Assist panel, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

