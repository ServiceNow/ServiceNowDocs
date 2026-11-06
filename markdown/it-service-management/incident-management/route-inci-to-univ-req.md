---
title: Transfer an incident
description: Transfer an incident back to the Universal Request queue or to another department, with or without a resolution. If the issue isn't related to an incident, transfer it without a resolution to the relevant department or service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/route-inci-to-univ-req.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident Management integration with Universal Request, Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Transfer an incident

Transfer an incident back to the Universal Request queue or to another department, with or without a resolution. If the issue isn't related to an incident, transfer it without a resolution to the relevant department or service.

## Before you begin

Role required: agent to whom the ticket is assigned

An incident must be associated with a Universal Request record.

## Procedure

1.  Open the incident to transfer.

2.  Select **Transfer**.

    \[Omitted image "route-to-ur.png"\] Alt text: Transfer incident to Universal Request

3.  In the Transfer Ticket dialog box, fill in the fields.

    **Note:** The fields that appear depend on your transfer type configuration. For more information, see [Universal Request properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/ur-properties.md).

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Option to transfer the incident to another department or back to Universal Request.

</td></tr><tr><td>

Department

</td><td>

Select the department from the list.

</td></tr><tr><td>

Service

</td><td>

Select the specific service of the chosen department.**Note:** This field does not appear if you have selected **Transfer to Department** in **Action**

</td></tr><tr><td>

Transfer reason

</td><td>

Select the reason from the list.

</td></tr><tr><td>

Transfer notes

</td><td>

Brief description for routing the primary ticket, passed to the Universal Request routing agent.

</td></tr><tr><td>

Copy additional comments and attachments

</td><td>

Clear the check box to transfer the ticket without additional comments and attachments. By default, all attachments and comments are transferred.**Note:** Work notes are not copied while transferring.

</td></tr></tbody>
</table>4.  Select **Transfer**.


**Parent Topic:**[Incident Management integration with Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/inci-mgmt-integ-with-univ-req.md)

