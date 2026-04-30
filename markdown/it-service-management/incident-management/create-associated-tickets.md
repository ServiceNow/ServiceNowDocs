---
title: Create an associated ticket from an incident
description: Create an associated ticket for another relevant department from an incident \(primary ticket\) when you realize that the issue can be resolved in that department.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Universal Request integration - Incident Management, Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Create an associated ticket from an incident

Create an associated ticket for another relevant department from an incident \(primary ticket\) when you realize that the issue can be resolved in that department.

## Before you begin

Ensure that the incident has an associated Universal Request record.

Role required: Ensure you have one of the following roles.

-   The agent to whom the incident is assigned.
-   The agent who belongs to the assignment group to whom the incident is assigned

## Procedure

1.  Navigate to **Incidents** &gt; **All**.

2.  Open the incident record from which you want to create an associated ticket.

3.  Click **Create Associated Ticket**.

    ![Create associated ticket from incident](../image/inci-form-asso-tick.png)

4.  In the Create Associated Ticket dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Department|Department for which you want to create an associated ticket.|
    |Short description|A brief description of the issue for which the associated ticket is created.|
    |Description|A detailed description of the issue for which the associated ticket is created.|
    |Work notes|A brief description of the issue. You can communicate this issue to the Universal Request Routing agent or to the agent of the department for which the associated ticket is created.|

5.  Click **Create**.


## Result

The ticket is created for the relevant department and is associated with the universal request record. You can view the associated tickets in the Associated Tickets related list of the Universal Request form.

**Note:** When an associated ticket is created, the information is copied from the fields of the universal request record to the fields of the associated ticket record. You can use the **Associated Ticket Information** and **Associated Ticket Mappings** tabs of the Mapping Configuration form for incidents. For more information, see [Mapping configuration](https://www.servicenow.com/docs/access?context=ur-direct-transfer-config-form&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

**Parent Topic:**[Universal Request integration - Incident Management](../concept/inci-mgmt-integ-with-univ-req.md)

