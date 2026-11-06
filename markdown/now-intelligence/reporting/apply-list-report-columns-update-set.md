---
title: List report columns in update sets
description: Configured columns in list reports can be moved to another instance by committing an update set.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/reporting/apply-list-report-columns-update-set.html
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [List reports, Core UI Report types, Core UI Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# List report columns in update sets

Configured columns in list reports can be moved to another instance by committing an update set.

**Important:** This topic is about Core UI List reports. For information about the newer Platform Analytics lists, see [Create a Platform Analytics list visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/create-dv-analytics-list.md).

Configured list report columns are not automatically applied to an instance when you commit an update set. List reports render using UI views created each time you save a report. To ensure configured columns render in a list report or on a dashboard widget in another instance:

1.  From the UI View table, search for the sys\_id of the report \(RPT\) view record for your changes.
2.  Add it to the update set.

For information on adding customized configurations to an update set and applying them, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets.md).

\[Omitted image "UIViewsReportViewRPTSysID.png"\] Alt text: UI Views report sys\_id

