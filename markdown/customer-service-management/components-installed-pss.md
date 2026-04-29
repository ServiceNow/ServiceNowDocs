---
title: Components installed with Customer Contracts and Entitlements
description: Several types of components are installed with the Customer Contracts and Entitlements application, including tables and roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Customer Contracts and Entitlements, Product data, Set up your environment, Configure, Customer Service Management]
---

# Components installed with Customer Contracts and Entitlements

Several types of components are installed with the Customer Contracts and Entitlements application, including tables and roles.

The following roles are added with the activation of the Customer Contracts and Entitlements plugins.

<table id="table_vtz_y2m_gyb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains role

</th><th>

Targeted persona

</th></tr></thead><tbody><tr><td>

sn\_pss\_core.service\_contract\_viewerService contract viewer

</td><td>

Performs read operation on:-   customer contracts
-   Contract lines
-   Entitlements
-   Characteristics
-   Entitlement usages

</td><td>

-   sn\_prd\_pm.characteristics\_viewer

Characteristic viewer

-   sn\_prd\_pm.product\_catalog\_viewer

Product catalog viewer


</td><td>

-   sn\_customerservice.consumer\_agent

Consumer service agent

-   sn\_customerservice\_agent

Customer service agent

-   sn\_customerservice.customer\_data\_viewer

Customer data viewer


</td></tr><tr><td>

sn\_pss\_core.service\_contract\_managerService contract manager

</td><td>

Performs create/read/update operations on: -   Customer contracts
-   Contract lines
-   Entitlements
-   Characteristics
-   Entitlement usages

</td><td>

sn\_pss\_core.service\_contract\_viewerService contract viewer

</td><td>

sn\_customerservice.managerCSM Manager

</td></tr><tr><td>

sn\_pss\_core.pss\_integratorIntegration user

</td><td>

Performs create/read operations by using rest endpoints on customer contracts and entitlements.

</td><td>

sn\_customerservice.managerCSM Manager

</td><td>

sn\_pss\_core.pss\_integratorIntegration User

</td></tr></tbody>
</table>The following tables are added with the activation of the Customer Contracts and Entitlements application.

<table id="table_lqw_1dm_gyb"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Characteristics\[sn\_pss\_core\_entitlement\_characteristic\]

</td><td>

Stores the characteristic values for entitlements or customer contract lines.

</td></tr><tr><td>

Entitlement Usage\[sn\_pss\_core\_contract\_entitlement\_usage\]

</td><td>

Stores the values used by end customers for entitlement characteristics.

</td></tr><tr><td>

Service Contract\[sn\_pss\_core\_service\_contract\]

</td><td>

Stores runtime contracts.

</td></tr><tr><td>

Service Contract Line\[sn\_pss\_core\_service\_contract\_line\]

</td><td>

Stores the runtime contract lines like a service plan.

</td></tr></tbody>
</table>You can assign roles to users and groups using the ServiceNow AI Platform user administration features. For more information, see:

-   [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US)
-   [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

The default view on customer contracts and entitlements in Customer Service Management workspace is Service Contract Workspace view. It can be changed by an administrator.

