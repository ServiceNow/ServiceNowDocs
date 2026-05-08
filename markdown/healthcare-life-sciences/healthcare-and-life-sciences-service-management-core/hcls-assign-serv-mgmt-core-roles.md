---
title: Assign roles for Healthcare and Life Sciences Service Management Core users
description: Assign roles to control access to features, capabilities, and data in the Healthcare and Life Sciences Service Management Core application.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 3
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Assign roles for Healthcare and Life Sciences Service Management Core users

Assign roles to control access to features, capabilities, and data in the Healthcare and Life Sciences Service Management Core application.

## Before you begin

Set the application scope to Healthcare and Life Sciences using the application picker. For more information, see Application picker.

Role required: sn\_hcls.manager or admin

## About this task

Users with the roles listed in the following table can use the Healthcare and Life Sciences Service Management Core application.

<table id="table_psq_chm_cvb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_hcls.admin

</td><td>

Administers who can access sensitive data by restricting how users acquire roles in the Healthcare and Life Sciences applications.

</td><td>

-   decision\_table\_admin
-   sn\_doc.admin
-   sn\_hcls.manager
-   sn\_previsit.admin

</td></tr><tr><td>

sn\_hcls.case\_task\_viewer

</td><td>

Grants access to view tasks associated with healthcare cases.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.case\_viewer

</td><td>

Grants access to view healthcare cases.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.clinical\_data\_viewer

</td><td>

Views details of the clinical data such as immunization and procedure.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.clinical\_data\_writer

</td><td>

Edits details of the clinical data such as immunization and procedure.

</td><td>

sn\_hcls.clinical\_data\_viewer

</td></tr><tr><td>

sn\_hcls.consumer\_agent

</td><td>

Creates, views, and edits healthcare cases and works with consumers to resolve cases.

</td><td>

-   sn\_hcls.healthcare\_agent
-   sn\_customerservice.consumer\_agent

</td></tr><tr><td>

sn\_hcls.customerservice\_agent

</td><td>

Creates healthcare cases for an account and contact as a customer service agent.

</td><td>

-   sn\_hcls.healthcare\_agent
-   sn\_customerservice\_agent

</td></tr><tr><td>

sn\_hcls.data\_access\_user

</td><td>

Grants data access rights to the users who need dedicated access to certain sensitive healthcare data.

</td><td>

-   sn\_hcls.clinical\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_hcls.patient\_data\_viewer
-   sn\_hcls.practitioner\_data\_viewer
-   sn\_hcls.health\_insurance\_data\_viewer
-   sn\_hcls.revenue\_cycle\_data\_viewer

</td></tr><tr><td>

sn\_hcls.device\_data\_viewer

</td><td>

Views details of the device.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.device\_data\_writer

</td><td>

Creates, deletes, and updates the device data.

</td><td>

sn\_hcls.device\_data\_viewer

</td></tr><tr><td>

sn\_hcls.employee\_patient

</td><td>

Grants access to the users with the snc\_internal role to healthcare data and healthcare cases when authorized to view them.

</td><td>

-   sn\_customerservice.self\_contributor
-   sn\_vaccine\_sm.user
-   sn\_hcls.data\_access\_user

</td></tr><tr><td>

sn\_hcls.foundation\_data\_viewer

</td><td>

Views details of the foundation data such as organization and healthcare location.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.foundation\_data\_writer

</td><td>

Edits details of the foundation data such as organization and healthcare location.

</td><td>

sn\_hcls.foundation\_data\_viewer

</td></tr><tr><td>

sn\_hcls.healthcare\_agent

</td><td>

Accesses and views healthcare data related to patients as a contact center agent. Can view and edit the CSM Households table, Member Plan table, Pre-authorization Request table, and all clinical tables.

 Can create household members and pre-auth requests.

</td><td>

-   canvas\_user
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.customer\_data\_viewer
-   sn\_hcls.clinical\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_hcls.health\_insurance\_data\_viewer
-   sn\_hcls.patient\_data\_viewer
-   sn\_hcls.practitioner\_data\_viewer
-   sn\_hcls.report\_viewer
-   sn\_hcls.revenue\_cycle\_data\_viewer

