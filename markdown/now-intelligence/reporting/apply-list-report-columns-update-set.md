---
title: Applying list report column configurations with an update set
description: Configured columns in list reports can be moved to another instance by committing an update set.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [List reports, Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Applying list report column configurations with an update set

Configured columns in list reports can be moved to another instance by committing an update set.

Configured list report columns are not automatically applied to an instance when you commit an update set. List reports render using UI views created each time you save a report. To ensure configured columns render in a list report or on a dashboard widget in another instance:

1.  From the UI View table, search for the sys\_id of the report \(RPT\) view record for your changes.
2.  Add it to the update set.

For information on adding customized configurations to an update set and applying them, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

![UI Views report sys_id](../image/UIViewsReportViewRPTSysID.png)

