---
title: Create a knowledge article from an incident
description: When you are ready to close an incident, you can create a knowledge article so the next time the issue comes up the resolution is easy to find.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create knowledge article, Managing incidents, Incident Management, IT Service Management]
---

# Create a knowledge article from an incident

When you are ready to close an incident, you can create a knowledge article so the next time the issue comes up the resolution is easy to find.

## Before you begin

KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\) must be activated. When activated, **Incident Create Knowledge** business rule does not run. For more information, see [Activate KCS Integration for Incident Management](activate-kcs-integration-for-im.md).

Role required: itil, sn\_incident\_write, or admin

**Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

## About this task

When an incident is closed automatically or by the caller, a draft knowledge article is created.

## Procedure

1.  Open a resolved incident that you want to close.

2.  Perform one of the following methods to create a knowledge article from an incident:

    -   Under Related Links, click **Create Knowledge**.
    -   Right-click the form header and click **Create Knowledge**.
    **Note:** The **Create Knowledge** related link is visible only if:

    -   Incident must be in **Resolved** state.
    -   A knowledge article does not exist for the same incident.
3.  Click **Close incident**.

    A new draft knowledge article is created. The content in the fields listed in the following table is copied from the Incident form to the Knowledge form.

    |Field on Incident form|Field on Knowledge form|
    |----------------------|-----------------------|
    |Short description|Short description|
    |Additional comments|Text|
    |Number|Source|

    The **Knowledge** related list on the Incident form is populated with the new draft knowledge article. The draft article does not appear in the knowledge base \(KB\) for users until it is reviewed and published.

    If the **Knowledge submission** workflow \(glide.knowman.submission.workflow\) is enabled from the System Properties \[sys\_properties\] table, the content in the **Short description** and **Additional comments** fields of the incident form become a knowledge submission instead of an article. The **KB Submissions** related list on the Incident form is populated with the new knowledge submission. For more information on creating a knowledge article and workflows, see [Create knowledge from incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/t_ApproveKnowledgeSubmission.md) and [Knowledge workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/r_KnowledgeWorkflows.md).

    When the KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\) is not activated, **Knowledge** check box is visible instead of **Create Knowledge** related link. You can select the check box and enter a resolution in the**Additional comments \(Customer visible\)** field and then close the incident. In such case, a knowledge article is created automatically using the **Incident Create Knowledge** business rule.


## What to do next

To see the draft articles, navigate to **Knowledge** &gt; **My Knowledge Articles** and then open the draft article by its KB number in the Knowledge form.

