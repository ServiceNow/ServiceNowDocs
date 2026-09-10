---
title: Configure LINE
description: Configure LINE integration with CSM omnichannel so customers can contact support from LINE and agents can manage those interactions in the CRM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/omnichannel-consumer-messaging-line.html
release: australia
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 2
keywords: [LINE messaging, omnichannel integration, customer service]
breadcrumb: [Configure consumer messaging apps, Configure omnichannel, Configure, Customer Service Management]
---

# Configure LINE

Configure LINE integration with CSM omnichannel so customers can contact support from LINE and agents can manage those interactions in the CRM Workspace.

Here's an example of routing customer inquiries from the LINE messaging application to CSM agents.

A restaurant group uses LINE with CSM omnichannel so customers can contact support from LINE for reservations, order issues, and general questions. In the example workflow, the administrator configures the LINE channel, connects it to CSM, defines how customer messages create interactions or cases, and sets routing rules. The administrator also prepares CRM Workspace so agents can review the customer context, respond to the inquiry, and send updates back through LINE.

\[Omitted image "omnichannel-line-integration-MMASSET0022373.png"\] Alt text: Use case example workflow displaying routing LINE customer inquiries to CSM agents.

## LINE implementation workflow

The following workflow shows how to install, configure and implement LINE messaging with CSM workflows.

<table id="table_etn_sgk_zjc"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

1. [Install Conversational Integration with LINE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-line-install.md)

</td><td>

Install the Conversational Integration with LINE plugin from the ServiceNow Store.

</td><td>

Admin, System Admin

</td></tr><tr><td>

2. [Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/va-integration-messaging-apps.md)

</td><td>

Review the Virtual Agent messaging app integration framework to understand supported channels, account linking patterns, and live agent transfer capabilities.

</td><td>

Admin

</td></tr><tr><td>

3. [Configure Conversational Integration with LINE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-line-configure.md)

</td><td>

Set up LINE Business Account credentials and OAuth tokens.

</td><td>

LINE Platform Mgr, Admin

</td></tr><tr><td>

4. [Set up Conversational Integration with LINE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-line-setup.md)

</td><td>

Configure the LINE channel in Conversational Interfaces Console.

</td><td>

Admin

</td></tr><tr><td>

5. [Integrating LINE with Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrate-line-csm.md)

</td><td>

Link LINE channel to CSM and configure interaction creation rules.

</td><td>

Admin

</td></tr><tr><td>

6. [Capturing information from a user in a LINE chat conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-line-capture-info.md)

</td><td>

Configure data capture rules to extract customer information from LINE messages.

</td><td>

Admin

</td></tr><tr><td>

7. [Configure case routing and assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-case-routing-assignment.md)

</td><td>

Define routing rules to assign LINE cases to appropriate teams.

</td><td>

Admin

</td></tr><tr><td>

8. \(Optional\) [AWA for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/awa-csm-overview.md)

</td><td>

Enable and configure Advanced Work Assignment \(AWA\) for intelligent agent assignment.

</td><td>

Admin

</td></tr><tr><td>

9. [Set up CRM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-set-up.md)

</td><td>

Set up and configure the CSM workspace to integrate with the LINE application.

</td><td>

Admin

</td></tr><tr><td>

10. [Transfer LINE chat conversations to live agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-line-live-agent-conv.md)

</td><td>

Configure live agent handoff from Virtual Agent to CSM agents.

</td><td>

Admin

</td></tr></tbody>
</table>