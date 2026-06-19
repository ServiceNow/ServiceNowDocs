---
title: Create a knowledge article from an incident
description: When you are ready to close an incident, you can create a knowledge article so the next time the issue comes up the resolution is easy to find.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/incident-management/create-knowledge-incident.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create knowledge article, Managing incidents, Incident Management, IT Service Management]
---

# Create a knowledge article from an incident

When you are ready to close an incident, you can create a knowledge article so the next time the issue comes up the resolution is easy to find.

## Before you begin

KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\) must be activated. When activated, **Incident Create Knowledge** business rule does not run. For more information, see [Activate KCS Integration for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/activate-kcs-integration-for-im.md).

Role required: itil, sn\_incident\_write, or admin

## About this task

When an incident is closed automatically or by the caller, a draft knowledge article is created.

## Procedure

1.  Open a resolved incident that you want to close.

2.  Perform one of the following methods to create a knowledge article from an incident:

    -   Under Related Links, select **Create Knowledge**.
    -   Right-click the form header and select **Create Knowledge**.
    **Note:** The **Create Knowledge** related link is visible only if:

    -   Incident must be in **Resolved** state.
    -   A knowledge article does not exist for the same incident.
3.  Select **Close incident**.

    A new draft knowledge article is created. The content in the fields listed in the following table is copied from the Incident form to the Knowledge form.

    |Field on Incident form|Field on Knowledge form|
    |----------------------|-----------------------|
    |Short description|Short description|
    |Additional comments|Text|
    |Number|Source|

    The **Knowledge** related list on the Incident form is populated with the new draft knowledge article. The draft article does not appear in the knowledge base \(KB\) for users until it is reviewed and published.

    If the **Knowledge submission** workflow \(glide.knowman.submission.workflow\) is enabled from the System Properties \[sys\_properties\] table, the content in the **Short description** and **Additional comments** fields of the incident form become a knowledge submission instead of an article. The **KB Submissions** related list on the Incident form is populated with the new knowledge submission. For more information on creating a knowledge article and workflows, see Create knowledge from incident and Knowledge workflows.

    When the KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\) is not activated, **Knowledge** check box is visible instead of **Create Knowledge** related link. You can select the check box and enter a resolution in the**Additional comments \(Customer visible\)** field and then close the incident. In such case, a knowledge article is created automatically using the **Incident Create Knowledge** business rule.


## What to do next

-   To confirm that draft articles are created, check the **Knowledge** related list on the incident form.
-   To open a draft article, go to **Knowledge** &gt; **My Knowledge Articles** and open the draft by its KB number.
-   If the article does not appear in **My Knowledge Articles** and the **glide.knowman.submission.workflow** property is enabled, the system creates the article as a knowledge submission. Look for it in the **KB Submissions** related list on the incident form.

    **Note:** Draft articles appear in the knowledge base only after they are reviewed and published. If the draft is still missing from **My Knowledge Articles**, contact your knowledge administrator to verify the configuration of your KCS plugin.


