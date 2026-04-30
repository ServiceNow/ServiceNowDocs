---
title: ITSM Predictive Intelligence Workbench notifications
description: Email notifications are added with Predictive Intelligence Workbench.
locale: en-US
release: yokohama
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITSM Predictive Intelligence Workbench administration, ITSM Predictive Intelligence Workbench, IT Service Management]
---

# ITSM Predictive Intelligence Workbench notifications

Email notifications are added with Predictive Intelligence Workbench.

**Important:**

Starting with the yokohama release, the ITSM Predictive Intelligence Workbench will reach its end of life \(EOL\) as part of its deprecation process. It will be completely deprecated and no longer deployed, enhanced, or supported from the yokohama release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Predictive Intelligence Workbench includes several email notifications that alert users throughout the use case model implementation.

Predictive Intelligence process architects creating and training use case models receive an email notification when a use case model is successfully trained and when batch testing has finished successfully. If a use case fails training or if batch testing produces errors, users will receive notifications about these scenarios, as well.

Users can click a link in the email notification to view a newly trained use case or batch test results. They can also download the test results, if desired. Users can receive the following notifications:

<table id="table_cyr_5r1_gs"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use case model training successfulTable: PI Solution Model \[piwb\_model\]

</td><td>

Sends an email to a specified user group when a use case model is successfully trained.

</td></tr><tr><td>

Batch test run complete

</td><td>

Sends an email to a specified user group when batch testing is complete.

</td></tr><tr><td>

Use case Model training failedTable: PI Solution Model \[piwb\_model\]

</td><td>

Sends an email to a specified user group when a use case model training has failed.

</td></tr></tbody>
</table>Create an ITSM Predictive Intelligence Workbench user group and add users or roles to ensure Predictive Intelligence process architects are notified during the use case model implementation process. Refer to [Create an ITSM Predictive Intelligence Workbench user group](../task/itsm-piwb-user-groups.md).

For more details about email notifications for Predictive Intelligence Workbench, refer to [Preview email notification](https://www.servicenow.com/docs/access?context=t_PreviewingNotifications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

