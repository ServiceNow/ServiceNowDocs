---
title: Set up Issue Auto Resolution for ITSM Virtual Agent
description: Users with the virtual\_agent\_admin or admin role can configure Virtual Agent settings to indicate discoverable topics, set business rules, and more.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up ITSM Virtual Agent, ITSM Virtual Agent, IT Service Management]
---

# Set up Issue Auto Resolution for ITSM Virtual Agent

Users with the virtual\_agent\_admin or admin role can configure Virtual Agent settings to indicate discoverable topics, set business rules, and more.

## Before you begin

Role required: admin or virtual\_agent\_admin

-   [Activate Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/activate-virtual-agent.md) to use Virtual Agent as a response channel.
-   [Set up ITSM Virtual Agent](setup-itsm-virtual-agent.md)

    Install the ITSM Virtual Agent Conversations app, which includes the ITSM NLU Model for Virtual Agent Conversations. Request this app from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).


## About this task

Most of the Issue Auto Resolution functionality is included with the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin. More functionality is available in the ITSM Virtual Agent Conversations Store App. Issue Auto Resolution is automatically enabled.

## Procedure

1.  Train the Machine Learning model.

    Train the Issue Auto Resolution Machine Learning model before activating the Auto Resolution Configuration record.

    **Note:** The query on the Incident table must have the minimum number of records that you specify in the **glide.platform\_ml.api.min\_agent\_zero\_records** system property to train the model. The default value of this property is 300000 and should not be increased because training the model can fail with more than 300,000 records. Ensure that the conditions that you specify in the Auto Resolution configuration record return less than 300,000 records before you click **Train**. For more information about predictive intelligence properties, see [Predictive Intelligence properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/predictive-intelligence-properties.md).

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

    2.  Under ITSM Virtual Agent \(IAR\), click **View Settings**.

    3.  Select the target table.

    4.  Under the **Details** tab, go to the Machine Learning Model section.

    5.  Click **Train**.

        The **Training Progress** field displays the percentage of training complete and updates whenever the form is refreshed.

    6.  When the **Training Status** field displays `Solution Complete`, select the **Active** property.

    7.  Set a **Retrain Frequency** to define how often the Machine Learning model automatically retrains.

        Users with the admin or virtual\_agent\_admin role can also manually retrain the model at any time.

2.  Change any mappings for Issue Auto Resolution intents to matched ITSM Virtual Agent topics.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

    2.  Under **Issue Auto Resolution \(IAR\)**, select **View Settings**.

    3.  Select the target table.

    4.  Under the **Auto Resolution Intent Topic Maps** tab, view the default mappings for the intents and matched topics and select the topic to change.

        You can modify mappings, but only supported Issue Auto Resolution intents and active Virtual Agent topics are available for mapping.

        These records are inactive by default. To use them, duplicate the template topics to create and publish them. After associating the intent to the topic of choice, make the intent topic map active.

    5.  For a given Issue Auto Resolution intent, double-click the corresponding **Matched topic**, select a different topic, and select **Save**.


**Parent Topic:**[Setting up ITSM Virtual Agent](../concept/setting-up-itsm-va.md)

