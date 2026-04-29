---
title: Configure IBM Watson Assistant as the NLU provider for Virtual Agent
description: Use the intents, entities, and utterances defined in IBM Watson Assistant and apply them as an NLU model for your Virtual Agent conversations.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure NLU in Virtual Agent, Configure, Virtual Agent, Conversational Interfaces]
---

# Configure IBM Watson Assistant as the NLU provider for Virtual Agent

Use the intents, entities, and utterances defined in IBM Watson Assistant and apply them as an NLU model for your Virtual Agent conversations.

## Before you begin

In IBM Watson Assistant, do the following:

-   In your IBM account, create a [Resource Link](https://www.ibm.com/docs/en/opw/8.3.0?topic=links-resource) in the AI \(Artificial Intelligence\) category. Once you have created the Resource Link, you should see the API key and URL:

    ![In your IBM Watson Assistant account, locate the API key and URL on the dashboard page for the Resource Link you created.](../images/ibm-watson-credentials.png)

-   In your workspace, define the intents, entities, and utterances for your NLU model.
-   Locate your workspace credentials and copy the workspace **Password**, which you must provide when setting your credentials during configuration.

In your ServiceNow instance, make sure that the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) is activated. This plugin installs the proxy agent for the IBM Watson Natural Language Understanding server plugin \(com.glide.nlu.ibmwatson.intent.discovery\), which is needed for this integration.

Role required: admin

## About this task

Configuring the IBM Watson Assistant integration involves providing IBM Watson Assistant credentials for authentication. You can set only one NLU service provider for your instance.

**Note:** If you upgraded from a previous release, the upgrade process automatically retains the IBM Watson Assistant workspace **Password** that you provided.

As of the Quebec release, Virtual Agent supports legacy version 1 URLs only:

-   Models: `https://<IBM HOST>/assistant/api/{{api_version}}/workspaces?version={{published_version}}`
-   Intents: `https://<IBM HOST>/assistant/api/{{api_version}}/workspaces/{{model_id}}/intents?version={{published_version}}&page_limit=1000`
-   Entities: `https://<IBM HOST>/assistant/api/{{api_version}}/workspaces/{{model_id}}/entities?version={{published_version}}`
-   Prediction: `https://<IBM HOST>/assistant/api/{{api_version}}/workspaces/{{model_id}}/message?version={{published_version}}`

## Procedure

1.  Set the IBM Watson endpoint in your ServiceNow instance for each of the following HTTP\(s\) Connections records:

    -   IBM Watson NLU Models
    -   IBM Watson NLU Intents
    -   IBM Watson NLU Entities
    -   IBM Watson NLU Prediction
    1.  Navigate to **All**, and then enter `http_connection.list` in the filter.

    2.  In the HTTP\(s\) Connections page, select an IBM Watson entry in the Name column to open the record.

        ![There are four IBM Watson NLU records to modify: Entities, Intents, Models, and Prediction. You must set the endpoint for each record.](../images/set-ibm-watson-endpoint.png)

    3.  Edit the URL in the **Host** and **Base path** fields to reflect the endpoint in your IBM Watson NLU account.

        ![On the form, change the Host and Base path fields to refer to your IBM Watson NLU endpoint.](../images/set-ibm-watson-endpoint-host.png)

    4.  Select **Update**.

    5.  Repeat these steps for the remaining IBM Watson records.

2.  Add the IBM Watson NLU API key in your ServiceNow instance for each of the following Basic Auth Credentials records:

    -   IBM Watson NLU Models
    -   IBM Watson NLU Intents
    -   IBM Watson NLU Entities
    -   IBM Watson NLU Prediction
    1.  Navigate to **All**, and then enter `basic_auth_credentials.list` in the filter.

    2.  In the Basic Auth Credentials page, select an IBM Watson entry in the Name column to open the record.

    3.  In the **Password** field, enter the IBM Watson NLU API key.

        ![Enter the API key name and password on the Basic Auth Credentials form for the IBM Watson NLU model.](../images/va-ibm-watson-credential-pw.png)

    4.  Select **Update**.

    5.  Repeat these steps for the remaining IBM Watson records.

3.  Make the IBM Watson NLU service active.

    1.  Navigate to **All**, and then enter `open_nlu_driver.list` in the filter.

    2.  In the Open NLU Drivers table, locate the IBM Watson Script record and in the **Active** field, set the value to true.

        ![For the IBM Watson - Script record, double-click in the Active column to change the value from false to true.](../images/open-nlu-drivers.png)

        Activating this setting adds **IBM Watson - Script active** to the list of available NLU services in Virtual Agent settings.

4.  To enable NLU in your instance, navigate to **Conversational Interfaces** &gt; **Settings**, and then do the following:

    1.  Click **Virtual Agent**.

    2.  Under Natural Language Understanding \(NLU\), click **View Settings**.

    3.  Slide the **Activate** toggle switch to enable Natural Language Understanding.

    4.  In the **NLU service provider** list, select **IBM Watson - Script**.

    5.  If you plan to use language-specific NLU models, enable the languages in the Supported NLU Languages list.

        A language is enabled if the Enabled column displays **true**. For more information, see [Enable NLU languages in Virtual Agent settings](enable-langs-va-gen-settings.md).

    6.  Click **Save**.

    IBM Watson Assistant is the NLU service provider for your instance.


**Parent Topic:**[Configure Natural Language Understanding in Virtual Agent](configure-nlu-settings.md)

