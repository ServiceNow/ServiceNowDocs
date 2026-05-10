---
title: Report\_view access control
description: The report\_view operation is a record type access control list \(ACL\) that restricts access to reports. Only users who have one of the required roles can view reports that contain the restricted resource.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report\_view access control

The report\_view operation is a record type access control list \(ACL\) that restricts access to reports. Only users who have one of the required roles can view reports that contain the restricted resource.

To create a report\_view ACL, follow the [general procedure for creating an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/t_CreateAnACLRule.md), but bearing the following points in mind:

There are two kinds of report\_view access control lists \(ACLs\): report\_view table ACLs and report\_view field ACLs. Report\_view table ACLs prevent users from viewing report or data visualization content based on the table specified in the ACL. Report\_view field ACLs prevent users from viewing reports or data visualizations that use the field specified in the ACL in the group by, row, column or aggregation settings.

For example, a report\_view field ACL grants the report\_admin role viewing access to the salary field in an HR table. When users with the itil or report\_user role access a report grouped on the salary field, they see: Access to this content denied based on report\_view field ACLs.

## Report\_view operation design considerations

Use these guidelines when creating your own report\_view operation access controls.

-   **Restrict access to reports by a required role**

    The report\_view operation only supports access restrictions based on a required role. A report\_view access control does not support scripts or advanced conditions.

-   **Restrict access to list reports with a read operation**

    A list report uses regular record access controls to determine who can access data in a table or field. A report\_view access control cannot prevent users from viewing lists to which they have read access. To restrict access to record data in lists and forms, create a read operation access control. For more information about record access controls, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).


-   **[Report execution security](read-access-control.md)**  
When a report is run, report\_view access control lists \(ACLs\) are evaluated on the table and table fields that the report is based on. If no report\_view ACL exists, there is a fallback check on table-level read ACL roles. The report\_view ACL checks on all fields, including those used in the condition builder \(including dot-walked fields\).

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

**Related topics**  


[ACL rule types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/acl-rule-types.md)

[Create an ACL Rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/t_CreateAnACLRule.md)

