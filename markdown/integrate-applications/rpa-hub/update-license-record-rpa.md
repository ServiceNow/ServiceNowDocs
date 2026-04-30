---
title: Update a robot license distribution record in RPA Hub
description: Update a robot license distribution record in RPA Hub to evaluate the consumption and distribution of licenses in your organization.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Update a robot license distribution record in RPA Hub

Update a robot license distribution record in RPA Hub to evaluate the consumption and distribution of licenses in your organization.

## Before you begin

Familiarize yourself with license distribution in RPA Hub concepts. For more information, see [Robot license distribution in RPA Hub](../concept/license-rpa-hub.md).

You must do this task in the classic environment.

Role required: sn\_rpa\_fdn.rpa\_admin

## About this task

For example, a domain separated instance with top domain and two child domains has 20 unattended robot licences and 45 attended robot licences. In each domain, you could assign 5 unattended robot licences and 15 attended robot licences. The **Available from Parent** field will show 10 unattended robot licences and 15 attended robot licences that are not yet assigned. When a robot is created in a child domain, a license is automatically utilized in that domain. In a license distribution record of a child domain, the **Utilized** field will show the value as 1 and the **Available to use or distribute** field will show the value as 4, which is remaining assigned licenses that are not yet utilized.

If you have more robots than the assigned licenses, then the instance or the specific domain \(and its child domains\) gets locked. Then, the robots do not execute automations in the current and child domains.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Robots License Distribution**.

2.  Open the license record that you want to update.

3.  Update the following fields as appropriate.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned \(Unattended\)

</td><td>

Total number of the assigned licenses for unattended robots in the current domain.This value must not exceed the value in the **Available from Parent \(Unattended\)** field.

</td></tr><tr><td>

Assigned \(Attended\)

</td><td>

Total number of the assigned licenses for attended robots in the current domain.This value must not exceed the value in the **Available from Parent \(Attended\)** field.

</td></tr></tbody>
</table>4.  Select **Update**.


**Related topics**  


[Create a robot license distribution record in RPA Hub](create-lua-record.md)

