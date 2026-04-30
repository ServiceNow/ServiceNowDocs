---
title: Create a robot license distribution record in RPA Hub
description: Define the consumption and distribution of licenses by creating a robot license distribution record in RPA Hub.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create a robot license distribution record in RPA Hub

Define the consumption and distribution of licenses by creating a robot license distribution record in RPA Hub.

## Before you begin

You must do this task in the classic environment.

Familiarize yourself with license distribution in RPA Hub concepts. For more information, see [Robot license distribution in RPA Hub](../concept/license-rpa-hub.md).

Install the RPA Hub. For more information, see [Install Robotic Process Automation \(RPA\) Hub](../../rpa-core/task/install-rpa.md).

Role required: sn\_rpa\_fdn.rpa\_admin

## About this task

If the instance you are using is not domain separated, then create the license distribution record in the global domain.

If the instance you are using is domain separated, create a license distribution record in a top-down approach, starting with the top-level or primary domain. Do not create the license distribution record in the global domain. If the parent domain does not have a license distribution record, you can't create a license distribution record for child domains.

You can create only one license distribution record per domain.

A license distribution record is necessary to create any robots in the instance, for each domain.

For example, a domain separated instance with top domain and two child domains has 20 unattended robot licences and 45 attended robot licences. In each domain, you could assign 5 unattended robot licences and 15 attended robot licences. The **Available from Parent** field will show 10 unattended robot licences and 15 attended robot licences that are not yet assigned. When a robot is created in a child domain, a license is automatically utilized in that domain. In a license distribution record of a child domain, the **Utilized** field will show the value as 1 and the **Available to use or distribute** field will show the value as 4, which is remaining assigned licenses that are not yet utilized.

If you have more robots than the assigned licenses, then the instance or the specific domain \(and its child domains\) gets locked. Then, the robots do not execute automations in the current and child domains.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Robots License Distribution**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated robot license distribution record number.This is a read-only field.

</td></tr><tr><td>

Available from Parent \(Unattended\)

</td><td>

Maximum number of the unattended robot licenses that are available from the parent domain and are not yet assigned.This is a read-only field.

</td></tr><tr><td>

Assigned \(Unattended\)

</td><td>

Total number of the assigned licenses for unattended robots in the current domain.This value must not exceed the value in the **Available from Parent \(Unattended\)** field.

</td></tr><tr><td>

Utilized \(Unattended\)

</td><td>

Total number of utilized licenses by the non-retired unattended robots that are created in the current domain.This is a read-only field.

</td></tr><tr><td>

Available to use or distribute \(Unattended\)

</td><td>

Maximum number of the unattended robot licenses that can be either distributed to the child domains or can be utilized in the current domain.This field shows difference of assigned and utilized licenses.

This is a read-only field.

</td></tr><tr><td>

Domain

</td><td>

Name of the current domain.Only one record can be created per domain. Once created, this record can only be edited and can't be deleted.

This is a read-only field.

</td></tr><tr><td>

Available from Parent \(Attended\)

</td><td>

Maximum number of the attended robot licenses that are available from the parent domain and are not yet assigned.This is a read-only field.

</td></tr><tr><td>

Assigned \(Attended\)

</td><td>

Total number of the assigned licenses for attended robots in the current domain.This value must not exceed the value in the **Available from Parent \(Attended\)** field.

</td></tr><tr><td>

Utilized \(Attended\)

</td><td>

Total number of utilized licenses by the non-retired attended robots that are created in the current domain.This is a read-only field.

</td></tr><tr><td>

Available to use or distribute \(Attended\)

</td><td>

Maximum number of the attended robot licenses that can be either distributed to the child domains or can be utilized in the current domain.This field shows difference of assigned and utilized licenses.

This is a read-only field.

</td></tr></tbody>
</table>    **Note:** Enter the values for the **Assigned \(Unattended\)** and **Assigned \(Attended\)** fields. Based on these values, the remaining fields are auto-populated.

4.  Select **Submit**.


**Related topics**  


[Update a robot license distribution record in RPA Hub](update-license-record-rpa.md)

