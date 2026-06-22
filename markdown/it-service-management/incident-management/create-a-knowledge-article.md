---
title: Create a knowledge article from an incident using an article template
description: Provide a resolution for an issue by creating a knowledge article from an incident with fields defined in an article template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/create-a-knowledge-article.html
release: zurich
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# Create a knowledge article from an incident using an article template

Provide a resolution for an issue by creating a knowledge article from an incident with fields defined in an article template.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

Activate the [KCS Integration for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/activate-kcs-integration-for-im.md) plugin \(com.snc.incident.knowledge\).

## About this task

You can create a knowledge article only when the incident is resolved and you have not already created a knowledge article from that incident.

**Important:**

In Zurich patch 4 and later, the behavior varies by view:

-   Platform \(classic\) view- Selecting **Create Knowledge** opens the Knowledge interceptor page.
-   Service Operations Workspace- Selecting **Create knowledge** opens the KCS article template directly.

This procedure documents the Platform \(classic\) view flow.

**Note:** Incident managers with the sn\_km\_ml.knowledge\_curation\_user role can use the Demand Insights for Incidents dashboard to identify which incidents have no or insufficient knowledge coverage. For more information, refer [Demand Insights for Incidents dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management/demand-insights-incidents-dashboard.md).

## Procedure

1.  Navigate to **All** &gt; **Incidents** &gt; **Resolved**.

2.  Open a resolved incident record.

3.  Access the Incident-KCS article - HTML form using one of the following methods:

    -   Under Related Links, select **Create Knowledge**.
    -   Select and hold \(or right-click\) the form header and select **Create Knowledge**.
    The behavior depends on your view and release:

    -   **Platform \(classic\) view \(Zurich patch 4 and later\):** the Knowledge interceptor page opens. Complete the interceptor flow to reach the KCS article template.
    -   In Service Operations Workspace, the **Incident-KCS article - HTML** template opens.
    The base system **Incident-KCS article - HTML** template appears by default. To use a custom template instead, refer to [Create an article template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management/create-a-new-article-templates.md).

    **Important:**

    In Zurich patch 4 and later, the platform \(classic\) view opens the Knowledge interceptor page before the KCS article template. Complete the interceptor flow to reach the KCS template article. This step does not apply to Service Operations Workspace.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|\[Auto-generated\] Unique number to identify the knowledge article.|
    |Knowledge base|Knowledge base in which the article is stored. The Incident KCS Article is stored in the \[kb\_template\_incident\_kcs\_article\] table.|
    |Category|\[Auto-generated\] The value of this field is automatically provided from the **Category** field of the knowledge.|
    |Valid to|Date after which the knowledge article is deleted from the database. After this date, the article does not appear in the search result.|
    |Confidence|Maturity of an article based on its completeness and reusability.|
    |Version|\[Auto-generated\] Displays the article version number, which is incremented when changes are made to a published article.|
    |Workflow|\[Auto-generated\] Workflow that is followed for creating the knowledge article. For more information, refer [Knowledge workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management/r_KnowledgeWorkflows.md) .|
    |Source Task|\[Auto-generated\] Incident record from which you have created the article.|
    |Attachment link|Check box to automatically download an attached article instead of opening the article, when you access an article.|
    |Display attachments|Check box to display attachments in the knowledge article. The attachments appear below the article text.|
    |Governance|An attribute of an article that enables you to control sensitive, critical, or regulated information. Not all articles have the same requirement for compliance reviews. Some articles are based on the collective experience of the people who use the articles \(experience-based\). Other articles have policy or legal information that require tight control \(compliance-based\).|
    |Short description|Brief description of the knowledge article.|
    |Issue|Information on the cause of the incident.|
    |Resolution|Method used to resolve the incident.|

    **Note:** The **Confidence** and **Governance** fields appear when the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) is activated. For more information, see [Managing the KCS article state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management/managing-kcs-article-states.md).

5.  Select **Submit**.

    A knowledge article is created. The article record is listed in the Knowledge related list.


