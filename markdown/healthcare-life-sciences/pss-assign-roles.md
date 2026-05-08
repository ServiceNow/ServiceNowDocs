---
title: Assign roles for Patient Support Services users
description: Assign roles to control access to features, capabilities, and data in the Patient Support Services application.
locale: en-US
release: australia
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Configure, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Assign roles for Patient Support Services users

Assign roles to control access to features, capabilities, and data in the Patient Support Services application.

## Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Set the application scope to Patient Support Services using the application picker. For more information, see Application picker.

Role required: sn\_patientservice.admin or admin

## About this task

Users with the roles listed in the following table can use the Patient Support Services application.

<table id="table_ebx_hlm_cvb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_patientservice.admin

</td><td>

Administers who can access the Patient Support Services application.

</td><td>

sn\_patientservice.agent

</td></tr><tr><td>

sn\_patientservice.agent

</td><td>

Views and fulfills enrollment cases as a care coordinator.

</td><td>

sn\_hcls.healthcare\_agent

</td></tr><tr><td>

sn\_patientservice.nurse\_educator

</td><td>

Manages training requests for a Patient Support Services as a nurse educator.

**Note:** By default, the sn\_patientservice.nurse\_educator role is assigned to the members of the Nurse Training Support assignment group.

</td><td>

sn\_hcls.practitioner

</td></tr><tr><td>

sn\_patientservice.case\_creator

</td><td>

Creates enrollment cases for all associated objects.

</td><td>

sn\_patientservice.case\_viewer

</td></tr><tr><td>

sn\_patientservice.agent\_connector

</td><td>

Views, creates, and updates enrollment cases for all associated objects.

 You can combine this role with other roles for a user with the agent connector profile. For more information, see [Determining additional user profiles in Patient Support Services](../concept/pss-connector-contributor.md).

</td><td>

-   sn\_hcls.healthcare\_agent
-   sn\_patientservice.sm\_agent

</td></tr><tr><td>

sn\_patientservice.case\_task\_viewer

</td><td>

Views all tasks associated with an enrollment case that the user has access to.

</td><td>

None

</td></tr><tr><td>

sn\_patientservice.case\_viewer

</td><td>

Views all enrollment cases available in the application.

</td><td>

None

</td></tr><tr><td>

sn\_patientservice.contributor

</td><td>

Creates enrollment cases for patients.

 You can combine this role with other roles for a user with the contributor profile. For more information, see [Determining additional user profiles in Patient Support Services](../concept/pss-connector-contributor.md).

</td><td>

-   sn\_hcls.clinical\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_patientservice.case\_task\_viewer
-   sn\_hcls.patient\_data\_viewer
-   sn\_hcls.practitioner\_data\_viewer
-   sn\_hcls.health\_insurance\_data\_viewer
-   sn\_patientservice.case\_viewer
-   sn\_hcls.revenue\_cycle\_data\_viewer
-   sn\_patientservice.case\_creator

</td></tr><tr><td>

sn\_patientservice.sm\_agent

</td><td>

Accesses and views all data related to enrollment requests as a care coordinator.

</td><td>

sn\_patientservice.case\_creator

</td></tr></tbody>
</table>## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   To assign a role to a user, see Assign a role to a user.
    -   To assign a role to a group, see Assign a role to a group.

