---
title: Assign HRBP roles
description: Give users access to the HRBP productivity assistant by assigning them the HRBP Hub user or admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/create-hrbp-sa-user.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Configure, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Assign HRBP roles

Give users access to the HRBP productivity assistant by assigning them the HRBP Hub user or admin role.

## Before you begin

Role required: admin

## About this task

The HRBP application includes an admin role and a user role. The admin role is for configuring HRBP components. The HRBP user role by itself does not grant access to HRSD applications data, so you must also assign roles from respective applications. For more information on HRBP roles, see [HRBP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hrbp-sa-roles.md).

These steps guide you through assigning necessary roles to a user. If your organization has more than one HR business partner, you must repeat these steps for each user. Alternatively, you can create a user group, assign roles to it, and assign users to the group. The users will inherit the group roles. For more information on groups, see [Creating groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ua-creating-groups.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Open the user record for the HR business partner.

3.  In the **Roles** related list, select **Edit**.

4.  Assign the roles for the user's persona.

<table id="choicetable_wtl_vc4_tkc"><thead><tr><th align="left" id="d477298e116">

User Persona

</th><th align="left" id="d477298e119">

Roles

</th></tr></thead><tbody><tr><td id="d477298e125">

**Admin**

</td><td>

`sn_hrbp_hub.admin`

</td></tr><tr><td id="d477298e135">

**User**

</td><td>

-   `sn_hrbp_hub.user`
-   `sn_hr_core.hrbp`
-   `sn_hr_er.case_reader`
-   `sn_hr_core.profile_reader`


</td></tr></tbody>
</table>    A standard HR business partner needs the roles listed in the User row. An HRBP administrator who configures the HRBP Productivity app, needs the sn\_hrbp\_hub.admin role, which includes the sn\_hrbp\_hub.user role.

5.  Select **Save**.


## What to do next

[Define HRBP data access and data access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

