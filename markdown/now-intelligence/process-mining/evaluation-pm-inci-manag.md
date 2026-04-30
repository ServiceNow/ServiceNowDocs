---
title: Process Mining evaluation project for Incident Management
description: Process Mining evaluation project for Incident Management is a limited version of Process Mining. It’s shipped as part of the Process Mining plugin and available for customers that aren’t entitled for Process Mining for ITSM. It enables you to familiarize with improving your process with Process Mining capability.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Evaluating Process Mining, Exploring Process Mining, Process Mining, Platform Analytics]
---

# Process Mining evaluation project for Incident Management

Process Mining evaluation project for Incident Management is a limited version of Process Mining. It’s shipped as part of the Process Mining plugin and available for customers that aren’t entitled for Process Mining for ITSM. It enables you to familiarize with improving your process with Process Mining capability.

ITSM customers can evaluate Process Mining with their Incident Management business process in their production instance. You can do this because the Process Mining plugin \(sn\_po\) is enabled by default in all your production instances. To evaluate Process Mining, a new project type is introduced that will enable you to become familiar with the product functionality with your own data.

**Note:** With this new project type, you can evaluate Process Mining in your production instance with limited records using the ITSM Incident Management KPIs. However, you’ll be able to evaluate and try Process Mining on your own project using the sample mining feature in your sub-production instances without any other functionality restrictions. These are the two alternative and complementary ways to evaluate the Process Mining functionality without a full license.

This evaluation version works on the data that you have stored in your production instance tables. Note the following about Process Mining evaluation project for Incident Management:

-   Allows you to access an Incident Management preconfigured Process Mining project configuration limited to up to 3600 records that were resolved in the last seven days. If there are more than 3600 records resolved in the last seven days, the evaluation is restricted to the first 3600 records.
-   The default activity definitions are: State and Assignment group \(so you can analyze State and Assignment group\).
-   Includes multiple automated improvement opportunities such as ping-pong, rework, and others.
-   Includes introduction videos, FAQs, Academy sessions, and use cases.

If you have the required roles \(itil, snc\_internal\), you can evaluate Process Mining for ITSM Incident Management via ITSM Incident Management Performance Analytics KPIs or through the Process Mining Workspace.

The Performance Analytics KPI details and analytics hub icon are available only for itil, sn\_sd.success\_dashboard\_read, sn\_sd.success\_dashboard\_details\_read, and business\_stakeholder roles. You can customize the roles to which the evaluation project is exposed on the KPI details and analytics hub by adding the promin.evaluation\_pa\_integration\_roles to the sys\_property table. It overwrites the default roles.

For more information, see [Run Process Mining evaluation project](../task/run-evaluation-project.md).

**Parent Topic:**[Evaluating Process Mining](evaluate-pm.md)

**Related topics**  


[Create a dashboard with the in-line editor](../../../use/dashboards/task/create-db-in-ac.md)

[Analytics Hub](../../../use/performance-analytics/concept/c_UsePerformanceAnalyticsScorecards.md)

