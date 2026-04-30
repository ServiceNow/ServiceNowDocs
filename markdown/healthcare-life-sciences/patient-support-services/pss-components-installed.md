---
title: Components installed with Patient Support Services
description: Several types of components are installed with installation of the Patient Support Services application, including tables, user roles, ServiceNow Store applications, and business rules.
locale: en-US
release: yokohama
product: Patient Support Services
classification: patient-support-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Patient Support Services reference, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Components installed with Patient Support Services

Several types of components are installed with installation of the Patient Support Services application, including tables, user roles, ServiceNow Store applications, and business rules.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

<table id="table_qzw_m3l_4pb"><thead><tr><th>

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
</table>## Tables installed

<table id="table_ec4_wdj_2rb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enrollment case \[sn\_patientservice\_enroll\_case\]

</td><td>

Stores the enrollment cases.

 The **Patient** field is mandatory for an enrollment case.

</td></tr><tr><td>

Patient service task \[sn\_patientservice\_task\]

</td><td>

Base task table from which Program Task \[sn\_patientservice\_program\_task\] and Program service item \[sn\_patientservice\_program\_service\_item\] tables are extended. Extends the Healthcare Task \[sn\_hcls\_task\] table.

</td></tr><tr><td>

Patient service training \[sn\_patientservice\_training\_task\]

</td><td>

Stores the details of the training tasks associated with a program task.

</td></tr><tr><td>

Program service item \[sn\_patientservice\_program\_service\_item\]

</td><td>

Stores the details of the program service item tasks associated with a program service.

</td></tr><tr><td>

Program Task \[sn\_patientservice\_program\_task\]

</td><td>

Stores the details of the program tasks created to fulfill services requested by a patient.

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

Auto assessment business rule

</td><td>

Enrollment case \[sn\_patientservice\_enroll\_case\]

</td><td>

After insert

</td><td>

Triggers a patient satisfaction survey when an enrollment case is set to **Closed complete**.

</td></tr><tr><td>

Cancel playbook on case inactive

</td><td>

Enrollment case \[sn\_patientservice\_enroll\_case\]

</td><td>

After update

</td><td>

Disables the activities in a playbook when the associated enrollment case state is set to **Closed complete**, **Closed incomplete**, or **Canceled**.

</td></tr><tr><td>

Change Appointment state

</td><td>

Patient service training \[sn\_patientservice\_training\_task\]

</td><td>

After update

</td><td>

Sets an appointment state to **Fulfilled** or **Canceled** when the associated conduct training task state is set to **Completed** or **Canceled**, respectively.

</td></tr><tr><td>

Populate patient and insurance

</td><td>

Pre-authorization request \[sn\_hcls\_pre\_auth\_header\]

</td><td>

After insert

</td><td>

Populates patient, practitioner, and insurance details on the Pre-authorization details form based on the name of a patient entered in an enrollment case.

</td></tr><tr><td>

Populate patient and prescriber

</td><td>

Medication Prescription \[sn\_hcls\_medication\_prescription\]

</td><td>

After insert

</td><td>

Populates patient and practitioner details on the Medication Prescription form based on the name of a patient entered in an enrollment case.

</td></tr><tr><td>

Set Child items to Cancelled

</td><td>

Enrollment case \[sn\_patientservice\_enroll\_case\]

</td><td>

After insert and update

</td><td>

Cancels all child items including open patient tasks, open enrolled program service, open enrolled program, and doc tasks when an enrollment case state changes to **Closed incomplete** or **Canceled**.

</td></tr><tr><td>

Set EPS state to Canceled

</td><td>

Program service item \[sn\_patientservice\_program\_service\_item\]

</td><td>

After update

</td><td>

Sets the state of an enrolled program service to **Canceled** when the associated program service item state is set to **Canceled**.

</td></tr><tr><td>

Set EPS state to Fulfilled

</td><td>

Program service item \[sn\_patientservice\_program\_service\_item\]

</td><td>

After update

</td><td>

Sets the state of an enrolled program service to **Fulfilled** when the associated program service item state is set to **Completed**.

</td></tr><tr><td>

Set EPS state to Pending Fulfillment

</td><td>

Program service item \[sn\_patientservice\_program\_service\_item\]

</td><td>

After update

</td><td>

Sets the state of an enrolled program service to **Pending Fulfillment** when the associated program service item state is set to **Work in Progress**.

</td></tr><tr><td>

Set PSI state to Canceled

</td><td>

Program Task \[sn\_patientservice\_program\_task\]

</td><td>

After update

</td><td>

Sets the program service item state to **Canceled** when the associated program task state is set to **Canceled**.

</td></tr><tr><td>

Set PSI state to Completed

</td><td>

Program Task \[sn\_patientservice\_program\_task\]

</td><td>

After update

</td><td>

Sets the program service item state to **Completed** when the associated program task state is set to **Completed**.

</td></tr><tr><td>

Set PSI state to Work In Progress

</td><td>

Program Task \[sn\_patientservice\_program\_task\]

</td><td>

After update

</td><td>

Sets the program service item state to **Work in Progress** when the associated program task state is set to **Work in Progress**.

</td></tr><tr><td>

Set Short description

</td><td>

Enrollment case \[sn\_patientservice\_enroll\_case\]

</td><td>

After update

</td><td>

Sets the short description of an enrollment case in the format `<program name> Enrollment Case` when the enrollment case is created or updated.

</td></tr><tr><td>

Set State to Open when Assigned

</td><td>

Enrollment case \[sn\_patientservice\_enroll\_case\]

</td><td>

After insert and update

</td><td>

Sets the enrollment case state to **Open** when the case is assigned to a care coordinator.

</td></tr></tbody>
</table>