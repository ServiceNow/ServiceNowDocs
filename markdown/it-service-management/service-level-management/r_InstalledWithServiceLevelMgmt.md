---
title: Installed with Service Level Management
description: Activating the Service Level Management plugin adds or modifies these components: tables, properties, UI actions, UI policies, script includes, client scripts, business rules, email notifications, scheduled jobs, and workflows.Tables are added with Service Level Management.Roles are added with activation of Service Level Management plugin.Scheduled jobs are added with Service Level Management.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Activate Service Level Management, Service Level Management plugins, Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Installed with Service Level Management

Activating the Service Level Management plugin adds or modifies these components: tables, properties, UI actions, UI policies, script includes, client scripts, business rules, email notifications, scheduled jobs, and workflows.

**Parent Topic:**[Activate Service Level Management](../task/activate-sla-plugin.md)

## Tables installed with Service Level Management

Tables are added with Service Level Management.

|Display name \[Table name\]|Description|
|---------------------------|-----------|
|SLA Definition \[contract\_sla\]|Provides the conditions, duration, and schedule for an SLA Definition.|
|SLA Conditions \[sla\_condition\_class\]|Defines how the conditions in the SLA Definition are used to determine the transitions between different stages of each task SLA.|
|SLA Repair Log\[sla\_repair\_log\]|Used to provide a log of when the SLA Repair function is set to action.|
|SLA Repair Log Entry \[sla\_repair\_log\_entry\]|Extends syslog and stores the before or after values of a task SLA record that has been repaired.|
|Task SLA \[task\_sla\]|Associates a task with the SLA Definition that applies to it.|
|SLA Timer Configuration \[sla\_timer\_config\]|Stores the timer configuration information.|
|SLA timer configuration mapping \[sla\_timer\_config\_mapping\]|Stores the Task SLA mapping information.|

## Roles installed with Service Level Management

Roles are added with activation of Service Level Management plugin.

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sla\_admin|Users with this role have full administrative rights to the Service Level Management application|flow\_operator|
|sla\_manager|Users with this role can define SLA definitions and view SLA repair logs.|flow\_operator|

## Scheduled jobs installed with Service Level Management

Scheduled jobs are added with Service Level Management.

|Scheduled job|Description|
|-------------|-----------|
|SLA update \(already breached\)|Refreshes the timings in task SLA records that have already breached. This is limited to task SLAs where the breach time is within the last 365 days. This job runs once a day.|
|SLA update \(breach after 30 days\)|Refreshes the timings in task SLA records where the breach time is more than 30 days away. This is limited to task SLA records where the breach time is within the next 365 days. This job runs every 5 days.|
|SLA update \(breach within 1 day\)|Refreshes the timings in task SLA records where the breach time is more than 1 hour away and less than 24 hours away. This job runs every hour.|
|SLA update \(breach within 1 hour\)|Refreshes the timings in task SLA records where the breach time is more than 10 minutes away and less than 1 hours away. This job runs every 10 minutes.|
|SLA update \(breach within 10 min\)|Refreshes the timings in task SLA records where the breach time is in the next 10 minutes This job runs every minute.|
|SLA update \(breach within 30 days\)|Refreshes the timings in task SLA records where the breach time is more than 1 day away and less than 30 days away. This job runs once a day.|

