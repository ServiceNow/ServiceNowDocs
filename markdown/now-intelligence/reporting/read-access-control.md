---
title: Report execution security
description: When a report is run, report\_view access control lists \(ACLs\) are evaluated on the table and table fields that the report is based on. If no report\_view ACL exists, there is a fallback check on table-level read ACL roles.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-07"
reading_time_minutes: 1
breadcrumb: [Report\_view access control, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report execution security

When a report is run, report\_view access control lists \(ACLs\) are evaluated on the table and table fields that the report is based on. If no report\_view ACL exists, there is a fallback check on table-level read ACL roles.

The fallback read ACL is controlled by the system property **glide.report.report\_view.read\_acl**.

This property has three possible values. The default value is `enforce`.

-   **ignore**

    No evaluation is conducted against the read ACL and all users can see the report.

-   **enforce**

    If no report\_view ACL for that table or table field exists, evaluation is conducted against the read ACL. Users can only view the report if they pass the read ACL.

-   **log**

    The read ACL check isn’t enforced if there is no report\_view ACL for that table or table field, but the administrator can see in the logs which users would have been blocked if the security check was enforced.


it isn’t recommended to change the system property to ignore or log as the read ACL fallback provides an extra level of protection when viewing a report.

**Note:** The fallback table-level read ACL check applies only to roles, not to scripts or conditions. If a table-level read ACL has roles and scripts or roles and conditions, or roles, scripts, and conditions, only the roles are evaluated.

![](../image/read-acl-evaluation.png)

**Parent Topic:**[Report\_view access control](report-view-access-control.md)

