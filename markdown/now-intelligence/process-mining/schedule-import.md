---
title: Schedule data import
description: Activate and schedule the trigger flow on a configuration record so that Process Mining automatically pulls new audit log data at a set interval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/schedule-import.html
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Process Mining for Workday and Salesforce, Import external data, Process Mining, Platform Analytics]
---

# Schedule data import

Activate and schedule the trigger flow on a configuration record so that Process Mining automatically pulls new audit log data at a set interval.

## Before you begin

Role required: sn\_process\_mining\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **External Data Set** &gt; **Connectors**.

    The Connector Configurations page is displayed.

    \[Omitted image "app-conn-config.png"\] Alt text: Connector configurations list

2.  Select **Schedule Import**.

    **Note:** This applies to all connector configurations that have the **Active** field set to **true**.

    The connector configuration opens in Workflow Studio.

3.  Select **Edit**.

4.  Update the **TRIGGER** area to match the import schedule you want.

5.  Select **Activate**.


## Result

The configuration connectors are scheduled to run according to the preference you have selected.

