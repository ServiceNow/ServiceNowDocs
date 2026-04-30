---
title: Cloud Cost Management roles
description: You assign Cloud Cost Management roles to user groups and to individual users based on user activities and responsibilities.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Cloud Cost Management, IT Asset Management]
---

# Cloud Cost Management roles

You assign Cloud Cost Management roles to user groups and to individual users based on user activities and responsibilities.

## Role relationships in Cloud Cost Management

![Role relationships in Cloud Cost Management](../image/role-permissions-cloud-in.png)

<table id="primary-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Permissions

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Insights Admin

 \[sn\_clin\_core.insights\_admin\]

</td><td>

The role is in the Cloud Cost Management Core plugin. You typically assign the role to the person who is financially responsible.-   Assign ownership of one or more service accounts and, optionally, the related CIs to users that have the insights\_owner role.
-   Define Business hours and Unassigned resources policies.
-   Define and view Budget plans.
-   View spend optimization reports.
-   Add report extensions.
-   Perform the required actions in the Cloud Cost Management application.

</td><td>

-   insights\_owner
-   spend\_admin
-   insights\_user
-   cloud\_integrations\_admin
-   budget\_viewer
-   spend\_owner
-   spend\_user
-   \[itil\]

</td></tr><tr><td>

Insights Owner

 \[sn\_clin\_core.insights\_owner\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 -   Define jobs and policies.
-   View data for owned service accounts.

 For more information, see [Assign service accounts to an insights\_owner](../task/insights-owner-new-cloudin.md).

</td><td>

insights\_user

</td></tr><tr><td>

Insights User

 \[sn\_clin\_core.insights\_user\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 View the Cloud Cost Management Workspace home page.

</td><td>

— none —

</td></tr><tr><td>

Spend Admin

 \[sn\_clin\_core.spend\_owner\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 Access the spend data for owned service accounts in the Cloud Cost Management application.

</td><td>

cloud\_integrations\_admin

</td></tr></tbody>
</table><table id="secondary-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Permissions

</th></tr></thead><tbody><tr><td>

Cloud Integrations Admin\[sn\_cld\_intg\_core.cloud\_integrations\_admin\]

</td><td>

The role is in the Cloud Integrations Core plugin.Configure Billing Download jobs and Price Sheet Download jobs.

</td></tr><tr><td>

Spend Owner\[sn\_clin\_core.spend\_owner\]

</td><td>

The role is in the Cloud Integrations Core plugin.Access all the spend data for owned service accounts in the Cloud Cost Management application.

</td></tr><tr><td>

Budget Viewer\[sn\_clin\_core.budget\_viewer\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 View Budget Forecast reports and policies.

</td></tr><tr><td>

Spend User\[sn\_cld\_spend\_core.spend\_user\]

</td><td>

The role is in the Cloud Cost Management Core plugin.

 Access Spend dashboards and tables.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Cost Management reference](../concept/reference-cloudinsights.md)

**Related topics**  


[Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

[Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

