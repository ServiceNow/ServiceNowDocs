---
title: Service delivery overview
description: Use the Service delivery overview to view the Analytics dashboards of the customer accounts. You can explore the details about the operational status of the accounts.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Review customer or partner accounts, Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# Service delivery overview

Use the Service delivery overview to view the Analytics dashboards of the customer accounts. You can explore the details about the operational status of the accounts.

Service delivery overview displays the Analytics dashboards of the customer accounts. These dashboards contains diagrams, charts, and summary data on metrics such as proactive cases, account escalations, Service Level Agreements \(SLAs\), Core Key Performance Index \(KPI\), and so on.

The Service delivery overview contains the following tabs for each dashboard.

-   Overview
-   SLA performance
-   Service Management

![Service delivery overview page view of the current operational status metrics.](../image/service-delivery-overview.png "Example of Service delivery overview")

## Access

You can access the Service delivery overview page as follows:

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** or **CSM/FSM Configurable Workspace**.
2.  Select the service delivery overview \(![Service Deliver Overview Icon.](../image/icon-service-delivery-overview.png)\) icon.

## Account selection

Select **Accounts**, and then select the customer account that you want to view the data. You can also select more than one account.

## Overview tab

The Overview tab provides a comprehensive overview of key performance metrics and service-related indicators, presenting essential data at a glance.

|Indicator|Description|
|---------|-----------|
|Overall SLA achievement|Total percentage of SLAs met out of the total number of SLAs.|
|Open account escalations|Total number of account-related issues that have been escalated and are currently unresolved.|
|Unplanned outages caused by changes|Total number of outages classified as Outage with task numbers labeled as Change type.|
|Configuration items involved in cases|Total number of configuration items \(CI\) involved in cases.|
|Total outage duration by type \(hours\)|Sum of the total duration of outages, categorized by their types. This visualization helps which types of outages are most frequent or have the longest durations, enabling targeted improvements and resource allocation.|
|Total outage duration caused by changes \(hours\)|Total duration of all outages associated with tasks identified by a task number starting with CHG.|
|First contact rate|Percentage of customer inquiries or issues that are resolved during the first interaction with a service or support team.|
|Average time to resolve case|Average amount of time taken to resolve a case from the moment it’s opened until it’s officially closed.|
|Average time to fulfill|Average duration taken to fulfill a request from the time it’s initiated until it’s fully completed or closed.|
|Percent of cases created proactively|Percentage of customer service or support cases that were initiated proactively by the organization itself, rather than in response to customer inquiries or complaints.|
|Proactive cases by incident|Number of cases where the proactive field is set to true and the Caused by Incident field is populated.|
|Proactive cases by change|Number of cases where the proactive field is set to true and the Caused by Change field is populated.|
|Major cases triggered by incident|Number of cases where the proactive field is set to true and the Incident field is populated.|
|Number of missed major case record SLAs|All breached SLAs associated with tasks labeled as Case and having an Accepted status in the major case state.|

## SLA performance tab

The SLA performance tab displays metrics that provide you with a summary of the effectiveness with which the managed services adhere to their SLAs.

|Indicator|Description|
|---------|-----------|
|Team overdue SLAs|Total number of SLAs marked as breached within a specific team, filtered based on the assignment groups linked to the logged-in user.|
|Team opened SLAs|Total number of SLAs that are either in progress or paused, specific to a team and filtered according to the assignment groups of the logged-in user.|
|Team SLA analysis achieved|Percentage of SLAs successfully met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|Team SLAs expiring today|Total number of SLAs within a specific team scheduled to reach their deadline or expire today, filtered based on the assignment groups linked to the logged-in user.|
|Team average SLAs age|Average duration between start time and end time for all SLAs marked as achieved or completed within a specific team, filtered by the assignment groups associated with the logged-in user.|
|Team SLA analysis breached|Percentage of SLAs that weren’t met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|Overdue SLAs|Number of open SLAs with the **Has breached** field activated.|
|Opened SLAs|Total number of SLAs that are in In progress or paused state.|
|Overall SLA analysis achieved|Percentage of SLAs that have been successfully met by a service provider.|
|SLAs expiring today|Number of SLAs that are scheduled to reach their deadline or expiration on the current day.|
|Average SLAs age|Average time span from start time to end time for all SLAs that are marked as either achieved or completed.|
|Overall SLA analysis breached|Percentage of SLAs that weren’t met by a service provider. It assesses the instances where the agreed-upon time lines outlined in the SLAs were violated.|

## Service management tab

The Service management tab provides metrics that deliver actionable insights, enabling you to track and enhance the efficiency and quality of your services.

| | |
|---|---|
|Items not updated in last 5 days|Gauge chart grouping of requests marked as New, In Progress, or On Hold, that haven’t received any updates or modifications within the past five days.|
|Items not updated for 7+ days|Gauge chart grouping of requests that aren’t updated for more than seven days.|
|Incident reopen rate|Percentage of incidents that were initially marked as resolved but later required reopening due to unresolved issues or the emergence of related problems.|
|Average re-assignment count for resolved incidents|Average number of times an incident is reassigned to different team members or teams before it’s finally resolved.|
|Average active case age|Average duration that cases remain open or active before they’re resolved or closed.|
|Problems created by case|All problems initially reported with the task type labeled as Case.|
|Problems created by incident|All problems initially reported with the task type labeled as Incident.|
|Preferred channel used for communication|Sum of the total number channels used for communication, categorized by the type of channel. This visualization helps which types of channels are most used or have the longest durations.|

## User roles

|User role|Description|
|---------|-----------|
|sn\_ind\_tsm\_sdwan.PSEW\_USER|Can view and edit the dashboard and manage users, groups, and roles for the dashboard.|

**Parent Topic:**[Reviewing customer or partner accounts in Proactive Service Experience Workflows](reviewing-customer-accounts-360.md)

