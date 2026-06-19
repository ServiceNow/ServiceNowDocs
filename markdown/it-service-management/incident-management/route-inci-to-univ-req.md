---
title: Transfer incident
description: Transfer the back to the Universal Request queue, or to another department with or without resolution. When you realise that the issue is not incident related, transfer the incident without any resolution to the relevant department or service. If you resolve the issue, you can transfer the incident with the resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/route-inci-to-univ-req.html
release: zurich
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Universal Request integration - Incident Management, Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Transfer incident

Transfer the back to the Universal Request queue, or to another department with or without resolution. When you realise that the issue is not incident related, transfer the incident without any resolution to the relevant department or service. If you resolve the issue, you can transfer the incident with the resolution.

## Before you begin

Role required: agent to whom the ticket is assigned to

Associate an incident with a Universal Request record.

## Procedure

1.  Open the incident that you want to transfer.

2.  Select **Transfer**.

    \[Omitted image "route-to-ur.png"\] Alt text: Transfer incident to Universal Request

3.  In the **Transfer Ticket** dialog box, provide the following details.

    **Note:** Based on your transfer type configuration, the given fields are displayed. For more information, see Universal Request properties.

    -   **Action**: Select if the case should be transferred to another department or back to Universal Request
    -   **Department**: Select the department from the list.
    -   **Service**: Select the specific service of the chosen department.

        **Note:** This field does not appear if you have selected **Transfer to Department** in **Action**

    -   **Transfer reason**: Select the reason from the list.
    -   **Transfer notes**: A brief description for routing the primary ticket that you want to pass to the UR Routing agent.
    -   **Copy additional comments and attachments**: Deselect if you do not want to transfer the ticket with additional comments and attachments. By default, all attachments and comments are transferred.

        **Note:** Work notes are not copied while transferring.

4.  Click **Transfer**.


**Parent Topic:**[Universal Request integration - Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/inci-mgmt-integ-with-univ-req.md)

