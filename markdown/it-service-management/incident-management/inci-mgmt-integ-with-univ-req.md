---
title: Incident Management integration with Universal Request
description: Incident Management integrates with Universal Request so users can get incident-related services through a single service desk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/inci-mgmt-integ-with-univ-req.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Incident Management integration with Universal Request

Incident Management integrates with Universal Request so users can get incident-related services through a single service desk.

Install and configure the Universal Request Integration for the Incident Management plugin \(com.snc.incident.universal\_request\). The integration provides the features described in the following sections.

## Features of the Incident Management integration with Universal Request

The integration of Incident Management with Universal Request provides the following features:

-   The Universal Request form has the UI action to create an incident. The following fields are copied by default from the universal request record to the incident record when a new incident is created:

    -   universal\_request
    -   short\_description
    -   description
    -   caller\_id
    -   opened\_by
    An incident manager can customize the fields using the system property **sn\_inc\_uni\_req.incident.universal\_request.copy\_fields**.

-   The **Universal Request** field appears on the Incident form only when an incident is associated with a universal request record.
-   The **Routing reason** field appears on the Incident form when an itil agent routes an incident back to the universal request.
-   On the record producer, if you select the **Create Universal Request** check box, a new incident created from that record producer automatically creates a universal request record. This universal request record is associated with the incident record.
-   You can activate the **Create Universal Request for Incident** business rule and create incidents using any channel, such as record producer, virtual agent support, or email. When you do this, a universal request record is automatically created. This universal request record is associated with the incident record. The incident is added as a primary ticket to the universal request record. By default, this business rule works as follows:
    -   The rule is inactive. To activate this business rule, navigate to **System Definition** &gt; **Business Rules** &gt; **Create Universal Request for Incident**, and then select the **Active** check box.
    -   The rule is not applicable to child incidents for which the parent incident is associated as a primary ticket to the universal request record.
-   When a universal request record is automatically created based on the incident, information is copied from the incident record fields to the universal request record fields. An incident manager with the admin role can customize and configure the fields using the **Create UR Mappings** and **Create UR Information** tabs in the Mapping Configuration form for incidents in Universal Request. For more information, see [Mapping configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/ur-direct-transfer-config-form.md).

## Visibility of incidents to a requester

The requesters cannot view the incidents that are associated with the Universal Request records. Instead, the requesters can only view the Universal Request record in the following ways:

-   On ServiceNow AI Platform, you can access the universal request records under **Self-Service** &gt; **Universal Requests**.
-   On Service Portal, you can access the universal request records under **Service Portal** &gt; **Requests**.

## Suppression of email notifications

If any incident is a part of Universal Request, then the notifications sent to the caller from the incident are suppressed. In all other incident email notifications, the universal request number is displayed instead of the incident number.

## Requester actions on Service Portal

For an Universal Request record that has an incident as its primary task, an Actions widget with the requester actions is displayed. The actions can be **Resolve**, **Reopen**, or **Close** depending on the state of the incident.

-   **[Request Universal Request integration for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/request-univ-req-integration-for-im.md)**  
To activate the integration between Incident Management and Universal Request, request the Universal Request: Integration for Incident management plugin \(com.snc.incident.universal\_request\) through the Now Support Customer Service system. This plugin includes demo data and activates related plugins if they are not already active.
-   **[Create an incident from Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/create-incident-from-univ-req.md)**  
Create an incident from a universal request record to restore service to a customer as soon as possible. After creating the incident record, you can investigate potential solutions.
-   **[Transfer an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/route-inci-to-univ-req.md)**  
Transfer an incident back to the Universal Request queue or to another department, with or without a resolution. If the issue isn't related to an incident, transfer it without a resolution to the relevant department or service.
-   **[Create an associated ticket from an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/create-associated-tickets.md)**  
Create an associated ticket for another relevant department from an incident \(primary ticket\) when you realize that the issue can be resolved in that department.
-   **[Resolve, reopen, or close incident associated with universal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/resolve-reopen-close-inc-sp.md)**  
As a requester, resolve, reopen, or close an incident from the Incident Actions widget on a universal request record. The widget is available only when an incident is the primary task of the universal request.
-   **[Customize fields copied from Universal Request to incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/customize-fields-copied-univ-inc.md)**  
Customize which fields are automatically copied from a universal request to an associated incident record. This eliminates manual data entry each time you create an incident.
-   **[Restrict access to an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/restrict-incident-access.md)**  
Restrict access to an incident that contains sensitive information so that only authorized agents can access it.

**Parent Topic:**[Incident Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/inci-mgmt-integrations.md)

