---
title: Schedule Optimization integration user access requirements
description: Describes the access requirements for the shared integration user account used by Schedule Optimization.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-25"
reading_time_minutes: 1
breadcrumb: [Schedule Optimization components, Reference, Field Service Management]
---

# Schedule Optimization integration user access requirements

Describes the access requirements for the shared integration user account used by Schedule Optimization.

## User access requirements

Schedule Optimization uses a dedicated service account `sharedservice.worker` to execute database queries during optimization. This account does not have admin access. Read access for all OOTB fields on the work order task table is already granted to this account. However, if a Task Filter references a custom field, a custom table, or a table other than the default work order task table to submit work orders, you must grant the `sharedservice.worker` account the admin role. If the role is not granted, affected tasks may be skipped during optimization, which can cause double booking or incorrect assignments.

To add the role, navigate to **User Administration** &gt; **Users**, search by **User ID** for `sharedservice.worker`, and open the record. In the **Roles** related list, select **Edit** to add the roles required to grant read access to the fields and tables referenced in your task filter.

**Parent Topic:**[Schedule Optimization components](schedule-optimization-components.md)

**Related topics**  


[Create a scheduling attribute for Schedule Optimization](../task/configure-scheduling-attributes.md)

