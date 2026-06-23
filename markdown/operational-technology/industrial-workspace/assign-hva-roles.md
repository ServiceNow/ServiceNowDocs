---
title: Assign roles for Hardware Vulnerability Assessment
description: Assign roles to users so that they can configure properties, and use hardware vulnerability assessments features, capabilities, and data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/operational-technology/industrial-workspace/assign-hva-roles.html
release: xanadu
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Hardware Vulnerability Assessment of OT devices using guided setup, Configure, Industrial Workspace, Operational Technology]
---

# Assign roles for Hardware Vulnerability Assessment

Assign roles to users so that they can configure properties, and use hardware vulnerability assessments features, capabilities, and data.

## Before you begin

Role required: admin

## About this task

Assign the following roles to users and user groups or Hardware Vulnerability Analyst users  or user groups that are listed in the following table:

<table id="table_lmr_qdy_4bc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[sn\_vul.manage\_exposure\_assessment\]

</td><td>

Can view or edit properties for Hardware Vulnerability Assessment.

</td></tr><tr><td>

OT Vulnerability Event Manager

\[sn\_otvr.vul\_event\_manager\]

</td><td>

Can view and perform assessments related to Hardware Vulnerability Assessment.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **User Roles assignment** &gt; **Configure** &gt; **Users**.

2.  Assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

    |Task|User administration feature|
    |----|---------------------------|
    |**Assign a role to a user**|See [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).|
    |**Assign a role to a group**|See [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).|


**Parent Topic:**[Setting up Hardware Vulnerability Assessment of OT devices using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/industrial-workspace/configure-hva-using-guided-setup.md)

