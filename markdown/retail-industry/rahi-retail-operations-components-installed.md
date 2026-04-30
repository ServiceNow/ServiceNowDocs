---
title: Components installed with Retail Core
description: Several types of components such as tables, user roles, and business rule are installed when you activate the Retail Core plugin.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Retail Core reference, Retail Core, Retail]
---

# Components installed with Retail Core

Several types of components such as tables, user roles, and business rule are installed when you activate the Retail Core plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Tables installed with Retail Core

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Retail Organization\[sn\_retail\_organization\]

</td><td>

Stores information about your retail organizations, including locations and organizational hierarchies.

</td></tr><tr><td>

Retail Case\[sn\_retail\_case\]

</td><td>

Stores information about your retail case types and provides the basis for retail case creation.**Note:** This table is an extension of the Case \[sn\_customerservice\_case\] table.

</td></tr></tbody>
</table>## Base roles installed with Retail Core

For information on configuring these roles for retail, see [Assign roles to Retail Core users](../task/rahi-retail-assign-roles-users.md).

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

</td></tr><tr><td>

sn\_retail.associate\_fulfiller

</td><td>

Creates, updates, and resolves retail cases associated to the location in which the user is associated.

</td><td>

-   sn\_customerservice.svc\_location\_agent
-   sn\_retail.case\_creator
-   sn\_retail.org\_viewer

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
|Area Manager|Location Manager Contributor|
|Regional Manager|Location Manager Contributor|
|Store Associate - Fulfiller|Location Agent|
|Store Associate|Location Contributor|
|Store Manager - Fulfiller|Location Manager Fulfiller|
|Store Manager|Location Manager Contributor|

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

 For more information, see [Configure Service Model Foundation](https://www.servicenow.com/docs/access?context=configure-industry-data-model&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

Customer Service

 \[com.sn\_customerservice\]

</td><td>

The Customer Service Management application enables you to provide service and support for your external customers using several communication channels, such as email, web, and telephone. A case is created to track the issue reported or service requested and assigned to groups or agents. Customer service agents in your organization work on the cases and resolve issues.

 For more information, see [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>## Business rules installed with Retail Core

|Business rule|Table|Rule criteria|Description|
|-------------|-----|-------------|-----------|
|Add manager member for retail org|sn\_customer\_service\_organization|After update or insert|Assigns the sn\_retail.manager role to the user added as a manager in a retail organization.|
|Restrict SO update|sn\_retail\_organization|Before update|Restricts the user from updating the Service Organization field in the Retail Organization \[sn\_retail\_organization\] table.|

**Parent Topic:**[Retail Core reference](rahi-retail-operations-reference.md)

