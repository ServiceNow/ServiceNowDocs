---
title: Configure the Google Gemini Cloud Assist agent
description: Configure the Google Gemini Cloud Assist agent to use the Gemini Cloud Assistant observability skill in the manage alerts autonomously agentic workflow. Once configured, the skill gathers information to help you investigate alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-config-google-cloud.html
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure the manage alerts autonomously agentic workflow, Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the Google Gemini Cloud Assist agent

Configure the Google Gemini Cloud Assist agent to use the Gemini Cloud Assistant observability skill in the manage alerts autonomously agentic workflow. Once configured, the skill gathers information to help you investigate alerts.

## Before you begin

Before configuring the Google Gemini Cloud Assist agent, you must do the following:

-   Install Now Assist for IT Operations Management \(ITOM\).
-   [Integrate Google Cloud Platform \(GCP\) events with Event Management.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/gcp-events-integration.md)
-   Download the JSON private key file from your Google Cloud project and gather the following credentials: Google project ID, service account email, and private key ID.
-   Create a keystore file and password by following the steps in .
-   Set up the following Google Cloud project settings and permissions. For detailed instructions, navigate to the Gemini for Google Cloud documentation and search for `Create a Cloud Assist investigation`.
    -   Enable the required APIs for your Google Cloud project.
    -   Assign the Investigation Creator role to the service account.
    -   Give the service account read-access to the resources that you want it to investigate.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Google Gemini Cloud Assist Agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Connection Name**|Name of your Google Gemini Cloud Assist connection. This name helps you identify it later. For example, `Google Gemini Cloud Assist agent connection`.|
    |**Google Project ID \(project\_id\)**|Identifier for the Google Cloud project that contains the relevant service account. For example, `project-12345`.|
    |**Service Account Email \(client\_email\)**|Email address assigned to your Google Cloud service account. The agent uses this email address to authenticate with the Google Cloud project.|
    |**Private Key ID \(private\_key\_id\)**|Identifier for the private key associated with your Google Cloud service account.|
    |**Keystore Password**|Password that protects the keystore file that you upload below.|
    |**Keystore**|File that contains your authentication credentials for the Google Cloud service account. Upload this file in `.jks` format.|

5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Google Gemini Cloud Assist agent to use it in the manage alerts autonomously agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Google Gemini Cloud Assist agent, and turn on the agent in the Select channels and status screen.

To learn more about using the Google Gemini Cloud Assist agent in the manage alerts autonomously agentic workflow, see [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md).

**Parent Topic:**[Configure the manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/configure-manage-alerts-autonomously-workflow.md)

