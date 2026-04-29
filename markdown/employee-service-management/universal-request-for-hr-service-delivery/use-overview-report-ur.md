---
title: Universal Request Overview dashboard
description: View and analyze the general statistics of the universal requests for routing agents, such as the number of open requests, breached, unassigned, and requests at risk. You can also view the weekly opening and closing universal requests along with the number of department tasks that are part of each UR.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reporting solutions for Universal Request, Universal Request, Employee Service Management]
---

# Universal Request Overview dashboard

View and analyze the general statistics of the universal requests for routing agents, such as the number of open requests, breached, unassigned, and requests at risk. You can also view the weekly opening and closing universal requests along with the number of department tasks that are part of each UR.

To view the Universal Request Overview dashboard, navigate to **Universal Request** &gt; **Overview**. You can view the dashboard in the Next Experience UI Framework.

## Overview of universal requests

![Universal Request overview dashboard for reporting](../images/ur-overview-dashboard.png)

Select any indicator widget to view it's details in a list view.

Use the **Edit** button to modify the dashboard and the widgets with the in-line editor. For more information, see [Edit Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=edit-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Required ServiceNow AI Platform roles

The following roles can view the Universal Request overview dashboard:

-   Admin
-   UR Admin \[sn\_uni\_req.ur\_admin\]
-   Service owner \[sn\_uni\_req.ur\_service\_owner\]

## Users and roles

|Users and goal|Required role|
|--------------|-------------|
|Routing agent: View the dashboard.|sn\_uni\_req.routing\_agent|
|UR admin: View and edit the dashboard and manage users, groups, and roles of the dashboard|admin, sn\_uni\_req.ur\_admin|
|UR service owner: View and analyze the UR behaviors and track transfers to make informed decisions.|sn\_uni\_req.ur\_service\_owner|

## Reports

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Open P1s|Single Score|Universal Request \[universal\_request\]|Count of all open P1 requests.|
|Unassigned|Single Score|Universal Request \[universal\_request\]|Count of all requests that are open and not assigned to any UR agents.|
|SLAs Breached|Single Score|Universal Request \[universal\_request\]|Count of all requests that breached the resolution SLA.|
|Open|Single Score|Universal Request \[universal\_request\]|Count of all requests that are open.|
|SLAs at Risk|Single Score|Universal Request \[universal\_request\]|Count of all requests that crossed 75 percent of the business elapsed time.|
|Open for &gt;30 days|Single Score|Universal Request \[universal\_request\]|Request that are open for more than 30 days.|
|Department Tickets per Universal Request|Bar|Task \[task\]|This report shows all the universal requests that were created in the last 3 months along with the associated department tickets. You can view the type of department ticket created by hovering over the bars. Also, you can view the list of all the department ticket clicking on the bars.|
|Opened &amp; Closed Weekly|Spline|Universal Request \[universal\_request\]|This report shows the universal request that were opened and closed over the last 3 months, aggregated weekly.|

**Parent Topic:**[Reporting solutions for Universal Request](reporting-soln-for-ur.md)

