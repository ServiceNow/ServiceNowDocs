---
title: Components installed with Pre-Visit Management
description: Several types of components are installed with installation of the Pre-Visit Management application, including tables, user roles, ServiceNow Store applications, scheduled jobs, and business rules.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Components installed with Pre-Visit Management

Several types of components are installed with installation of the Pre-Visit Management application, including tables, user roles, ServiceNow Store applications, scheduled jobs, and business rules.

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Demo data is available for this feature.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_qzw_m3l_4pb"><thead><tr><th>

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
</table>## Tables installed

<table id="table_ib2_btj_sqb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Procedure request \[sn\_previsit\_procedure\_request\]

</td><td>

Stores procedure request cases. Extends the Healthcare case \[sn\_hcls\_case\] table.

</td></tr></tbody>
</table>## ServiceNow Store applications installed

<table id="table_ldj_jhj_sqb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Healthcare and Life Sciences Service Management Core \(sn\_hcls\)

</td><td>

Provides a data model and critical digital health capabilities including patient 360-degree view, consent management, and digital documentation to better address healthcare services.

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_u5w_d1k_sqb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Send procedure consent schedule

</td><td>

Sends procedure consent document before the procedure appointment date.

</td></tr></tbody>
</table>## Business rules installed

<table id="table_lyf_vdl_4pb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Rule criteria

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create book appointment task

</td><td>

Procedure request \[sn\_previsit\_procedure\_request\]

</td><td>

After update

</td><td>

Creates an appointment task for the scheduling group when a patient opts for insurance and an agent completes the review of patient insurance.

</td></tr><tr><td>

Create insurance info task

</td><td>

Procedure request \[sn\_previsit\_procedure\_request\]

</td><td>

After update

</td><td>

Creates an insurance task for the patient when the patient service representative completes the review of a procedure request case.

</td></tr><tr><td>

Update appt booked on procedure request

</td><td>

Book appointment \[sn\_hcls\_book\_appt\_task\]

</td><td>

After insert and update

</td><td>

Indicates that an appointment is booked for a procedure request when the appointment task moves to the terminal state.

</td></tr><tr><td>

Patient access to procedure request

</td><td>

Procedure request \[sn\_previsit\_procedure\_request\]

</td><td>

Before query

</td><td>

Enables patients to view their procedure request cases.

</td></tr></tbody>
</table>