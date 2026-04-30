---
title: Manage Proactive Triggers
description: After admins have installed Proactive Triggers and created related actions and rules, admins can check that the Proactive Triggers feature is performing as expected. For example, admins can view the Proactive Execution History table and the Proactive Daily Report table.
locale: en-US
release: yokohama
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Proactive Triggers, Proactive Triggers, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manage Proactive Triggers

After admins have installed Proactive Triggers and created related actions and rules, admins can check that the Proactive Triggers feature is performing as expected. For example, admins can view the Proactive Execution History table and the Proactive Daily Report table.

This topic includes information admins can use to see if the Proactive Triggers feature is performing as expected. For example, admins can review the Proactive Triggers history tables to make sure that the rules and actions are working as intended.

This topic also includes common issues that admins may encounter when they're creating rules and actions, along with the proposed solutions.

## View Proactive Triggers history and report tables

To see if the Proactive Triggers feature is running as intended, admins can review these two tables' data:

-   Proactive Execution History  \(sys\_cs\_ptrigger\_execution\) table
    -   Real-time execution history of Proactive Triggers events.

        **Tip:** The Notes column provides a brief rule execution status. For additional information about why Proactive Triggers didn't run successfully, select the execution event from the Created column, and then view the **Details** field under the **Others** section.

    -   The data from this table is removed every seven days.
-   Proactive Daily Report \(sys\_cs\_ptrigger\_report\_daily\) table
    -   Aggregated execution data by user, rule, and action per day.
    -   Execution data is processed every hour and updates this table.
    -   The data from this table is removed every 35 days.

## Common issues and resolutions

The following table lists issues that you may encounter when you're creating rules and actions, and the suggested resolutions.

|Issue|Resolution|
|-----|----------|
|If a trigger type is defined as a URL in the rule, when the page is actually a catalog item, knowledge, or portal, the rule won't run.|Admin must fix the rule to match the page type.|
|The **Frequency** is set to run once per user but the rules don't run.|Clear the rule history at the rule level. For details on clearing the rule history, see [Multiple Proactive Triggers rules and actions](multiple-rules-and-actions.md).|
|Rule doesn't run for some end users, and the **action** type selected is **virtual agent topic**.|End users may not have access to the Virtual Agent topic defined on the action. Check the access to the topic in Virtual Agent Designer.|
|The Proactive Triggers rule doesn't run.|Close any active conversations in the Virtual Agent chat widget.|

