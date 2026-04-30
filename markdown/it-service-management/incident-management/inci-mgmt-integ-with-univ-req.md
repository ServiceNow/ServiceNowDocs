---
title: Universal Request integration - Incident Management
description: Incident Management integrates with Universal Request to provide incident-related service as unified services to users. The integration helps users to have a single service desk.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Universal Request integration - Incident Management

Incident Management integrates with Universal Request to provide incident-related service as unified services to users. The integration helps users to have a single service desk.

Install and configure the Universal Request Integration for the Incident Management plugin \(com.snc.incident.universal\_request\). The integration provides the following configurations and functionalities:

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
-   The **Routing reason** field appears on the incident form when an itil agent routes an incident back to the universal request.
-   On the record producer, if you select the **Create Universal Request** check box, a new incident created from that record producer automatically creates a universal request record. This universal request record is associated with the incident record.
-   You can activate the **Create Universal Request for Incident** business rule and create incidents using any channel, such as record producer, virtual agent support, email, and so on. When you do this, a universal request record is automatically created. This universal request record is associated with the incident record. The incident is added as a primary ticket to the universal request record. By default, this business rule works as follows:
    -   The rule is inactive. To activate this business rule, navigate to **System Defination** &gt; **Business Rules** &gt; **Create Universal Request for Incident**, and then select **Active** check box to activate this business rule.
    -   The rule is not applicable to child incidents for which the parent incident is associated as a primary ticket to the universal request record.
-   When a universal request record is automatically created based on the incident, Incident record information is copied from the incident record fields to the universal request record fields. An incident manager with admin role can customize and configure the fields using the **Create UR Mappings** and **Create UR Information** tabs in the Mapping Configuration form for incidents in Universal Request. For more information, see [Mapping configuration](https://www.servicenow.com/docs/access?context=ur-direct-transfer-config-form&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

## Visibility of Incidents to a requester

The requesters cannot view the incidents that are associated with the Universal Request records. Instead, the requesters can only view the Universal Request record using the following ways:

-   On ServiceNow AI Platform, you can access the universal request records under **Self-Service** &gt; **Universal Requests**.
-   On Service Portal, you can access the universal request records under **Service Portal** &gt; **Requests**.

## Suppression of email notifications

If any incident is a part of Universal Request, then the notifications sent to the caller from an Incident are suppressed. In all other incident email notifications, the universal request number is displayed instead of the incident number.

## Requester Actions on Service Portal

For an Universal Request record that has an incident-related as its primary task, an Actions widget with the requester actions is displayed. The actions can be **Resolve**, **Reopen**, or **Close** depending on the state of the incident.

-   **[Request Universal Request integration for Incident Management](../task/request-univ-req-integration-for-im.md)**  
To activate the integration between Incident Management and Universal Request, request the Universal Request: Integration for Incident management plugin \(com.snc.incident.universal\_request\) through the Now Support Customer Service system. This plugin includes demo data and activates related plugins if they are not already active.
-   **[Create incident from Universal Request](../task/create-incident-from-univ-req.md)**  
Create an incident from a universal request record to restore service to a customer as soon as possible. After creating the incident record, you can investigate potential solutions.
-   **[Transfer incident](../task/route-inci-to-univ-req.md)**  
Transfer the back to the Universal Request queue, or to another department with or without resolution. When you realise that the issue is not incident related, transfer the incident without any resolution to the relevant department or service. If you resolve the issue, you can transfer the incident with the resolution.
-   **[Create an associated ticket from an incident](../task/create-associated-tickets.md)**  
Create an associated ticket for another relevant department from an incident \(primary ticket\) when you realize that the issue can be resolved in that department.
-   **[Resolve, reopen, or close incident associated with universal request](../task/resolve-reopen-close-inc-sp.md)**  
Resolve, reopen, or close are actions from the **Incident Actions** widget that is available on the universal request record for the requester. The **Incident Actions** widget is available only when an incident is the primary task of a Universal Request record.
-   **[Customize fields copied from Universal Request to incident](../task/customize-fields-copied-univ-inc.md)**  
Customize fields so that the values of some fields in the universal request automatically get copied to an incident record when an incident is associated with a universal request record. It saves your time from manually entering the information every time you create an incident.
-   **[Restrict an incident access](../task/restrict-incident-access.md)**  
You can restrict an incident ticket that contains sensitive information. By marking an incident as restricted, you limit its access for the agents.

**Parent Topic:**[Incident Management integrations](inci-mgmt-integrations.md)

