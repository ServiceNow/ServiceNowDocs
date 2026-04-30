---
title: Components installed with Retail core
description: Several types of components such as tables, user roles, and business rule are installed when you activate the Retail Core.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Retail core

Several types of components such as tables, user roles, and business rule are installed when you activate the Retail Core.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Tables installed with Retail Core

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Retail Tasksn\_retail\_task

</td><td>

Stores information about the task details.

</td></tr></tbody>
</table>## Base roles installed with Retail Core

For information on configuring these roles for retail, see [Assign roles to Retail users](../task/rahi-retail-assign-roles-users.md).

<table id="table_d5t_ttp_bdc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_retail.associate\_contributor

</td><td>

Create, review, and comment on retail cases for the location in which the user is associated.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_retail.case\_creator
-   sn\_retail.org\_viewer
-   sn\_retail.report\_viewer

</td></tr><tr><td>

sn\_retail.associate\_fulfiller

</td><td>

Creates, updates, and resolves retail cases associated with the location in which the user is associated.

</td><td>

-   sn\_customerservice.svc\_location\_agent
-   sn\_retail.case\_creator
-   sn\_retail.org\_viewer
-   sn\_retail.report\_viewer

</td></tr><tr><td>

sn\_retail.support\_agent​

</td><td>

Creates, updates, resolves, and tracks retail cases across service organizations at the system level.

</td><td>

-   sn\_customerservice\_agent
-   sn\_retail.case\_creator​
-   sn\_retail.org\_viewer​
-   sn\_retail.report\_viewer

</td></tr><tr><td>

sn\_retail.manager\_contributor​

</td><td>

Creates, reviews, and monitors all retail cases for the location and hierarchy for the location in which the user is associated.

</td><td>

-   sn\_customerservice.svc\_location\_manager\_contributor
-   sn\_retail.associate\_contributor
-   sn\_retail.report\_viewer

</td></tr><tr><td>

sn\_retail.manager​\_fulfiller

</td><td>

Creates, updates, and resolves retail cases for the location and hierarchy in which the user is associated.

</td><td>

-   sn\_customerservice.svc\_location\_manager
-   sn\_retail.associate\_fulfiller
-   sn\_retail.report\_viewer

</td></tr></tbody>
</table>## Related Party Configurations installed with Retail Core

|Name|Default responsibility|
|----|----------------------|
|Store Associate|Location Contributor|
|Store Associate - Fulfiller|Location Agent|
|Store Manager|Location Manager Contributor|
|Store Manager - Fulfiller|Location Manager Fulfiller|
|Area Manager|Location Manager Contributor|
|Area manager - Fulfiller|Location Manager - Fulfiller|
|Regional Manager|Location Manager Contributor|
|Regional manager - Fulfiller|Location Manager - Fulfiller|

## Plugins installed with Retail Core

<table id="table_a2m_wyr_1cc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Location

 \[com.snc.business\_location\]

</td><td>

This plugin supports the Service Model Foundation, where the corporation does business with customers through physical channels such as stores and branches.

 For more information, see [Configure Service Model Foundation](https://www.servicenow.com/docs/access?context=configure-industry-data-model&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

Customer Service

 \[com.sn\_customerservice\]

</td><td>

The Customer Service Management application enables you to provide service and support for your external customers using several communication channels, such as email, web, and telephone. A case is created to track the issue reported or service requested and assigned to groups or agents. Customer service agents in your organization work on the cases and resolve issues.

 For more information, see [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

CIWF UI Components

 \(sn\_ciwf\_ui\_cmpnt\)

</td><td>

Includes common themes, widgets, and code artifacts for customer and industry workflow applications.

</td></tr></tbody>
</table>## Table installed with Retail task

|Field|Example|
|-----|-------|
|Name|RT00001|
|Subject |HQ creating a task to verify store tasks |
|Description  |Verify if stores have completed tasks as per instructions |
|Requested by |HQ Agent |
|Due date |1 week from now \(date/time\) |
|Priority |Critical/High/Medium/Low |
|Assigned to |HQ Agent |

## Business rules installed with Retail Core

|Business rule|Table|Rule criteria|Description|
|-------------|-----|-------------|-----------|
|Add manager member for retail org|sn\_customer\_service\_organization|After update or insert|Assigns the sn\_retail.manager role to the user added as a manager in a retail organization.|
|Restrict SO update|sn\_retail\_organization|Before update|Restricts the user from updating the Service Organization field in the Retail Organization \[sn\_retail\_organization\] table.|
|Hide multistore child cases|sn\_retail\_case|Before Query|Filters retail cases whose parent's child case creation state is either none or Completed successfully.|

**Parent Topic:**[Components installed with plugins](rahi-retail-components-installed-with-plugins.md)

