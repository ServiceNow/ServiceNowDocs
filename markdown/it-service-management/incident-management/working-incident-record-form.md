---
title: Working with incident record form
description: Once an incident is created, you can use the incident record form to perform various actions to track, process and resolve the incident.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Working with incident record form

Once an incident is created, you can use the incident record form to perform various actions to track, process and resolve the incident.

On the incident form, you can perform actions to manage and resolve the incident:

-   If you want to mail the incident record, click the more options icon \(![More options icon](../../change-management/image/more-options.png)\) in the title bar and select **Email**.

    The user who requested the incident and the user who is assigned to the incident are automatically populated in the list of recipients.

-   When an incident is created from a case, the Customer Service with Service Management plugin \(com.sn\_cs\_sm\) is installed and you have a customer service agent \(sn\_customerservice\_agent\) role, you can view the **Customer Cases** tab in the Related Links section of the Incident form. This tab contains the list of the customer cases associated with the incident record.
-   When there are one or more interaction records associated with the incident record, you can view the **Interaction** tab in the Related Links section of the Incident form that contains the list of the interaction records.
-   When a problem record is linked to an incident or multiple incidents, the incident and problem workflow has the following features:
    -   When a fix or workaround is shared from the problem record, an event is added to the activity stream of the incident record as work notes. The event includes a brief description of the provided fix or workaround and a link to the problem record.
    -   When a Known Error \(KE\) article is linked to the problem record, an event is added to the activity stream of the incident record as work notes. The event includes the links to the problem record and the KE article.
-   Respond to an incident quickly with response templates. Some of the response templates available in the base system include Need more information and Schedule meeting response templates. The response templates can be used with communication channels such as form channel, SMS and email. The form channel enables you to access the response templates from the incident record, copy the response templates texts to the clipboard from the incident form to be shared in the work notes, comments or other communication channels. For more information on defining and configuring the response templates for incident tables in Service Operations Workspace, see [Response templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/response-templates-templated-snippets.md).
-   A **Primary device health** link appears on the Related Links section of the Incident form. Select to launch the Digital End-User Experience application and device health page for the selected CI in Service Operations Workspace on a separate browser tab. This tab enables agents to view all the available metrics and the device health for the selected CI, which were collected by DEX. You can also access this feature using the **View device health** option on the classic U16 CI record.

    **Note:**

    -   DEX requires a separate entitlement.
    -   This link is available to the agent only if the following conditions are met:
        -   The selected CI is of type Device, which is also known as Endpoint.
        -   The DEX plugin is installed on the instance. For more information on DEX, see [Digital End-User Experience](../../digital-end-user-experience/concept/dex-landing.md).
        -   The DEX agent is installed on the selected CI.

