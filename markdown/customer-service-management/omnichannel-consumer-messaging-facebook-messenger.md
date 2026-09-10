---
title: Configure Facebook Messenger
description: Configure Facebook Messenger as a consumer messaging channel within ServiceNow Customer Service Management \(CSM\). Enabling Facebook Messenger as a channel lets customers start support conversations. Those conversations route to service agents, who manage them in the CRM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/omnichannel-consumer-messaging-facebook-messenger.html
release: australia
topic_type: concept
last_updated: "2026-07-17"
reading_time_minutes: 2
keywords: [Facebook Messenger, omnichannel, consumer messaging, integration]
breadcrumb: [Configure consumer messaging apps, Configure omnichannel, Configure, Customer Service Management]
---

# Configure Facebook Messenger

Configure Facebook Messenger as a consumer messaging channel within ServiceNow Customer Service Management \(CSM\). Enabling Facebook Messenger as a channel lets customers start support conversations. Those conversations route to service agents, who manage them in the CRM Workspace.

Here's an example of a customer service journey for Wi-Fi router troubleshooting showing Facebook Messenger integration with omnichannel.

A customer contacts the router manufacturer through Facebook Messenger because a new laptop can't connect to the home Wi-Fi. CSM matches the Facebook ID to the customer account when available in the system and creates a Messaging interaction. When the user is not logged in, a live agent does a lookup and verifies in the CRM Workspace to link the customer account. Virtual Agent asks the customer to select the product, then suggests relevant knowledge articles for Wi-Fi troubleshooting. The customer follows an article and reconnects the laptop, so CSM logs the interaction as resolved and closes the chat. If the issue continues, the customer can escalate to a live agent, who receives the account history, device details, and the articles already reviewed.

\[Omitted image "omnichannel-facebook-messenger-integration-MMASSET0022344.png"\] Alt text: Use case example workflow displaying customer service journey for a Wi-Fi router troubleshooting issue.

## Facebook Messenger implementation workflow

The following workflow shows how to [Configure Conversational Integration with Facebook Messenger](https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/messg-fbm-configure.html)

<table id="table_n5b_syf_yjc"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

1. [Install Conversational Integration with Facebook Messenger](https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/messg-fbm-install.html)

</td><td>

Install required Plugins for Conversational integration and the Facebook Messenger application.

</td><td>

Admin

</td></tr><tr><td>

2. [Set up Conversational Integration with Facebook Messenger](https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/messg-fbm-setup.html)

</td><td>

Integrate  Facebook Messenger with your  ServiceNow  instance using the  Conversational Integration with Facebook Messenger application.

 Facebook Messenger settings:

1.  [Set up a Facebook developer account](https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/messg-fbm-setup.html#:~:text=Set%20up%20a%20Facebook%20developer%20account.)

2.  [Create a Facebook app](https://developers.facebook.com/docs/messenger-platform/getting-started/app-setup)

3.  [Review Messenger Platform Policy](https://developers.facebook.com/docs/messenger-platform/policy/policy-overview) and [Pre-launch checklist](https://developers.facebook.com/docs/messenger-platform/prelaunch-checklist)

4.  [Submit app for review](https://developers.facebook.com/docs/messenger-platform/#review---submission-process)

5.  [Create a Facebook page within the Facebook app created earlier](https://www.facebook.com/pages/creation/)

6.  [Enable Facebook Messenger](https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/messg-fbm-setup.html#:~:text=Enable%20Facebook%20Messenger)


</td><td>

Admin

</td></tr><tr><td>

3. [Configure and integrate Virtual Agent](https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-integration-messaging-apps.html)

</td><td>

Integrate the  Customer Service  Virtual Agent with  Facebook Messenger to enable virtual agent conversations in the messenger.

</td><td>

Admin

</td></tr><tr><td>

4. [Transfer Facebook Messenger chat conversations to live agents](https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/messg-fbm-live-agent-conv.html)

</td><td>

Configure the  Advanced Work Assignment application to transfer a  Facebook Messenger chat conversation initiated by a requester \(customer contact or consumer\) to a live agent.

</td><td>

Admin

</td></tr><tr><td>

5. [Activate Advanced Work Assignment \(AWA\)](https://www.servicenow.com/docs/r/conversational-interfaces/advanced-work-assignment/implement-awa.html)

</td><td>

To implement  Advanced Work Assignment , complete these initial configuration and setup steps.

</td><td>

Admin

</td></tr><tr><td>

6. [Set up CSM Configurable Workspace](https://www.servicenow.com/docs/r/customer-service-management/csm-config-workspace-set-up.html)

</td><td>

CSM Configurable Workspace is a user interface that provides customer service agents with the tools they need to assist customers, answer questions, and resolve issues quickly and efficiently.

 Set up  CSM Configurable Workspace for your agents so they can engage with customers, answer questions, create cases, and resolve issues.

</td><td>

Admin

</td></tr></tbody>
</table>