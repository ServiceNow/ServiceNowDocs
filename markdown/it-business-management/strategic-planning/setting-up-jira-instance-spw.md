---
title: Setting up a Jira instance for SPW Jira Integrations
description: Establish a connection between Strategic Planning Workspace \(SPW\) and Jira using a Jira instance record.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Setting up a Jira instance for SPW Jira Integrations

Establish a connection between Strategic Planning Workspace \(SPW\) and Jira using a Jira instance record.

Before connecting SPW and Jira, you need a Jira instance record and Jira connection alias in your ServiceNow instance.

Based on the type of your Jira instance, perform the following steps:

-   For Jira Cloud:
    1.  [Create a child alias for the Jira Spoke alias](../task/create-child-alias-for-jira-spoke-alias.md).
    2.  Integrate your ServiceNow instance with your Jira account using OAuth. See [Option 1: Using OAuth authentication \(Authorization Code grant type\)](https://www.servicenow.com/docs/access?context=setup-jira-spk-opt2&version=australia&pubname=australia-integrate-applications&section=setup-jira-spk-oauth&ft:locale=en-US)

        **Note:** To create credential record and connection record in this task, use the child alias that you created earlier and not the parent Jira Spoke.

    3.      4.      5.  [Create a Jira instance record in ServiceNow AI Platform](../task/create-jira-instance.md).
-   For Jira Server or Data center:
    1.  [Create a child alias for the Jira Spoke alias](../task/create-child-alias-for-jira-spoke-alias.md).
    2.  Set up a MID server. See [Tips to set up your MID Server](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0535145).
    3.  [Create Personal Access Token \(PAT\) in Jira](../task/create-personal-access-token-pat-in-jira-server-data-center.md).
    4.  [Using the PAT, set up connection &amp; credentials for the child alias](../task/create-connection-and-credentials.md).
    5.  [Create a Jira instance record in ServiceNow AI Platform](../task/create-jira-instance.md).

After successfully setting up the Jira instance record, proceed to connect Strategic Planning Workspace and Jira. For more information, see [Connect SPW to Jira](../task/connect-spw-to-jira.md).

-   **[Create a child alias for Jira Spoke alias for SPW Jira Integrations](../task/create-child-alias-for-jira-spoke-alias.md)**  
Create a child connection &amp; credential alias that will be used to connect to Jira later, to enable integration between Strategic Planning and Jira.
-   **[Create Personal Access Token in Jira Server/Data Center for SPW Jira Integrations](../task/create-personal-access-token-pat-in-jira-server-data-center.md)**  
Create a Personal Access Token \(PAT\) for your Jira Server/Data Center instance, which is later used to create a connection between Strategic Planning and Jira.
-   **[Create connection and credentials for SPW Jira Integrations](../task/create-connection-and-credentials.md)**  
Using your Jira instance details, create a connection and credential for the child alias, which is used to enable the two-way sync of work item updates between Strategic Planning Workspace and Jira.
-   **[Create Jira instance for SPW Jira Integrations](../task/create-jira-instance.md)**  
Create a Jira instance record which is later used to connect Strategic Planning Workspace and Jira.

**Parent Topic:**[Configuring SPW Jira Integrations](configuring-spw-jira-integrations.md)

