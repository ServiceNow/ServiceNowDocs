---
title: Create a knowledge article from an incident using an article template
description: Provide a resolution for an issue by creating a knowledge article from an incident with fields defined in an article template.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Create a knowledge article from an incident using an article template

Provide a resolution for an issue by creating a knowledge article from an incident with fields defined in an article template.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

Activate the [KCS Integration for Incident Management](activate-kcs-integration-for-im.md) plugin \(com.snc.incident.knowledge\).

## About this task

You can create a knowledge article only when the incident is resolved and you have not already created a knowledge article from that incident.

**Note:** Incident managers with the sn\_km\_ml.knowledge\_curation\_user role can use the Demand Insights for Incidents dashboard to identify which incidents have no or insufficient knowledge coverage. For more information, refer Demand Insights for Incidents dashboard.

## Procedure

1.  Navigate to **All** &gt; **Incidents** &gt; **Resolved**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open a resolved incident record.

3.  Access the Incident-KCS article - HTML form using one of the following methods:

    -   Under Related Links, click **Create Knowledge**.
    -   Right-click the form header and click **Create Knowledge**.
    The Incident-KCS article - HTML template provided with the base system appears. If you want to create your own article template, refer to Create an article template.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|\[Auto-generated\] Unique number to identify the knowledge article.|
    |Knowledge base|Knowledge base in which the article is stored. The Incident KCS Article is stored in the \[kb\_template\_incident\_kcs\_article\] table.|
    |Category|\[Auto-generated\] The value of this field is automatically provided from the **Category** field of the knowledge.|
    |Valid to|Date after which the knowledge article is deleted from the database. After this date, the article does not appear in the search result.|
    |Confidence|Maturity of an article based on its completeness and reusability.|
    |Version|\[Auto-generated\] Displays the article version number, which is incremented when changes are made to a published article.|
    |Workflow|\[Auto-generated\] Workflow that is followed for creating the knowledge article. For more information, refer Knowledge workflows .|
    |Source Task|\[Auto-generated\] Incident record from which you have created the article.|
    |Attachment link|Check box to automatically download an attached article instead of opening the article, when you access an article.|
    |Display attachments|Check box to display attachments in the knowledge article. The attachments appear below the article text.|
    |Governance|An attribute of an article that enables you to control sensitive, critical, or regulated information. Not all articles have the same requirement for compliance reviews. Some articles are based on the collective experience of the people who use the articles \(experience-based\). Other articles have policy or legal information that require tight control \(compliance-based\).|
    |Short description|Brief description of the knowledge article.|
    |Issue|Information on the cause of the incident.|
    |Resolution|Method used to resolve the incident.|

    **Note:** The **Confidence** and **Governance** fields appear when the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) is activated. For more information, see Managing the KCS article state.

5.  Click **Submit**.

    A knowledge article is created. The article record is listed in the Knowledge related list.


