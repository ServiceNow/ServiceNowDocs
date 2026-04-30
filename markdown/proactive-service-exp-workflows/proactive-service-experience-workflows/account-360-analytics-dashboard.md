---
title: Account 360 Analytics dashboards
description: The Analytics dashboards provided by Operations Account 360 view displays charts and summary data on metrics like proactive cases, account escalations, SLAs, channels used, core KPIs, and more.
locale: en-US
release: zurich
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Review customer or partner accounts, Use, Proactive Service Experience Workflows]
---

# Account 360 Analytics dashboards

The Analytics dashboards provided by Operations Account 360 view displays charts and summary data on metrics like proactive cases, account escalations, SLAs, channels used, core KPIs, and more.

To view the Analytics dashboards, navigate to **Workspaces** &gt; **Service Operations Workspace** &gt; **Lists** &gt; **Accounts** &gt; **All**. Open a customer account from the list and then select the **Analytics** tab.

The Analytics tab contains the additional tabs for each dashboard.

-   Analytics Snapshot
-   Core KPIs
-   Service Level
-   Proactive Service

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|Customer service agent: View case metrics like proactive cases, account escalations, SLA, channels used, core KPIs to understand the current performance of customer service at your organization.|sn\_ind\_tsm\_core\_noc\_agent|
|Content administrator: Can edit the dashboard and manage users, groups, and roles for the dashboard.|pa\_admin|
|Content creator: Can view the dashboard.|pa\_viewer|

## Analytics breakdown

The Analytics dashboards use the Account selection breakdown. Select an account to exclusively view its data.

## Analytics Snapshot dashboard

The Analytics Snapshot dashboard offers a comprehensive overview of key performance metrics and service-related indicators, presenting essential data at a glance.

## Analytics Snapshot indicators

|Indicator|Description|
|---------|-----------|
|% Overall SLA achievement|Total percentage of SLAs met out of the total number of SLAs.|
|Total proactive cases created|Total proactive cases initiated by changes and incidents.|
|Number of open account escalation|Total number of account-related issues that have been escalated and are currently unresolved.|
|Outage duration – Type-wise distribution|Sum of the total duration of outages, categorized by their types. This visualization helps in understanding which types of outages are most frequent or have the longest durations, enabling targeted improvements and resource allocation.|
|% of cases created proactively|Percentage of customer service or support cases that were initiated proactively by the organization itself, rather than in response to customer inquiries or complaints.|
|CI vs Cases|Comparison of Configuration Items \(CI\) involved in service cases versus the total number of cases reported. Configuration Items can include any component essential for the delivery of IT services such as software, hardware, and network infrastructure.|
|Preferred channel used for communication|Identification of the most commonly used method of communication by customers within a given system or service. For example, incidents.|

## Core KPIs dashboard

The Core KPIs dashboard delivers actionable insights, enabling users to track and enhance the efficiency and quality of their services.

## Core KPIs indicators

|Indicator|Description|
|---------|-----------|
|% First contact rate|Percentage of customer inquiries or issues that are resolved during the first interaction with a service or support team.|
|% Incident re-open rate|Percentage of incidents that were initially marked as resolved but later required reopening due to unresolved issues or the emergence of related problems.|
|Closed case with breached SLAs|Number of cases that were closed but failed to meet the predefined service level agreements \(SLAs\).|
|Avg re-assignment count for resolved incidents|Average number of times an incident is reassigned to different team members or teams before it is finally resolved.|
|Avg active case age|Average duration that cases remain open or active before they are resolved or closed.|
|Avg time to resolve case|Average amount of time taken to fully resolve a case from the moment it is opened until it is officially closed.|
|Avg time to fulfill|Average duration taken to completely fulfill a request from the time it is initiated until it is fully completed or closed.|
|Number of open incidents not updated in last 5 days|Number of incidents marked as New, In Progress, or On Hold, that have not received any updates or modifications within the past five days.|
|Number of open cases not updated in last 5 days|Number of active cases marked as New, Open, or Awaiting Info, that have not been updated or modified within the past five days.|
|Number of catalog tasks not updated in the last 5 days|Number of catalog tasks in an Open, Pending, or Work in Progress state that have not been updated in over five days.|
|Cases|Number of cases in a New, Open, or Awaiting Info state that have not been updated for more than seven days since their creation.|
|Incidents|Number of incidents in a New, In Progress, or On Hold state that have not been updated for more than seven days since their creation.|
|Request Items|Number of requested items in a Open, Pending, or Work in Progress state that have not been updated for more than seven days since their creation.|
|Approvals|Number of approvals in a Requested or More Information Required state that have remained unchanged for more than seven days since their creation.|
|Catalog Tasks|Number of catalog tasks in an Open, Pending, or Work in Progress state that were created more than seven days ago and have not been updated since.|

