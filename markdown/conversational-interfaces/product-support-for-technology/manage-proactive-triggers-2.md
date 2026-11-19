---
title: Monitoring Proactive Triggers
description: After admins have installed Proactive Triggers and created related actions and rules, admins can check that the Proactive Triggers feature is performing as expected. For example, admins can view the Proactive Execution History table and the Proactive Daily Report table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/product-support-for-technology/manage-proactive-triggers-2.html
release: brazil
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Monitoring Proactive Triggers

After admins have installed Proactive Triggers and created related actions and rules, admins can check that the Proactive Triggers feature is performing as expected. For example, admins can view the Proactive Execution History table and the Proactive Daily Report table.

This topic includes information admins can use to see if the Proactive Triggers feature is performing as expected. For example, admins can review the Proactive Triggers history tables to make sure that the rules and actions are working as intended.

Admins might encounter common issues when creating rules and actions. Each issue has a suggested resolution.

## View Proactive Triggers history and report tables

To see if the Proactive Triggers feature is running as intended, admins can review the data in the following tables:

-   Proactive Execution History  \[sys\_cs\_ptrigger\_execution\] table
    -   Real-time execution history of Proactive Triggers events.

        **Tip:** The Notes column provides a brief rule execution status. For additional information about why Proactive Triggers didn't run successfully, select the execution event from the Created column, and then view the **Details** field under the **Others** section.

    -   The data from this table is removed every seven days.
-   Proactive Daily Report \[sys\_cs\_ptrigger\_report\_daily\] table
    -   Aggregated execution data by user, rule, and action per day.
    -   Execution data is processed every hour and updates this table.
    -   The data from this table is removed every 35 days.

## Common issues and resolutions

The following table lists issues that you may encounter when you're creating rules and actions, and the suggested resolutions.

|Issue|Resolution|
|-----|----------|
|The rule's trigger type is URL, but the page is a catalog item, knowledge article, or portal home page, so the rule doesn't run.|Change the rule's trigger type to match the page type.|
|The **Frequency** field is set to **Once per user**, but the rule doesn't run.|Clear the rule history at the rule level. For details on clearing the rule history, see [Multiple Proactive Triggers rules and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/product-support-for-technology/multiple-rules-and-actions.md).|
|The rule doesn't run for some end users, and the selected action type is **Message that launches a virtual agent topic**.|End users may not have access to the Virtual Agent topic defined on the action. Check the access to the topic in Assistant Designer.|
|The Proactive Triggers rule doesn't run.|Close any active conversations in the Virtual Agent chat widget.|

