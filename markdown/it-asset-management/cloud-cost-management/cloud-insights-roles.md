---
title: Cloud Cost Management roles
description: Roles are installed with the activation of the Cloud Cost Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/cloud-insights-roles.html
release: brazil
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Cloud Cost Management reference, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Cloud Cost Management roles

Roles are installed with the activation of the Cloud Cost Management application.

## Role relationships in Cloud Cost Management

\[Omitted image "role-permissions-cloud-in.png"\] Alt text: Role relationships in Cloud Cost Management

**Note:** Starting with Cloud Cost Management 10.1.0, the discovery\_admin role has been removed from the insights\_admin, spend\_admin, and cloud\_integrations\_admin roles. As a result, the following roles that are inherited through discovery\_admin are also no longer included:

-   credential\_admin
-   sn\_capi.cloud\_developer

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

The role is in the Cloud Cost Management Core plugin. You typically assign the role to the person who is financially responsible.-   View service accounts and all the related information.
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

</td></tr><tr><td>

Insights Owner

 \[sn\_clin\_core.insights\_owner\]

</td><td>

The role is in the Cloud Cost Management Core plugin. The role spans only the Cloud Cost Management application.

 -   Define jobs and policies.
-   View data for owned service accounts.

 For more information, see [Assign service accounts to an insights\_owner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-cost-management/insights-owner-new-cloudin.md).

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
</table>**Parent Topic:**[Cloud Cost Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-cost-management/reference-cloudinsights.md)

**Related topics**  


[Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignRoleToGroup.md)

[Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignARoleToAUser.md)

