---
title: Configure Engagement Messenger for Playbooks
description: Configure certain Engagement Messenger settings to enable public sector end users to create and track requests. With Engagement Messenger, public sector users can access self-service and chat features from third-party web applications outside of the ServiceNow environment.Configure Engagement Messenger settings for creating and tracking non-emergency service requests.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable communication channels, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Engagement Messenger for Playbooks

Configure certain Engagement Messenger settings to enable public sector end users to create and track requests. With Engagement Messenger, public sector users can access self-service and chat features from third-party web applications outside of the ServiceNow environment.

-   Create an Engagement Messenger module. For more information on implementing Engagement Messenger, see Set up Engagement Messenger.
-   Be familiar with customizing the Engagement Messenger module. For details, see Customize the feature configuration of Engagement Messenger.
-   Activate the Agent Chat plugin \(com.glide.interaction.awa\).
-   Activate the Virtual Agent plugin \(com.glide.cs.chatbot\), which requires a subscription.
-   Activate the Customer Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\), which requires a subscription.

## Configure Engagement Messenger for Service Request Playbook

Configure Engagement Messenger settings for creating and tracking non-emergency service requests.

### Before you begin

Role required: sn\_csm\_ec.ec\_admin or admin

### About this task

Public sector end users can create and track service requests in Engagement Messenger. They can choose from a catalog of pre-packaged service requests that are provided with the Service Request Playbook application. If Virtual Agent is implemented, they can use the pre-built Virtual Agent conversation, Create a Service Request, to submit and update non-emergency service requests from Engagement Messenger. You must enable the Government Service Catalog and this pre-built Virtual Agent conversation in Engagement Messenger.

### Procedure

1.  In Engagement Messenger, navigate to **All** &gt; **Engagement Messenger** &gt; **Modules**.

2.  Customize the Catalog feature to use the Government Service Catalog, which provides the pre-packaged, non-emergency services that users can select from when creating a service request.

    1.  From the **Features** section, open the **Catalog** feature.

    2.  Select **Edit** to search for and then add the Government Service Catalog.

3.  Customize the Chat feature by enabling the pre-built Virtual Agent conversation for creating a service request.

    1.  From the **Features** section, open the **Chat** feature.

    2.  Under **Reference chat**, find and select the **Create a Service Request** conversation topic.

4.  Select **Update**.