## Service Level dashboard

This dashboard displays metrics that provide users a summary of the effectiveness with which the managed services adhere to their Service Level Agreements \(SLAs\).

## Service Level indicators

|indicator|Description|
|---------|-----------|
|% Overall SLA achieved|Percentage of service level agreements \(SLAs\) that have been successfully met by a service provider.|
|% Incident SLA achieved|Percentage of incident-related service level agreements \(SLAs\) that have been successfully met by a service provider.|
|% Case SLA achieved|Percentage of case-related service level agreements \(SLAs\) that have been successfully met by a service provider.|
|% Request SLA achieved|Percentage of request-related service level agreements \(SLAs\) that have been successfully met by a service provider.|
|% Overall SLA breached|Percentage of service level agreements \(SLAs\) that were not met by a service provider. It assesses the instances where the agreed-upon time lines outlined in the SLAs were violated.|
|% Incident SLA breached|Percentage of incident-related service level agreements \(SLAs\) that were not met by a service provider.|
|% Case SLA breached|Percentage of case-related service level agreements \(SLAs\) that were not met by a service provider.|
|% Request SLA breached|Percentage of request-related service level agreements \(SLAs\) that were not met by a service provider.|
|% My team Overall SLA achieved|Percentage of service level agreements \(SLAs\) successfully met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|% My team Incident SLA achieved|Percentage of incident-related service level agreements \(SLAs\) successfully met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|% My team Case SLA achieved|Percentage of case-related service level agreements \(SLAs\) successfully met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|% My team Request SLA achieved|Percentage of request-related service level agreements \(SLAs\) successfully met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|% My team Overall SLA breached|Percentage of service level agreements \(SLAs\) that were not met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|% My team Incident SLA breached|Percentage of incident-related service level agreements \(SLAs\) that were not met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|% My team Case SLA breached|Percentage of case-related service level agreements \(SLAs\) that were not met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|% My team Request SLA breached|Percentage of request-related service level agreements \(SLAs\) that were not met by a specific team. The data is filtered based on the assignment groups to which the logged-in user belongs to.|
|Average SLAs age|Average time span from start\_time to end\_time for all SLAs that are marked as either achieved or completed.|
|Opened SLAs|Total number of service level agreements \(SLAs\) that are in In progress or paused state.|
|Overdue SLAs|Number of open service level agreements \(SLAs\) with the **Has breached** field activated.|
|SLAs expiring today|Number of service level agreements \(SLAs\) that are scheduled to reach their deadline or expiration on the current day.|
|My team Average SLAs age|Average duration between start\_time and end\_time for all SLAs marked as achieved or completed within a specific team, filtered by the assignment groups associated with the logged-in user.|
|My team Opened SLAs|Total number of service level agreements \(SLAs\) that are either in progress or paused, specific to a team and filtered according to the assignment groups of the logged-in user.|
|My team overdue SLAs|Total number of service level agreements \(SLAs\) marked as breached within a specific team, filtered based on the assignment groups linked to the logged-in user.|
|My team SLAs expiring today|Total number of service level agreements \(SLAs\) within a specific team scheduled to reach their deadline or expire today, filtered based on the assignment groups linked to the logged-in user.|

## Proactive Service dashboard

The Proactive Service dashboard offers a detailed overview of the influence of incidents, changes, and key records on organizational operations and the extent to which it has transitioned towards a mature service delivery model.

## Proactive Service indicators

|Indicator|Description|
|---------|-----------|
|Proactive cases triggered by the incident|Number of cases where the proactive field is set to true and the Incident field is populated.|
|Proactive cases triggered by change|Number of cases where the proactive field is set to true and the Caused by Change field is populated.|
|Major cases triggered by the incident|Number of cases where the Major case state is set to Accepted and the Incident field is populated.|
|Total outage duration caused by change|Total duration of all outages associated with tasks identified by a task number starting with CHG.|
|Unplanned outages caused by the incident|Total number of outages classified as Outage with task numbers labeled as "Incident" type.|
|Planned outages caused by change|Total number of planned outages associated with task numbers categorized as Change Request.|
|Number of missed major case record SLAs|All breached SLAs associated with tasks labeled as Case and having an Accepted status in the major case state.|
|Number of problems created by case|All problems initially reported with the task type labeled as Case.|
|Number of problems created by the incident|All problems initially reported with the task type labeled as incident.|

**Parent Topic:**[Reviewing customer or partner accounts in Proactive Service Experience Workflows](reviewing-customer-accounts-360.md)

