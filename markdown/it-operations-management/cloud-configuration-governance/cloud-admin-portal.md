---
title: Cloud Admin Portal
description: The Cloud Admin Portal is a role-based portal. You can manage, design, govern, operate, and analyze all your cloud resources from a unified base.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Admin Portal

The Cloud Admin Portal is a role-based portal. You can manage, design, govern, operate, and analyze all your cloud resources from a unified base.

Depending on the role you are logged in with, the Cloud Admin Portal displays different metrics. As an example, if you are logged in to the Cloud Provisioning and Governance application as a Cloud Service Designer, the Cloud Admin Portal displays only the **Design** metrics.

![Cloud Admin Portal](../image/admin-portal.png)

Starting this release, you can now use the **Dashboards** link on the left navigation pane of Cloud Admin Portal to access these Next Experience dashboard pages:

![Link to Next Experience Dashboard from Cloud Admin Portal](../image/admin-portal-dashboard.png)

Find the link to these dashboards on a new tab based on your user role:

-   Cloud root cause analysis dashboard
-   Cloud operations dashboard
-   Cloud tag values dashboard

Follow [Request the Cloud Provisioning and Governance application](../../cloud-management-v2-setup/task/request-plugin-cloud-mgt.md) to learn more about installing Cloud Provisioning and Governance to access the admin and user pages. Log in to the portal with the following Cloud Provisioning and Governance roles to view or manage the associated metrics:

<table id="table_y3d_gcy_1bb"><thead><tr><th>

Descriptive name and role name

</th><th>

Access to the metrics in Cloud Admin Portal

</th></tr></thead><tbody><tr><td>

Root administrator `[sn_cmp.cmp_root_admin]`

</td><td>

All the metrics.-   Overview
-   Manage
-   Design
-   laC
-   Govern
-   Operate
-   Analyze
-   Guided Setup

</td></tr><tr><td>

Cloud administrator`[sn_cmp.cloud_admin]`

</td><td>

Managethe metrics.-   Overview
-   Manage

</td></tr><tr><td>

System administrator`[admin]`

</td><td>

All the metrics.-   Overview
-   Manage
-   Design
-   laC
-   Govern
-   Operate
-   Analyze
-   Guided Setup

</td></tr><tr><td>

Governor`[sn_cmp.cloud_governor]`

`[sn_capi.cloud_developer]`

</td><td>

-   Govern
-   Analyze
-   Design

</td></tr><tr><td>

Service Designer`[sn.cmp.cloud_service_designer]`

</td><td>

Design

</td></tr><tr><td>

Operator`[sn_cmp.cloud_operator]`

</td><td>

Operate

</td></tr><tr><td>

CAPI Developer`[sn_capi.cloud_developer]`

</td><td>

Design

</td></tr></tbody>
</table>Only the Root administrator, the Cloud administrator, and the System administrator roles can view and manage all the metrics in the Cloud Admin Portal.

Click **Guided Setup** to configure the Cloud Provisioning and Governance application on your ServiceNow instance. You are guided through completing various configuration tasks. The percentage of the tasks that you have completed is displayed for you to monitor your progress.

Click **Get Help** to ask a question, open an incident, go to the product documentation or the Knowledge base website.

