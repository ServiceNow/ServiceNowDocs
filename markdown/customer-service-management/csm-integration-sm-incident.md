---
title: CSM integration with Incident Management
description: Integration with the Incident Management application enables customer service agents to create incident records from cases or associate existing incident records to cases.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CSM integration with IT Service Management overview, Integrating with IT Service Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# CSM integration with Incident Management

Integration with the Incident Management application enables customer service agents to create incident records from cases or associate existing incident records to cases.

With this integration, customer service agents can:

-   Create an incident from a case.
-   Associate an existing open incident to a case.
-   Remove an associated incident from a case.
-   View the following in the case work notes:
    -   Incident state changes.
    -   Additional comments added to the incident record.

**Note:** A case can be associated with one incident. If a case is already associated with an incident, the **Create Incident** item does not appear on the Additional Actions menu.

## Plugins

Integration with Incident Management requires the Customer Service with Service Management plugin \(com.sn\_cs\_sm\).

## Roles

The following roles enable customer service agents to view and create incidents for customer service cases.

-   sn\_incident\_read
-   sn\_incident\_write

For more information, see [Assign CSM/ITSM integration roles](../task/assign-csm-itsm-integration-roles.md#).

## Determining the incident priority, impact, and urgency

When creating an incident from a case:

-   If the incident data lookup is active, the system copies the case priority to the incident priority and calculates the incident impact and urgency based on the Priority Data Lookup \[dl\_u\_priority\] table.
-   If the Incident data lookup is inactive, the system uses these default settings for the incident fields:
    -   Priority: 5 - Planning
    -   Impact: 3 - Low
    -   Urgency: 3 - Low

## Synchronizing data between the incident and the case

Work notes are synchronized from the incident to the case when:

-   The incident state changes. If the incident state changes to On Hold, the hold reason is copied to the case work notes.
-   The incident is resolved or closed. The incident resolution notes and resolution code are copied to the case work notes.
-   Additional comments are added to the incident.

**Note:** When an incident is created or an existing incident is associated with a case, notification from the incident is suppressed if the caller is an external user \(contact or consumer\).

