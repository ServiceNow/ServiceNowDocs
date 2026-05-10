---
title: Determining additional user profiles in Patient Support Services
description: You can determine who can act as an agent connector or contributor for enrollment cases in the Patient Support Services application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Determining additional user profiles in Patient Support Services

You can determine who can act as an agent connector or contributor for enrollment cases in the Patient Support Services application.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

As a user with the admin role, you can create contributor and agent connector profiles with the desired level of access to enrollment cases, case tasks, and other case-related information.

The sn\_patientservice.agent\_connector and sn\_patientservice.contributor roles installed with the Patient Support Services application provide the following user profiles:

-   [Agent connector](pss-connector-contributor.md#section_ers_kby_ztb)
-   [Contributor](pss-connector-contributor.md#section_wyb_lby_ztb)

## Agent connector

An agent connector within the Patient Support Services application acts as a fulfiller who can create, update, and close enrollment cases and tasks.

As a user with the admin role, you can determine who can act as an agent connector for the enrollment cases by assigning the sn\_patientservice.agent\_connector role and other agent-specific roles to a group, and then assigning the group to the user with the agent connector profile. To assign roles to a group, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

The following table describes the location agent profile within the Patient Support Services application scope that you can refer to as an example for combining the sn\_patientservice.agent\_connector role with the [industry data model roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-data-model-roles.md) in the CSM application.

<table id="table_n1p_spx_ztb"><thead><tr><th>

Profile

</th><th>

Description

</th><th>

Assigned roles

</th></tr></thead><tbody><tr><td>

Location agent

</td><td>

Creates and fulfills enrollment cases in the agent's business location.

**Note:** To create enrollment cases for a service organization \(business location\), a user with the location agent profile must be a member of the service organization and assigned the **Location Consumer Agent** responsibility type. The mapping of a service organization and its members is included in the Service Organization Member \[sn\_csm\_service\_organization\_member\] table.

</td><td>

sn\_patientservice.agent\_connector and sn\_customerservice.svc\_location\_consumer\_agent

</td></tr></tbody>
</table>## Contributor

A contributor within the Patient Support Services application acts as a requester who can create and read enrollment cases.

As a user with the admin role, you can determine who can act as a contributor to the enrollment cases by assigning the sn\_patientservice.contributor role and other contributor roles to a group, and then assigning the group to the user with the contributor profile. To assign roles to a group, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

The following table describes different contributor profiles within the Patient Support Services application scope that you can refer to as an example for combining the sn\_patientservice.contributor role with the [contributor roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-contributor-user-roles.md) in the CSM application.

<table id="table_uvh_kmw_ztb"><thead><tr><th>

Profile

</th><th>

Description

</th><th>

Assigned roles

</th></tr></thead><tbody><tr><td>

Relationship contributor

</td><td>

Creates enrollment cases for only those patients with whom a relationship is established. For more information, see [Create relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-data-model-relationships.md).

**Note:** To create enrollment cases for a patient, a user with the relationship contributor profile must have a relationship with the patient included in the Consumer Team Member \[sn\_customer\_rel\_consumer\_to\_user\_list\] table and the **Relationship Manager** responsibility type.

</td><td>

sn\_patientservice.contributor and sn\_customerservice.relationship\_contributor

</td></tr><tr><td>

Patient contributor

</td><td>

Creates enrollment cases for any patients.

</td><td>

sn\_patientservice.contributor and sn\_customerservice.consumer\_contributor

</td></tr><tr><td>

Location contributor

</td><td>

Creates enrollment cases for any patients in a particular service organization \(business location\) with which the user is associated as a service organization member.

**Note:** To create enrollment cases for a service organization \(business location\), a user with the location contributor profile must be the member of the service organization and assigned the **Location Contributor** responsibility type. The mapping of a service organization and its members is included in the Service Organization Member \[sn\_csm\_service\_organization\_member\] table.

</td><td>

sn\_patientservice.contributor, sn\_customerservice.service\_organization\_contributor, and sn\_customerservice.consumer\_contributor

</td></tr></tbody>
</table>