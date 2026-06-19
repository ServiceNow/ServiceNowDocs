---
title: DevOps Config roles
description: DevOps Config uses these roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-family/devops-config-roles.html
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps Config reference, DevOps Config, IT Service Management]
---

# DevOps Config roles

DevOps Config uses these roles.

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

<table id="table_j2c_z4g_wpb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

\[sn\_devops.app\_admin\]

</td><td>

DevOps Config app admin

 Can create/read/update/delete DevOps Config apps.

</td><td>

None

</td></tr><tr><td>

\[sn\_devops\_config.viewer\]

</td><td>

DevOps Config viewer

 Has read-only access in DevOps Config.

</td><td>

sn\_cdm.cdm\_viewer

</td></tr><tr><td>

\[sn\_devops\_config.editor\]

</td><td>

DevOps Config editor

 Can manage config data, create/commit changesets, and publish/unpublish snapshots.

</td><td>

-   sn\_devops\_config.viewer
-   sn\_cdm.cdm\_editor

</td></tr><tr><td>

\[sn\_devops\_config.secrets\]

</td><td>

DevOps Config secrets

 Able to manage encrypted config data within an application.

</td><td>

sn\_cdm.cdm\_secrets

</td></tr><tr><td>

\[sn\_devops\_config.admin\]

</td><td>

DevOps Config admin

 Has editor role permissions plus ability to manage policies and exporters, and applications.

</td><td>

-   sn\_devops.app\_admin
-   sn\_devops\_config.editor
-   sn\_cdm.cdm\_admin

</td></tr></tbody>
</table>-   **[Roles in CDM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-roles.md)**  
List of roles and permissions in CDM.

**Parent Topic:**[DevOps Config reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-reference.md)

