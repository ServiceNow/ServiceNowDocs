---
title: Assign roles for Pre-Visit Management users
description: Assign roles to control access to features, capabilities, and data in the Pre-Visit Management application.
locale: en-US
release: australia
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Configure, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Assign roles for Pre-Visit Management users

Assign roles to control access to features, capabilities, and data in the Pre-Visit Management application.

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Before you begin

Set the application scope to Pre-Visit Management using the application picker. For more information, see Application picker.

Role required: sn\_previsit.admin, sn\_hcls.admin, or admin

## About this task

Users with the roles listed in the following table can use the Pre-Visit Management application.

<table id="table_amm_1lm_cvb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_previsit.admin

</td><td>

Administers who can access the Pre-Visit Management application.

</td><td>

sn\_previsit.patient\_service\_agent

</td></tr><tr><td>

sn\_previsit.patient\_service\_agent

</td><td>

Views and fulfills procedure request cases as a patient service representative.

</td><td>

sn\_hcls.healthcare\_agent

</td></tr><tr><td>

sn\_previsit.case\_creator

</td><td>

Creates procedure request cases for all associated objects.

</td><td>

sn\_previsit.case\_viewer

</td></tr><tr><td>

sn\_previsit.agent\_connector

</td><td>

Views, creates, and updates procedure request cases for all associated objects.

 You can combine this role with other roles for a user with the agent connector profile. For more information, see [Determining additional user profiles in Pre-Visit Management](../concept/pre-visit-connector-contributor.md).

</td><td>

-   sn\_hcls.healthcare\_agent
-   sn\_previsit.sm\_agent

</td></tr><tr><td>

sn\_previsit.case\_viewer

</td><td>

Views all procedure request cases available in the application.

</td><td>

None

</td></tr><tr><td>

sn\_previsit.contributor

</td><td>

Creates procedure request cases for patients.

 You can combine this role with other roles for a user with the contributor profile. For more information, see [Determining additional user profiles in Pre-Visit Management](../concept/pre-visit-connector-contributor.md).

</td><td>

-   sn\_hcls.clinical\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_hcls.patient\_data\_viewer
-   sn\_hcls.practitioner\_data\_viewer
-   sn\_hcls.health\_insurance\_data\_viewer
-   sn\_previsit.case\_viewer
-   sn\_hcls.revenue\_cycle\_data\_viewer
-   sn\_previsit.case\_creator

</td></tr><tr><td>

sn\_previsit.sm\_agent

</td><td>

Accesses and views all data related to procedure requests as a patient service representative.

</td><td>

sn\_previsit.case\_creator

</td></tr></tbody>
</table>## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   To assign a role to a user, see Assign a role to a user.
    -   To assign a role to a group, see Assign a role to a group.

