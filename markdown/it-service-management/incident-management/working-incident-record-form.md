---
title: Working with the incident record form
description: After an incident is created, you can use the incident record form to track, process, and resolve the incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/working-incident-record-form.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Working with the incident record form

After an incident is created, you can use the incident record form to track, process, and resolve the incident.

On the incident form, you can perform actions to manage and resolve the incident:

-   To email the incident record, select the more options icon \[Omitted image "more-options.png"\] Alt text: in the title bar and select **Email**.

    The user who requested the incident and the user who is assigned to the incident are automatically populated in the list of recipients.

-   If the Customer Service with Service Management plugin \(com.sn\_cs\_sm\) is installed and you have the customer service agent \(sn\_customerservice\_agent\) role, the **Customer Cases** tab appears in the Related Links section. This tab lists the customer cases associated with the incident record.
-   When interaction records are associated with the incident record, the **Interaction** tab appears in the Related Links section, listing the associated interaction records.
-   When a problem record is linked to an incident or multiple incidents, the incident and problem workflow has the following features:

    -   When a fix or workaround is shared from the problem record, an event is added to the activity stream of the incident record as work notes. The event includes a brief description of the provided fix or workaround and a link to the problem record.
    -   When a Known Error \(KE\) article is linked to the problem record, an event is added to the activity stream of the incident record as work notes. The event includes the links to the problem record and the KE article.
    For more information on the incident and problem workflow, see [Incident and problem workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/using-the-plugin.md).

-   Respond to an incident quickly with response templates. Some of the response templates available in the base system include Need more information and Schedule meeting response templates. The response templates can be used with communication channels such as form channel, SMS, and email. The form channel enables you to access the response templates from the incident record. Use it to copy the response template text to the clipboard and share it in work notes, comments, or other communication channels. For more information on defining and configuring the response templates for incident tables in Service Operations Workspace, see [Response templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/response-templates-templated-snippets.md).
-   A **Primary device health** link appears on the Related Links section of the Incident form. Select the link to launch the Digital End-User Experience application and device health page for the selected CI in Service Operations Workspace in a separate browser tab. This tab enables agents to view all the available metrics and the device health for the selected CI, which were collected by DEX. You can also access this feature using the **View device health** option on the classic U16 CI record.

    **Note:**

    -   DEX requires a separate entitlement.
    -   This link is available to the agent only if the following conditions are met:
        -   The selected CI is of type Device, which is also known as Endpoint.
        -   The DEX plugin is installed on the instance. For more information on DEX, see .
        -   The DEX agent is installed on the selected CI.

