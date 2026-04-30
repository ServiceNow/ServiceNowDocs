---
title: Create log protection property
description: Create a log protection property to avoid the risk of log tampering.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Avoid log tampering, System logs, Logs, Platform Security]
---

# Create log protection property

Create a log protection property to avoid the risk of log tampering.

## Before you begin

Role required: admin

## Procedure

1.  If the **com.glide.security.protected\_table.enabled** property doesn't exist in the System Properties list, select **New**.

    The new system property form shows up.

2.  On the form, fill in the details

<table id="table_ph5_fns_xjb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the property as com.glide.security.protected\_table.enabled

</td></tr><tr><td>

Application

</td><td>

Application that has the property.

</td></tr><tr><td>

Description

</td><td>

Description of the property

</td></tr><tr><td>

Choices

</td><td>

 

</td></tr><tr><td>

Type

</td><td>

Value type - true or false

</td></tr><tr><td>

Value

</td><td>

Actual value of the property

</td></tr><tr><td>

Ignore cache

</td><td>

Option to ignore the cache content

</td></tr><tr><td>

Private

</td><td>

Option to make the property private-   Read roles
-   Write roles


</td></tr></tbody>
</table>3.  Select **Submit** to create the property.


