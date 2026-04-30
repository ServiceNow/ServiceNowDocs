---
title: Integrating Virtual Agent with Workflow Studio workflows
description: The workflows of ServiceNow Workflow Studio can be integrated within ServiceNow Virtual Agent topics. You can then use these workflows in Virtual Agent conversations.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Workflow Studio workflows

The workflows of ServiceNow® Workflow Studio can be integrated within ServiceNow Virtual Agent topics. You can then use these workflows in Virtual Agent conversations.

**Note:** If you have turned on and set up Now Assist in Virtual Agent, you can use the base system conversational actions and subflows from the Virtual Agent Designer home page. You currently can't create conversational subflows in Virtual Agent Designer, you can only view and edit them. Conversational subflows can be created, tested, and deleted only in Workflow Studio. For more information on conversational actions and subflows, see [Conversational actions](https://www.servicenow.com/docs/access?context=conversational-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) and [Conversational subflows](https://www.servicenow.com/docs/access?context=conversational-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US). You can still integrate actions and subflows that are not conversational from Workflow Studio into Virtual Agent topics through Virtual Agent Designer. The following content is only relevant to actions or subflows that cannot be made conversational in Workflow Studio.

You can integrate Workflow Studio actions and subflows as follows:

-   Add the actions or subflows to Virtual Agent conversations.
-   Use actions created for another product in Virtual Agent conversations.
-   Create conversations that call workflows directly in the conversation. For example, users can place catalog requests, create incidents, or input information securely.

In Virtual Agent conversations, you can use actions to trigger workflows that are custom built in an application \(such as Workflow Studio\) or workflows of the third-party applications and products available in the Integration Hub. Integrations built using Workflow Studio and Integration Hub help to ensure a high level of resiliency and performance.

If an action in the workflow is slow to respond or appears to be waiting, topic authors see a relevant error message.

By default, a scheduled job checks the conversation flow every 120 seconds. For more information about scheduled jobs, see [Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

You can change this interval as needed. To change the interval, see [Specify the action workflow timeout](../task/va-fdih-action-timeout.md).

## Integrate workflows of third-party products available on the Integration Hub

You can use the Integration Hub to create end-to-end digital workflows and automate processes that integrate the ServiceNow AI Platform® with any third-party application, platform, or data.

For example, you can use one of the 100 prebuilt spokes available on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). These prebuilt spokes include popular applications, such as Microsoft Azure, Workday, and Okta.

For more information about the ServiceNow Integration Hub, see [ServiceNow IntegrationHub – natively integrate ServiceNow with anything](https://www.youtube.com/watch?v=YGlGwGBNEfY).

-   **[Add actions or subflows to Virtual Agent topics](../task/setup-flow-designer-va-properties.md)**  
Use the Action utility to integrate ServiceNow Workflow Studio workflows in Virtual Agent topics. The Action utility node triggers the required Workflow Studio workflows used in the Virtual Agent conversation.
-   **[Virtual Agent secure password inputs](va-secure-inputs.md)**  
The **Include a password input** toggle switch on the Action utility properties sheet lets you enter passwords securely for use in Virtual Agent conversations.
-   **[Workflow Studio scoped application requirements for secure inputs](va-fd-app-reqs-secure-inputs.md)**  
Adhere to the following scoped application requirements to implement secure \(password2\) inputs in your Virtual Agent topics.
-   **[Test the Action utility](../task/test-flow-designer-va-integration.md)**  
Test the Action utility to make sure that the integrated action works as intended in the conversation.
-   **[Specify the action workflow timeout](../task/va-fdih-action-timeout.md)**  
Set the length of time before the Workflow Studio Integration Hub action workflow times out.

**Parent Topic:**[Exploring other Virtual Agent features](exploring-other-vad-features.md)

