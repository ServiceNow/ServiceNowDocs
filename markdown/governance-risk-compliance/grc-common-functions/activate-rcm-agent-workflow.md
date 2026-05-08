---
title: Activate the get regulatory analysis agentic workflow
description: Configure and activate the get regulatory analysis agentic workflow that uses AI agents to enrich regulatory alerts with external context, classification, summarization, and recommended potential impacted items.
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

# Activate the get regulatory analysis agentic workflow

Configure and activate the get regulatory analysis agentic workflow that uses AI agents to enrich regulatory alerts with external context, classification, summarization, and recommended potential impacted items.

## Before you begin

Install the Now Assist for IRM plugin \(sn\_irm\_gen\_ai\).

The regulatory alert recommendation and summarization skills are required to generate enriched insights and identify impacted areas. For more information, see [AI-generated recommendations for a regulatory alert skill](../../grc-rcm/concept/recommendations-for-a-regulatory-alert.md) and [AI-driven regulatory alert summarization skill](../concept/regulatory-alert-summarization.md).

Role required: sn\_nowassist\_admin.nsa\_admin or sn\_aia.admin

## About this task

**Important:** This agentic workflow is active by default. All fields are read-only except for the Triggers and Channels and status sections. To modify other fields, clone the workflow. Currently, you can't edit agent prompts or provide feedback for training.

If you have the RCM user \[sn\_grc\_reg\_change.user\] role and the sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user role, you can get regulatory analysis using the get regulatory analysis agentic workflow in the Now Assist panel.

This workflow uses web search to enhance alert context, summarizes the alert, and recommends potential impacts on citations, policies, and control objectives to support faster and more accurate compliance decisions. The regulatory alert must be in the New or In Progress state to generate analysis.

**Note:** You can add or remove AI agents from this workflow by making a copy and customizing it. For more information, about copying agentic workflows, see Duplicate an agentic workflow.

You can perform the following actions on Now Assist workflows if you have the sn\_generative\_ai.nsa\_admin role:

-   Duplicate an agentic workflow
-   Modify an agentic workflow
-   Delete an agentic workflow

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  In the Recent agentic workflows and AI agents activity section, open the workflows configuration page by selecting **Get Regulatory Analysis**.

3.  Select the Define key requirements section to review the following fields and confirm that the Get Regulatory Analysis workflow meets your requirements.

    |Field|Description|
    |-----|-----------|
    |Workflow Name|Get regulatory analysis.|
    |Workflow description|The get regulatory analysis agentic workflow assists regulatory change management professionals by analyzing regulatory alerts, enriching them with relevant contextual data, and recommending potential impacts on internal Citations, Policies, Control objectives, and so on. This workflow streamlines the review process, enabling faster and more accurate decision-making to maintain compliance with evolving regulatory requirements.|
    |List of steps|Instructions for the LLM service.|

<table id="id_o2v_k4c_cfd"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Tools and knowledge sources

</th><th>

Model support

</th><th>

Active

</th></tr></thead><tbody><tr><td>

Regulatory alert recommendation agent

</td><td>

The process of generating recommendations for impacted areas when a regulatory alert is raised. It involves fetching recommendation contexts, retrieving template-specific recommendations, and summarizing the results for the user.

</td><td>

-   Get Recommendation Context
-   Getting recommendation related to a template


</td><td>

Available

</td><td>

Active

</td></tr><tr><td>

Regulatory alert enrichment agent

</td><td>

The Regulatory alert enrichment agent is responsible for enriching the regulatory alert by adding more context collected using web search.

</td><td>

Regulatory alert enriched insights updater

</td><td>

Available

</td><td>

Active

</td></tr></tbody>
</table><table id="table_bjh_f1q_ghc"><thead><tr><th>

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
    |Roles|sn\_grc\_comp\_genai.reg\_change\_ai\_user|
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
-   snc\_required\_script\_writer\_permission


</td></tr></tbody>
</table>    **Note:**

    The user identity type that this agentic workflow runs under determines the roles and the data access permissions derived from them. Remember, when agentic workflows can access data, they can also share that data with the human user who interacts with them. [Learn more about access control list rules](https://www.servicenow.com/docs/csh?topicname=access-control-rules&version=latest).

5.  Select **Add triggers** and configure conditions that start the workflow, such as when a new regulatory alert is created.

    Triggers can include record conditions, schedules, or inbound email.

    For more information, see Add a trigger to an agentic workflow.

6.  Define where alerts and summaries are delivered \(for example, the Now Assist panel or Regulatory alert record\) by selecting **Channels and status**.

    For more information, see Select channels and access for an agentic workflow.

7.  Select **Save and test**.


## What to do next

Use the **Testing** playground to test your new agentic workflow using example utterances.

Verify that the enriched insights and recommendations are generated. If activation fails, check roles and skill configuration.

After confirming the workflow performs as expected, you can get started by selecting **Get analysis** from the Ask Now Assist action menu on a regulatory alert page or by selecting **Get Regulatory Analysis** from the Now Assist panel. The regulatory alert must be New or In Progress to generate analysis.

If you have not already set up the Now Assist panel, for more information see, Activate the Now Assist panel standard chat.

