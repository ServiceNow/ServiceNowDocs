---
title: Callback interaction features
description: Integrate callback voice capabilities and core contact center functions into Agent Workspace using Interaction Controls Component \(ICC\) to streamline call handling and enhance the agent experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Interaction Controls Component ICC integration with CCaaS callback, CCaaS callback, Interaction Controls Component \(ICC\) callback interaction features, Callback interaction features]
breadcrumb: [Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks, Integrating with contact centers, Integrate, Customer Service Management]
---

# Callback interaction features

Integrate callback voice capabilities and core contact center functions into Agent Workspace using Interaction Controls Component \(ICC\) to streamline call handling and enhance the agent experience.

## ICC Callback interaction features

The following table shows the Interaction Controls Component \(ICC\) callback interaction features on the Callback actions component:

<table id="table_n5d_rf2_1gc"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Callback actions component

</td></tr><tr><td>

Initiate a call

</td><td>

The Call number button enables you to initiate a call with the customer by dialing the number in the **Callback number** drop-down.

</td></tr><tr><td>

Redial a number

</td><td>

The Retry call button enables you to redial the number in the drop-down, when the customer doesn't answer.-   If the customer answers, resolve customer issue.
-   If customer doesn’t answer after multiple retries, agents can close the callback. The number of retries is typically left to the discretion of the agent.

</td></tr><tr><td>

Choose a callback number

</td><td>

The drop-down enables you to view the list of the available contact numbers of the customer. You can select any number in the drop-down to connect with the customer.

</td></tr><tr><td>

Close a call request

</td><td>

The Close callback button enables you to wrap up a callback request.

</td></tr><tr><td>

Transfer callback

</td><td>

Enables agents to transfer an ASAP or scheduled callback to another queue or agent before the call to the customer begins.

</td></tr><tr><td>

Manual dial

</td><td>

In manual dial method, agent dials the customer manually after viewing callback context. In this mechanism, the timer doesn’t appear on the Callback actions component.

</td></tr><tr><td>

Automatic dial

</td><td>

In automatic dial, the call automatically gets dialed after the countdown timer reaches zero. Alternatively, the agent can select the **Call number** button and manually dial the call before the timer reaches zero. In this mode, after the call ends, the callback is automatically wrapped up after the countdown timer reaches zero.

</td></tr></tbody>
</table>In the agent-first mode, the callback interaction page appears with Callback actions component and Callback context card when you accept the callback request in your inbox. In this mode, you can view the callback context card to get the callback request details before making the call. In the customer-first scenario, the callback interaction appears like any other voice interaction and the customer will already be on the call. For more information on these modes, see [Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks](interaction-controls-component-icc-callback-integration-features.md).

For more information on how to handle callback requests in the CSM/FSM Configurable Workspace, see [Manage a CCaaS callback request in the Configurable Workspace](../task/ccaas-address-callback-requests.md).

When agents are working from an unsupported workspace or they aren’t on the callback interaction page, they can manage callbacks through the Global Voice Control \(GVC\) component. This feature offers quick access to the Callback Actions component, enabling agents to initiate calls and handle active calls using the available call controls. The features described in the preceding table are available in the Global Voice control \(GVC\) for easy access to the agent. In addition to these features, you’re provided with an **Open Interaction page** link on the global call list so that you can navigate to the current callback interaction page. For more information on how to use GVC for callback interactions, see [Manage a CCaaS callback request using Global Voice Control](../task/handle-ccaas-callback-gvc.md).

![Callback interaction page with Callback actions component, Callback context card, and Global Voice control (GVC) with Callback actions.](../image/Interaction_Interface.png "Callback interactions page with ICC Callback features and callback context card")

## Additional callback features

In addition to the ICC callback features, the following features are available in the callback interactions.

-   Callback context card: The callback context card on the Callback interaction page provides the details of the callback request. For more information on the callback context card, see [Callback context card](csm-native-voice-record-page.md#section-callback-context).

    This feature uses the Interaction table, which includes a reference to the Callback \[sys\_cs\_callback\] table. The Callback table, in turn, references the Callback Context \[sys\_cs\_callback\_context\] table to store the information related to the callback request.

    Agents with the callback\_writer role can edit callback tasks. They can select the appropriate option from the Reason for the call field to manage callback requests effectively for both sales and customer service scenarios.

    For sales-related callbacks, the relevant options in the Reason for the call field are Customer Survey, Sales Discovery, Product Feedback, and Customer Relationship Building. For customer service-related callbacks, the relevant options in the Reason for the call field are Product Issue, Order Issue, Billing Issue, and Other issue.

    In UI Builder, the callback context card is configured to use the [Lookup component](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades), which can be used to look up a record on any table in card format. It also uses a data resource that returns the callback task for the specific interaction.

-   Preview duration: The preview time measures the time between the agent accepting the callback in their inbox and the agent dialing the customer from the CSM/FSM Configurable Workspace. You can view the preview time in the Interaction table.
-   Callback list: You can view the callback interactions assigned to you by navigating to the My callbacks list on the List page of the CSM/FSM Configurable workspace.

**Related topics**  


[Implement the Interaction Controls Component \(ICC\) for contact center voice call and callback integrations](../task/enable-icc-for-ccaas.md)

[Plugin requirements for voice and callback integrations with contact centers](../task/plugin-requirements-for-external-call-routing-integration-for-contact-centers.md)

[Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks](interaction-controls-component-icc-callback-integration-features.md)

[Manage a CCaaS callback request in the Configurable Workspace](../task/ccaas-address-callback-requests.md)

[Manage a CCaaS callback request using Global Voice Control](../task/handle-ccaas-callback-gvc.md)

[Components installed with Omnichannel Callback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/omnichannel-callback/installed-with-omnichannel-callback.md)

