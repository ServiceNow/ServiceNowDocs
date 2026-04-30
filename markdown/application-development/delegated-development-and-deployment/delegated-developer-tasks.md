---
title: Delegated Developer tasks
description: You can delegate deployment tasks \(application publishing, first-time installation, or update\) to developers or non-admin users, such as Change Management personnel.
locale: en-US
release: zurich
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: concept
last_updated: "2025-08-20"
reading_time_minutes: 1
breadcrumb: [Explore, Delegated Development, Planning your application, Building applications]
---

# Delegated Developer tasks

You can delegate deployment tasks \(application publishing, first-time installation, or update\) to developers or non-admin users, such as Change Management personnel.

## Delegated deployment tasks

You can delegate deployment tasks to specific users at the application level, or through assignment of specific user roles at the instance level.

<table id="table_ugl_svv_jdb"><thead><tr><th>

Assignment Method

</th><th>

Applies to

</th><th>

Available options

</th></tr></thead><tbody><tr><td>

Setting deployment permissions in Manage Developers. See [Delegating development permissions to personnel](../task/t_AddADeveloper.md)

</td><td>

Specific applications

</td><td>

Publishing and upgrades of specific applications. Publishing options include the application repository, ServiceNow Store, and update sets.

</td></tr><tr><td>

Assignment of deployment user roles to specific persons. See [Instance-specific deployment user roles](delegated_deployment_user_roles.md).

</td><td>

Local non-production instance \(for example, Development or QA\)

</td><td>

First-time installations and upgrades of all applications that contain the same company as the current instance. For example, applications for ABC Company and XYZ Company display on the Application Client page. A user with this role can only install XYZ Company applications when logged in to a XYZ Company instance. The user cannot install applications for ABC Company.

</td></tr></tbody>
</table>