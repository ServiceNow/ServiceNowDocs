---
title: Create a vendor ticket in Vendor Management Workspace
description: Create vendor tickets to monitor how quickly your vendors resolve issues for your products and services.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Create a vendor ticket in Vendor Management Workspace

Create vendor tickets to monitor how quickly your vendors resolve issues for your products and services.

## Before you begin

Role required: sn\_vlm.vendor\_manager

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Workspace**.

2.  Select the List icon.

3.  Select the incident, outage, or a service availability list to create a vendor ticket.

4.  Create a vendor ticket from an incident, outage, or a service availability.

<table id="table_aqd_py5_lwb"><thead><tr><th>

Record

</th><th>

Conditions to set for creating a vendor ticket

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

-   The incident state is **On Hold**.
-   The on hold reason is **Awaiting Vendor**.


</td></tr><tr><td>

Outage

</td><td>

The configuration item field in the outage record must be configured to a service offering.

</td></tr><tr><td>

Service availability

</td><td>

The service offering must be configured in the service availability record.

</td></tr></tbody>
</table>5.  In the **Vendor** field, select the vendor associated with the incident.

6.  In the **Vendor Ticket** field, enter a ticket or incident number provided by the vendor.

    This ticket is the vendor identification number for the issue that's being resolved by the vendor.

7.  Select **Save**.


