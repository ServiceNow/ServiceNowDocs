---
title: Perform the Report View Assessment scan
description: Scan your instance for data visualizations and Core UI reports that users were stopped from viewing based on existing access control lists \(ACLs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/perform-report-view-acl-assessment-scan.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ACL Assessment for Data Visualizations, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Perform the Report View Assessment scan

Scan your instance for data visualizations and Core UI reports that users were stopped from viewing based on existing access control lists \(ACLs\).

## Before you begin

Roles required: admin and security\_admin.

## About this task

The assessment scan returns a list of affected data visualizations and Core UI reports. A visualization or report is affected if a user who lacks access has attempted to view it. Access is determined by a report\_view ACL or, for visualizations of tables without report\_view ACLs, by a read ACL.

The time the assessment scan takes can vary according to the number of records in the instance. Consider running the assessment overnight. Also consider filtering the reports that the assessment applies to. For more information, see [Filter report assessment scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/filter-report-assessment-scans.md).

## Procedure

1.  Elevate your role to security\_admin.

    For more information, see [Elevate to a privileged role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **ACL Assessment for Data Visualizations** &gt; **ACL Dashboard**.

3.  Select **Run Assessment Scan**.

    The assessment scan can take a long time on instances with many reports. You can choose to view partial results while the scan is in progress, or select **View Result** when the scan is complete. When the scan is complete, a message shows who ran the assessment and the start and stop time of the assessment.

    **Note:** The scan calculates the number of executions of each affected report.

    The initial scan shows:

    -   The user who executed the scan and the scan's start and end times
    -   The number of affected reports
    -   The percent of reports on the instance that are affected
    -   The number of tables with report\_view access control lists
4.  If the affected reports list is empty, navigate to **report\_executions.list**.

    1.  If this table is empty, there are no ACL issues.

    2.  If the **report\_executions.list** has entries, change the system property **sn\_report\_acl.run\_scan\_based\_on\_report\_execution\_only** to false and run the scan again.

        This time, the scan shows all the affected reports, not only those reports that have been executed. The second scan often takes longer to run.

5.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **ACL Assessment for Data Visualizations** &gt; **Affected Data Visualizations** to [view the list of impacted reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-impacted-reports.md).

    The Report view ACL assessments list shows the visualizations with attempted views affected by ACLs.


**Parent Topic:**[ACL Assessment for Data Visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/report-view-acl-dashboard.md)

