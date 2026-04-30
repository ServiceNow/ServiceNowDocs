---
title: Application quota rule form
description: A description of the fields on the Application Quota Rule form.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Platform performance, Maintain and monitor, Administer]
---

# Application quota rule form

A description of the fields on the Application Quota Rule form.

<table id="table_drb_nv1_rp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name to identify the rule.

</td></tr><tr><td>

Application

</td><td>

The scoped application's name. To change this field, use the application picker to change the application. This field cannot be Global.

</td></tr><tr><td>

Order

</td><td>

A number that represents the priority of the quota transaction in relation to other quotas.

</td></tr><tr><td>

Active

</td><td>

A check box that determines if this rule is active \(selected\).

</td></tr><tr><td>

Log only

</td><td>

When checked, transactions are not canceled by a quota violation, but entries are added to the local host log that indicate the transactions are violating the quota rule.An entry is added to the Transaction Cancellation Log where the log only field is set.

</td></tr><tr><td>

Maximum Events

</td><td>

The maximum number of events allowed during the update period.

</td></tr><tr><td>

Maximum Jobs

</td><td>

The maximum number of jobs allowed during the update period.

</td></tr><tr><td>

Condition

</td><td>

The conditions that determine when the transaction quota applies. The condition builder displays conditions that are only applicable to transactions. For example, Foreground is true.

</td></tr><tr><td>

Description

</td><td>

A description of the transaction quota.

</td></tr></tbody>
</table>**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

