---
title: Report permission issues
description: There are several reasons why a report is showing less information than expected or possibly no data at all. These include insufficient permissions on the report and the report not being shared.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report permission issues

There are several reasons why a report is showing less information than expected or possibly no data at all. These include insufficient permissions on the report and the report not being shared.

## Report not shared

A common reason that a report may not be viewable is that the report hasn’t been shared with the users who are attempting to access it. By default, a newly created report won’t be shared and therefore inaccessible to anyone except the report creator or users with the admin role. A report can be shared with an individual user, with one or more groups, or assigned to one or more roles.

Unshared reports don’t appear in lists of reports a user has access to or in other options in which a report might be opened or selected. When users are able to see a dashboard the report has been added to, but not the report itself, a message indicates that the "Report is visible only to a specific user or group".

To correct this issue, the owner of the report \(or an administrator\) can share that report with the individuals who should have visibility and access to that report. You can share a report directly from the report's sharing icon. For more information, see [Share a Core UI report](../task/t_ShareASetting.md).

## List reports show fewer rows than expected

Another common issue is that fewer rows appear in list reports than the viewer expects. For example, one user sees 100 rows in a list report, but another user, viewing that same report may see fewer rows or even no rows at all. When one or more rows have been removed from the report, a message indicates the number rows removed due to security constraints.

The usual cause is that each row of a list report is first compared against any read access control lists \(ACLs\) defined on the report's source tables.

The ACL is considered for each list row that might be displayed in a report. For more information, see [Report\_view access control](../concept/report-view-access-control.md).

## Non-list reports show incomplete data

Graphical reports \(defined as any non-list type report\) may show an incomplete set of data for one user, as compared to another user reviewing that same report.

This issue is caused by the fact that Before Query business rules are performed on the data from the source table before a report is generated and rendered. Business rules, found on a report's source tables, limit the data based on permissions or similar criteria. Any records that don’t fulfill the rule's criteria aren’t included in the report. Therefore, users with differing permission levels \(due to group or role permissions mainly\) see the same report showing different results. For more information, see [Before Query business rules](https://www.servicenow.com/docs/access?context=bp-before-query-business-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[Administering reports](../concept/c_AdminsteringReports.md)

