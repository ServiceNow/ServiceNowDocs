---
title: Cloud Cost Management roles
description: You assign Cloud Cost Management roles to user groups and to individual users based on user activities and responsibilities.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Cost Management reference, Cloud Cost Management, IT Asset Management]
---

# Cloud Cost Management roles

You assign Cloud Cost Management roles to user groups and to individual users based on user activities and responsibilities.

**Important:** This information applies to both the Cloud Cost Management and Cloud Insights Billing apps. All references to Cloud Cost Management also apply to Cloud Insights Billing.

## Role relationships in Cloud Cost Management

![Role relationships in Cloud Cost Management](../image/role-permissions-cloud-in.png)

## Primary Roles

<table id="table_avl_std_mgb"><thead><tr><th>

Role title \[name\]

</th><th>

Permissions

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Cloud Insights Admin \[sn\_clin\_core.insights\_admin\]

</td><td>

The role is in the Cloud Cost Management Core plugin. You typically assign the role to the person who is financially responsible.-   Assign ownership of one or more service accounts and, optionally, the related CIs to users that have the insights\_owner role.
-   Define Business hours and Unassigned resources policies.
-   Define and view Budget plans.
-   View spend optimization reports.
-   Add report extensions.
-   Perform the actions that Cloud Cost Management recommends.

</td><td>

-   insights\_owner
-   spend\_admin
-   cloud\_integrations\_admin
-   budget\_viewer
-   \[pa\_admin\]
-   \[schedule\_admin\]
-   \[itil\]

</td></tr><tr><td>

Cloud Insights Owner \[sn\_clin\_core.insights\_owner\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 -   Define jobs and policies.
-   View data for owned service accounts.

 For more information, see [Assign service accounts to an insights\_owner](../task/insights-owner-new-cloudin-1.md).

</td><td>

insights\_user

</td></tr><tr><td>

Cloud Insights User

 \[sn\_clin\_core.insights\_user\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 View the Cloud Cost Management Workspace home page.

</td><td>

— none —

</td></tr></tbody>
</table>## Secondary roles

The roles in this section are contained in the insights\_admin role. These roles enable integration with platform \(Performance Analytics, MetricBase/Clotho\) to execute Cloud Cost Management flows.

<table id="table_t2t_5qv_4lb"><thead><tr><th>

Role title \[name\]

</th><th>

Permissions

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Cloud Spend Admin \[sn\_cld\_spend\_core.spend\_admin\]

</td><td>

The role is in the Cloud Spend Reports Core plugin.Edit the Cloud Billing dashboards.

</td><td>

-   cloud\_integrations\_admin
-   \[sn\_capi.cloud\_developer\]

</td></tr><tr><td>

Cloud Integrations Admin\[sn\_cld\_intg\_core.cloud\_integrations\_admin\]

</td><td>

The role is in the Cloud Integrations Core plugin.Configure Billing Download jobs and Price Sheet Download jobs.

</td><td>

-   \[api\_integrator\]
-   \[discovery\_admin\]
-   \[flow\_operator\]

</td></tr><tr><td>

API Integrator\[sn\_cld\_intg\_core.api\_integrator\]

</td><td>

The role is in the Cloud Integrations Core plugin.Used by the MID Server to access REST endpoints that are related to the Cloud Integrations, Cloud Integrations AWS applications, and Cloud Integrations Azure applications.

</td><td>

\[clotho\_rest\_put\]

</td></tr><tr><td>

Cloud Budget Viewer \[sn\_clin\_core.budget\_viewer\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 View Budget Forecast reports and policies.

</td><td>

— none —

</td></tr><tr><td>

PA Admin\[pa\_admin\]

</td><td>

See [Performance Analytics roles](https://www.servicenow.com/docs/access?context=r_PARoles&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

</td><td>

— none —

</td></tr><tr><td>

Clotho Put\[clotho\_rest\_put\]

</td><td>

Role that is used by the MID Server to send the billing data to the instance and store the data in MetricBase / Clotho.

</td><td>

— none —

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Cost Management reference](../concept/reference-cloudinsights.md)

**Related topics**  


[Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

[Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

