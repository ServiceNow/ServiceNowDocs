---
title: \(Legacy\) Publish a report
description: Publish a report to create a URL that anyone can use to access the report, including people who are not users. When anyone navigates to the URL, the report is generated with current data from the instance. Reports are available until they are unpublished.Published reports are available at the published URL until you unpublish them.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Distribute reports, Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# \(Legacy\) Publish a report

Publish a report to create a URL that anyone can use to access the report, including people who are not users. When anyone navigates to the URL, the report is generated with current data from the instance. Reports are available until they are unpublished.

## Before you begin

**Danger**

This functionality is deactivated by default because of the risk of exposing data to unauthorized persons.

For this functionality to be available, the system property **glide.report.published\_reports.enabled** must be set to `true`.

Role required: report\_publisher, report\_admin, or admin.

## About this task

There are limitations to what users see when they follow the publish URL for a report.

-   Data that is visualized as a graphic report and not limited by business rules is always visible in published reports. Graphic reports are all reports except for list reports.
-   Read ACLs govern the content of list reports. Users cannot see records for which they do not have access.
-   Public roles with access to a published report may see a smaller subset of the original data displayed in the report when they're not logged in. For help with resolving published reports not showing all the expected data, see [KB article KB0736982](https://support.servicenow.com/kb_view.do?sysparm_article=KB0736982).

Users with the admin or report\_admin role can see if a report has been published. Navigate to **Reports** &gt; **View / Run**, open the report, and click the **Sharing** icon \(![Sharing icon](../../../common/image/Form_ShareIcon.png)\). If the Sharing menu has the **Publish** option, the report is not yet published. If the Sharing menu has the **Unpublish** option, the report has been published.

**Note:** To make a report available only to users who are logged in, set its **Sharing** setting to **Everyone**, but do not publish it.

## Procedure

1.  Navigate to **Reports** &gt; **View / Run**.

2.  Click the report you want to publish.

3.  In the upper right side of the report form, click the **Sharing** icon \(![Sharing icon](../../../common/image/Form_ShareIcon.png)\) and select **Publish**.

    A link icon \(![Link icon](../image/link-icon.png)\) shows with the Report option icons message. Click this icon to show a link to the published report. This link is available as long as the report is published.

    **Note:** Business rules may affect how records are collected for public reports.


**Parent Topic:**[Distribute reports](../concept/c_DistributeReports.md)

## Unpublish a report

Published reports are available at the published URL until you unpublish them.

### Before you begin

Role required: both the report\_publisher and report\_user, report\_admin, or admin.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report you want to unpublish.

3.  From the upper right side of the report form, click the **Sharing** icon \(![](../../../common/image/Form_ShareIcon.png)\) and select **Unpublish**.


### Result

The report is no longer published and the link icon \(![](../image/link-icon.png)\) is removed from the report designer for the unpublished report.