</td></tr><tr><td>

sn\_hcls.health\_insurance\_data\_viewer

</td><td>

Views details of the health insurance data such as member plan and payer plan.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.health\_insurance\_data\_writer

</td><td>

Edits details of the health insurance data such as member plan and payer plan.

</td><td>

health\_insurance\_data\_viewer

</td></tr><tr><td>

sn\_hcls.manager

</td><td>

Manages who can perform create, read, update, and delete \(CRUD\) operations on healthcare objects within a ServiceNow instance. In addition, creates and manages accounts, contact, account relationships, contact relationships, and account consumer relationships.

</td><td>

-   canvas\_user
-   model\_manager
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.customer\_data\_viewer
-   sn\_hcls.clinical\_data\_writer
-   sn\_hcls.foundation\_data\_writer
-   sn\_hcls.health\_insurance\_data\_writer
-   sn\_hcls.patient\_data\_writer
-   sn\_hcls.practitioner\_data\_writer
-   sn\_hcls.report\_viewer
-   sn\_hcls.revenue\_cycle\_data\_writer
-   sn\_previsit.patient\_service\_agent

</td></tr><tr><td>

sn\_hcls.patient

</td><td>

Views own records including healthcare cases, addresses, patient data, and clinical data as a patient. Also, views the records of other patients including their addresses for whom they are the authorized representative. Adds comments to their healthcare cases and for whom they are the authorized representative. Views their household members, if any.

 Household members and addresses associated with a patient are maintained by using the Household Member \[csm\_household\_member\] and Location \[cmn\_location\] tables, respectively. Location is associated with the foundation domain in the Common Service Data Model \(CSDM\).

</td><td>

-   sn\_customerservice.consumer
-   sn\_hcls.clinical\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_hcls.health\_insurance\_data\_viewer
-   sn\_hcls.patient\_data\_viewer
-   sn\_hcls.practitioner\_data\_viewer
-   sn\_hcls.revenue\_cycle\_data\_viewer

</td></tr><tr><td>

sn\_hcls.patient\_data\_viewer

</td><td>

Views details of the patient data such as patient and policy consent.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.patient\_data\_writer

</td><td>

Edits details of the patient data such as patient and policy consent.

</td><td>

sn\_hcls.patient\_data\_viewer

</td></tr><tr><td>

sn\_hcls.practitioner

</td><td>

Accesses and views healthcare data related to patients as a healthcare practitioner \(a triage nurse or clinical coordinator\).

 Creates Medication Prescriptions.

 Create Immunizations.

</td><td>

-   sn\_customerservice.customer\_data\_viewer
-   sn\_hcls.clinical\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_hcls.health\_insurance\_data\_viewer
-   sn\_hcls.patient\_data\_viewer
-   sn\_hcls.practitioner\_data\_viewer
-   sn\_hcls.report\_viewer
-   sn\_hcls.revenue\_cycle\_data\_viewer

</td></tr><tr><td>

sn\_hcls.practitioner\_data\_viewer

</td><td>

Views details of the practitioner data such as practitioner and practitioner facility.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.practitioner\_data\_writer

</td><td>

Edits details of the practitioner data such as practitioner and practitioner facility.

</td><td>

sn\_hcls.practitioner\_data\_viewer

</td></tr><tr><td>

sn\_hcls.report\_viewer

</td><td>

Views reports generated from tables for which they have access as agents or managers.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.revenue\_cycle\_data\_viewer

</td><td>

Views details of the revenue cycle data such as claims.

</td><td>

None

</td></tr><tr><td>

sn\_hcls.revenue\_cycle\_data\_writer

</td><td>

Edits details of the revenue cycle data such as claims.

</td><td>

sn\_hcls.revenue\_cycle\_data\_viewer

</td></tr></tbody>
</table>## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   To assign a role to a user, see Assign a role to a user.
    -   To assign a role to a group, see Assign a role to a group.

