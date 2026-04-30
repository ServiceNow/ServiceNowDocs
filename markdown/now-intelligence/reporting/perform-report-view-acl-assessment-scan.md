---
title: Perform the Report View assessment scan
description: Scan your instance for reports that users would be unable to view based on existing access control lists \(ACLs\).
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ACL Assessment for Reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Perform the Report View assessment scan

Scan your instance for reports that users would be unable to view based on existing access control lists \(ACLs\).

## Before you begin

Roles required: admin and security\_admin.

## About this task

The assessment scan returns a list of affected reports. A report is affected if a user has seen the report who would not be able to see it based on a report\_view ACL or blocking READ ACL, in the case of reports based on tables without report\_view ACLs.

The time the assessment scan takes can vary according to the number of records in the instance. Consider running the assessment over night. Also consider filtering the reports that the assessment applies to. For more information, see [Filter report assessment scans](filter-report-assessment-scans.md#).

## Procedure

1.  Elevate your role to security\_admin.

    For more information, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

2.  Navigate to **All** &gt; **Reports** &gt; **ACL Assessment for Reports** &gt; **Report ACL Dashboard**.

3.  Select **Run Assessment Scan**.

    The assessment scan can take a long time on instances with many reports. You can choose to view partial results while the scan is in progress, or select **View Result** when the scan is complete. When the scan is complete, a message shows who ran the assessment and the start and stop time of the assessment.

    **Note:** The scan calculates the number of executions of each affected report. If the property **sn\_report\_acl.run\_scan\_based\_on\_report\_execution\_only** is false, the **Total Executions** column in the Impacted Reports list is always empty, and **process\_reports\_executed\_within\_X\_days\_ago** is ignored.

    The initial scan shows:

    -   The user who executed the scan and the scan's start and end times
    -   The number of affected reports
    -   The percent of reports on the instance that are affected
    -   The number of tables with report\_view access control lists
4.  If the affected reports list is empty, navigate to **report\_executions.list**.

    1.  If this table is empty, there are no ACL issues.

    2.  If the **report\_executions.list** has entries, change the system property **sn\_report\_acl.run\_scan\_based\_on\_report\_execution\_only** to false and run the scan again.

        This time, the scan shows all the affected reports, not only those reports that have been executed. The second scan often takes longer to run.

5.  Navigate to **All** &gt; **Reports** &gt; **ACL Assessment for Reports** &gt; **Affected Reports List** to [view the list of impacted reports](view-impacted-reports.md).

    The Impacted Reports list shows the reports affected by ACLs.


**Parent Topic:**[ACL Assessment for Reports](../concept/report-view-acl-dashboard.md)

