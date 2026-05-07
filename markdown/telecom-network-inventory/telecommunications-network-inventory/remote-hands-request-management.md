---
title: Remote Hands Request Management
description: Remote Hands enables your customers to request services for their equipment housed in your datacenters. Your customers can seamlessly submit and track service requests on the Customer Service Management , eliminating the need for phone calls, emails, or site visits.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Remote Hands Request Management

Remote Hands enables your customers to request services for their equipment housed in your datacenters. Your customers can seamlessly submit and track service requests on the Customer Service Management , eliminating the need for phone calls, emails, or site visits.

Remote Hands Request Management is an independent plugin. It enables customers to request services for equipment in your datacenters by connecting them with onsite agents who handle remote hands requests. Customers can submit and track their service requests directly through the ServiceNow Customer Service Management \(CSM\) portal. This removes the need for phone calls, emails, or site visits.

The following are the tasks that your customers can request via the Customer Service Management portal:

1.  Power Usage Enquiry
2.  Equipment Installation
3.  Equipment Restart
4.  Other Remote Hands

If their request doesn’t fall under the listed options, users can select the **Other Remote Hands** option and describe the requested service in the Additional Information section. Remote Hands Agents handling requests at your site can review submitted requests and update the corresponding case records directly from the CSM/FSM Configurable Workspace.

## Remote Hands Request Management Case Creation

Remote Hands Request Management is implemented using the Remote Hands Case table \(sn\_remote\_hands\_case\). This case table stores customer service requests related to remote hands activities. When a customer submits a Remote Hands request through the Customer Service Management \(CSM\) portal, the form data is captured and mapped to the corresponding fields in the Remote Hands Case table \(sn\_remote\_hands\_case\). On submission, a Remote Hands Case record is automatically created in the system.

The Remote Hand Case table \(sn\_remote\_hands\_case\) extends from the Customer Service Case table \(sn\_customerservice\_case\) in the Customer Service Management portal \(CSM\). By extending the base table, it inherits the standard fields and functionality of the Case table \(sn\_customerservice\_case\) table.

## Remote Hands Request Management Roles

<table id="id_khk_fy1_k3c"><tbody><tr><td>

Role

</td><td>

Permissions

</td><td>

Description

</td></tr><tr><td>

Remote Hands Agent \(sn\_remote\_hands.agent\)

</td><td>

Grants Create, Read, and Write access to records in the Remote Hands Case table.

</td><td>

Remote Hands Agents can review submitted requests and update the corresponding case records from the CSM/FSM Configurable Workspace.

</td></tr><tr><td>

Remote Hands User \(sn\_remote\_hands.user\)

</td><td>

Grants Read-only access to records in the Remote Hands Case table.

</td><td>

Remote Hands User can view the records in the Remote Hands Case table.

</td></tr><tr><td>

DCIM User \(sn\_ni\_core\_dcim\_user\):

</td><td>

Grants access to submit and review the submitted Remote Hands Request in the CSM portal.

</td><td>

The DCIM User role is intended for your customers. This role inherits the Remote Hands User \(sn\_remote\_hands.user\) and \(sn\_customerservice.customer\) role. Users assigned to this role can submit Remote Hands requests using the Remote Hands request form available in the Customer Service Management \(CSM\) portal.

</td></tr></tbody>
</table>## Accessing Remote Hands Request Management Interfaces

DCIM Users submit their Remote Hands in the **Customer Service Management portal \(CSM\)**. To learn more, see [Submit a Remote Hands Request](../task/submit-remote-hands-request.md).![CSM portal](../image/csm-portal.png)

The Remote Hands Agent can review the submitted remote hands request, by navigating to: **CSM/FSM Configurable Workspace** &gt; **Select list icon \(![list icon](../image/ni-workspace-list-icon.png)** &gt; **Remote Hands Cases**

The following sections are made available:

-   **My Cases**: View all Remote Hands cases assigned to you.
-   **My Open**: Active cases with open status assigned to the logged in agent working on the case is displayed.
-   **All**: View all Remote Hands cases in the system.

![CSM/FSM Configurable workspace](../image/csm-fsm-workspace.png)

On opening a Remote Hands Case record, the fields mapped from the Remote Hands request form in the CSM portal are displayed in the case record. The Remote Hands Agent can further modify case fields. Add Work Notes for customers to view, update state, and close the case. To learn more, see [Update a Remote Hands Request](../task/update-a-remote-hands-request.md).

## Remote Hands Case Archival Policy

Remote Hands cases that were created two years ago are archived, regardless of whether the case is active or closed. This archival policy helps prevent performance degradation by reducing the number of active records in the system. The archive rule is condition-based and can be modified.

Navigate to **CSM/FSM Configurable workspace** &gt; **All** &gt; **Archive Rules** to access Remote Hands Case Archival Policy.

To learn more about the required plugin for Remote Hands Request Management, see [Remote Hands Request](remote-hands-request.md)

