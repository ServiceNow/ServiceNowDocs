---
title: Create a proactive case from an alert
description: Create a case for customer install base affected by an alert to anticipate customer issues and address them proactively.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Proactive Customer Service Operations, Automate and optimize, Use, Customer Service Management]
---

# Create a proactive case from an alert

Create a case for customer install base affected by an alert to anticipate customer issues and address them proactively.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator

## About this task

**Note:** This task only applies if you are using Event Management integration on CSM Agent Workspace or the ServiceNow AI Platform interface.

A proactive case is a case created on behalf of customers, whose install base is directly affected by an alert. You can open a proactive case manually or through automation. Customer service agents then work on cases. From the Alert form, you can also track the install base items affected by the alert.

If the **Create Proactive Case** rule is enabled, a case is automatically created when an incident is created from an alert and the system has determined that there are external customer install base items affected. For more information, see [Activate an alert rule to automatically create a proactive case from an alert](automate-case-creation-alert.md).

ITOM Event Management calculates the services \(CIs\) impacted by an alert and populates the em\_impacted\_ci\_table with the impacted services \(CIs\) and alert CI on the given alert.

The Affected Install Base related list on the Alert form displays the install base items that are linked to the impacted services \(CIs\).

The **Refresh Affected Install Base Items** button on the Alert form recalculates the impacted services \(CIs\) and updates the em\_impacted\_ci\_table and affected install base items with the latest changes. For more details, see [Alert Impact Calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/c_EMImpactCalculation.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home** &gt; **Lists** &gt; **All Alerts**.

2.  Click an alert that you want to create a case for.

3.  To trace the install base items affected by the alert, click **Refresh Affected Install Base Items**.

    These items are listed in the Affected Install Base Items related list on the Alert form. The **Affected Install Base Items** list is not updated automatically, so refresh the install base items each time you open an alert.

4.  Click **Create Case**.

    **Note:** If you don't see the **Create Case** option, click **...**.

5.  Fill out the **Short Description** and other fields, as required.

6.  Click **Submit**.

    A proactive case is created and the case number is added to the **Case** field on the Alert form.

    Case priority is set based on the severity of the alert. Customer service agents can then take action accordingly.

    |Alert severity|Case priority|
    |--------------|-------------|
    |Critical|Critical|
    |Major|High|
    |Minor|Moderate|
    |Warning|Low|
    |Info|Low|


