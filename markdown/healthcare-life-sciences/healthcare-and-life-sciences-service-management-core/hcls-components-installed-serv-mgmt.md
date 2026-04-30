---
title: Components installed with Healthcare and Life Sciences Service Management Core
description: Several types of components are installed with installation of the Healthcare and Life Sciences Service Management Core application, including user roles, tables, plugins, ServiceNow Store applications, and business rules.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 20
breadcrumb: [Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Components installed with Healthcare and Life Sciences Service Management Core

Several types of components are installed with installation of the Healthcare and Life Sciences Service Management Core application, including user roles, tables, plugins, ServiceNow Store applications, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

User roles are assigned by the use case that is being supported. For each feature, there are both roles with view-only access and roles with various levels of interactive access.

<table id="table_qzw_m3l_4pb"><thead><tr><th>

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
</table>## Tables installed

<table id="table_nnq_kr2_ppb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Allergy intolerance \[sn\_hcls\_allergy\]](hcls-allergy-intolerance.md)

</td><td>

Stores the information about a clinical assessment of an allergy or intolerance; a propensity, or a potential risk to an individual, to have an adverse reaction on future exposure to the specified substance, or class of substance.

</td></tr><tr><td>

[Appointment \[sn\_hcls\_appointment\]](hcls-appointment-table.md)

</td><td>

Stores the appointment booking details for a patient in your healthcare organization.

</td></tr><tr><td>

[Appointment participant \[sn\_hcls\_appointment\_participant\]](hcls-appointment-participant.md)

</td><td>

Stores the participant details of an appointment.

</td></tr><tr><td>

[Attribute \[sn\_hcls\_characteristic\_attribute\]](hcls-attribute.md)

</td><td>

Stores the characteristics options associated with a program or program service selected by a patient when submitting a healthcare request.

</td></tr><tr><td>

[Book appointment \[sn\_hcls\_book\_appt\_task\]](hcls-book-appointment-table.md)

</td><td>

Stores the task details for booking an appointment associated with a healthcare case or its extended case types.

</td></tr><tr><td>

[Claim diagnosis \[sn\_hcls\_claim\_diagnosis\]](hcls-claim-diagnosis-table.md)

</td><td>

Stores diagnosis information for claims.

</td></tr><tr><td>

[Claim header \[sn\_hcls\_claim\_header\]](hcls-claim-header-table.md)

</td><td>

Stores the details of the main claim submitted on behalf of a patient to a payer organization.

</td></tr><tr><td>

[Claim line \[sn\_hcls\_claim\_line\]](hcls-claim-line-table.md)

</td><td>

Stores the details of the items pertaining to a claim header.

</td></tr><tr><td>

[Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\]](hcls-clinical-device-ib-item.md)

</td><td>

Stores the details of medical devices as install base items.

</td></tr><tr><td>

[Condition \[sn\_hcls\_condition\]](hcls-condition-table.md)

</td><td>

Stores the information about a condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern.

</td></tr><tr><td>

[Dosage definition \[sn\_hcls\_dosage\_definition\]](hcls-dosage-defn-table.md)

</td><td>

Models the Dosage specification \[sn\_hcls\_dosage\_specification\] table for use as a request definition parameter.

</td></tr><tr><td>

[Dosage specification \[sn\_hcls\_dosage\_specification\]](hcls-dosage-spec-table.md)

</td><td>

Stores the information about medication product dosage associated with a program.

</td></tr><tr><td>

[Dosage variable \[sn\_hcls\_dosage\_variable\]](hcls-dosage-var-table.md)

</td><td>

Stores the variables configured for a dosage specification displayed on the Medication Prescription form of a Healthcare and Life Sciences Service Management application.

</td></tr><tr><td>

[Encounter \[sn\_hcls\_encounter\]](hcls-encounter-table.md)

</td><td>

Stores the information about an interaction between a patient and healthcare providers for providing healthcare services or assessing the health status of a patient.

</td></tr><tr><td>

[Enrolled Program \[sn\_hcls\_enrolled\_program\]](hcls-enrolled-program.md)

</td><td>

Stores the programs that a patient has been enrolled into

</td></tr><tr><td>

[Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\]](hcls-enrolled-program-service.md)

</td><td>

Stores the program services provided to a patient as part of a program enrollment process.

</td></tr><tr><td>

[Healthcare case \[sn\_hcls\_case\]](hcls-case-table.md)

</td><td>

Stores healthcare-related cases.

**Note:** The Healthcare case \[sn\_hcls\_case\] table is an abstract table and is extendable.

</td></tr><tr><td>

[Healthcare code set \[sn\_hcls\_code\_set\]](hcls-healthcare-code-set-table.md)

</td><td>

Stores the details of code sets available in your ServiceNow instance.

</td></tr><tr><td>

[Healthcare location \[sn\_hcls\_location\]](hcls-healthcare-location-table.md)

</td><td>

Stores details of the location associated with your healthcare organization.

</td></tr><tr><td>

[Healthcare organization \[sn\_hcls\_organization\]](hcls-healthcare-organization-table.md)

</td><td>

Stores the details of a healthcare organization in your ServiceNow instance.

</td></tr><tr><td>

[Healthcare Task \[sn\_hcls\_task\]](hcls-task-table.md)

</td><td>

Stores the details of the task associated with a healthcare case or a patient in your healthcare organization.

**Note:** The Healthcare Task \[sn\_hcls\_task\] is an abstract table and is extendable.

</td></tr><tr><td>

[Immunization \[sn\_hcls\_immunization\]](hcls-immunization-table.md)

</td><td>

Stores the information about an event of a patient being administered a vaccine or a record of an immunization as reported by a patient, a clinician, or another party.

</td></tr><tr><td>

[Medication \[sn\_hcls\_medication\]](hcls-medication-table.md)

</td><td>

Stores the information about a medication for the purposes of prescribing, dispensing, and administering a medication as well as for making statements about medication use.

</td></tr><tr><td>

[Medication Prescription \[sn\_hcls\_medication\_prescription\]](hcls-medication-presc-table.md)

</td><td>

Stores the information about prescriptions ordered for a patient.

</td></tr><tr><td>

[Member Plan \[sn\_hcls\_member\_plan\]](hcls-memb-plan-table.md)

</td><td>

Stores the details of a health insurance plan associated with a patient.

</td></tr><tr><td>

[Observation \[sn\_hcls\_observation\]](hcls-observation-table.md)

</td><td>

Stores the information about measurements and simple assertions made about a patient.

</td></tr><tr><td>

[Patient \[sn\_hcls\_patient\]](hcls-patient-table.md)

</td><td>

Stores the details of a patient in your healthcare organization.

</td></tr><tr><td>

[Policy \[sn\_hcls\_policy\]](hcls-policy-1.md)

</td><td>

Stores the details of a policy shared with patients in the Healthcare and Life Sciences applications.

</td></tr><tr><td>

[Policy consent \[sn\_hcls\_policy\_consent\]](hcls-policy-consent-table.md)

</td><td>

Stores the details of a consent accepted by a patient or a household member on behalf of the patient.

</td></tr><tr><td>

[Practitioner \[sn\_hcls\_practitioner\]](hcls-practitioner-table.md)

</td><td>

Stores the details of a practitioner in your healthcare organization.

</td></tr><tr><td>

[Practitioner location \[sn\_hcls\_practitioner\_facility\]](hcls-practitioner-location-table.md)

</td><td>

Stores the details of the location at which a practitioner provides healthcare services.

</td></tr><tr><td>

[Practitioner location specialty \[sn\_hcls\_pract\_location\_specialty\]](hcls-practitioner-loc-spec-table.md)

</td><td>

Stores the details about types of services that a practitioner can provide for an organization at a specific location.

</td></tr><tr><td>

[Practitioner specialty \[sn\_hcls\_practitioner\_specialty\]](hcls-practitioner-specialty-table.md)

</td><td>

Stores the association details of a specialty with a practitioner.

</td></tr><tr><td>

[Pre-authorization diagnosis \[sn\_hcls\_pre\_auth\_diagnosis\]](hcls-pre-auth-diagnosis-table.md)

</td><td>

Stores diagnosis information pertaining to a pre-authorization for healthcare services.

</td></tr><tr><td>

[Pre-authorization item \[sn\_hcls\_pre\_auth\_item\]](hcls-pre-auth-item-table.md)

</td><td>

Stores the details of items pertaining to a pre-authorization request for healthcare services.

</td></tr><tr><td>

[Pre-authorization request \[sn\_hcls\_pre\_auth\_header\]](hcls-pre-auth-header-table.md)

</td><td>

Stores the authorization request details for a healthcare service provided by a payer organization.

</td></tr><tr><td>

[Procedure \[sn\_hcls\_procedure\]](hcls-procedure-table.md)

</td><td>

Stores the information about an action that is or was performed on or for a patient. An action can be a physical intervention like an operation, or less invasive like long-term services, counseling, or hypnotherapy.

</td></tr><tr><td>

[Program \[sn\_hcls\_program\]](hcls-program.md)

</td><td>

Stores the programs offered by healthcare organizations.

</td></tr><tr><td>

[Program relationship \[sn\_hcls\_program\_relationship\]](hcls-program-relation.md)

</td><td>

Stores the association details between a program and program service.

</td></tr><tr><td>

[Program service \[sn\_hcls\_program\_service\]](hcls-program-service.md)

</td><td>

Stores the program services associated with a program.

</td></tr><tr><td>

[Source system \[sn\_hcls\_source\_system\]](hcls-source-system.md)

</td><td>

Stores the source and destination IDs of an external healthcare system in your ServiceNow instance.

</td></tr><tr><td>

[Update insurance information \[sn\_hcls\_insurance\_info\_task\]](hcls-insurance-info-task-table.md)

</td><td>

Stores the task details for updating the insurance information of a patient in your healthcare organization.

</td></tr></tbody>
</table>## Plugins installed

<table id="table_jfn_dbl_4pb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Encryption Support plugin \(com.glide.encryption\)

</td><td>

Encrypts table columns and attachments associated with an EMR system in the Healthcare and Life Sciences applications.

</td></tr><tr><td>

Business Location plugin \(com.snc.business\_location\)

</td><td>

Enables you to create an organizational structure that includes Healthcare locations.

</td></tr><tr><td>

Customer Service Install Base Management plugin \(com.snc.install\_base\)

</td><td>

Captures the install base for a customer by creating sold products, install base items, and installed products to enable customer service agents to easily trace issues back to the right product, instances of that product, and other entities that might impact their functioning.

</td></tr><tr><td>

Document Templates plugin \(com.snc.document\_templates\)

</td><td>

Enables you to create HTML and PDF document templates to generate standard letters or documents.

</td></tr><tr><td>

Customer Service Household plugin \(com.snc.household\)

</td><td>

Enables you to create households, define the members of a household, and identify relationships between household members.

</td></tr><tr><td>

Playbook Experience Core \(com.glide.playbook\_experience.config\)

</td><td>

Enables you to visualize and interact with business process workflows in a simple, task-oriented view.

</td></tr></tbody>
</table>## ServiceNow Store applications installed

<table id="table_ldj_jhj_sqb"><thead><tr><th>

App

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Playbook Experience Components \(now\_playbook\_exp\)

</td><td>

Enables you to access Playbook Experience Components for viewing and interacting with process executions in UI Builder pages and Healthcare Workspace.

</td></tr><tr><td>

Playbook Experience \(sn\_playbook\_exp\)

</td><td>

Enables you to view and interact with business process workflows in real time.

</td></tr><tr><td>

Playbooks for Customer Service Management \(sn\_csm\_playbook\)

</td><td>

Enables the CSM Configurable Workspace playbook experience.

</td></tr><tr><td>

Product Catalog Management Core \(sn\_prd\_pm\)

</td><td>

Includes the base product catalog data model and functionality to define product, services, and resource specifications, and product offerings based on those specifications

</td></tr><tr><td>

Industry Core \(com.sn\_ind\)

</td><td>

Includes common objects, code artifacts, and request definitions for industry vertical applications.

</td></tr><tr><td>

CIWF UI Components \(sn\_ciwf\_ui\_cmpnt\)

</td><td>

Includes common themes, widgets, and code artifacts for customer and industry workflow applications.

</td></tr><tr><td>

CMDB CI Class Models

</td><td>

Includes class models for medical devices that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships, if applicable.

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_u5w_d1k_sqb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set inactive status for expired policy consents

</td><td>

Sets the status of policy consents to inactive when the policy validity duration has expired.

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

Add/Update member plan

</td><td>

Update insurance information \[sn\_hcls\_insurance\_info\_task\]

</td><td>

After update

</td><td>

Updates the member plan when the payment type is set to insurance.

</td></tr><tr><td>

Autofill name

</td><td>

Practitioner \[sn\_hcls\_practitioner\]

</td><td>

Before insert and update

</td><td>

Fills the **Name** field value from the prefix, given name, family name, or suffix field when the **Name** field in the Practitioner \[sn\_hcls\_practitioner\] table is not set.

</td></tr><tr><td>

Clear insurance if patient opts self pay

</td><td>

Update insurance information \[sn\_hcls\_insurance\_info\_task\]

</td><td>

Before update

</td><td>

Updates the payer field when the payment type is set to self-pay.

</td></tr><tr><td>

Create consumer for patient if not set

</td><td>

Patient \[sn\_hcls\_patient\]

</td><td>

After insert

</td><td>

Creates the consumer record after a patient is created and sets the **Consumer** field from the patient record and associates the consumer with the patient.

</td></tr><tr><td>

Create dosage definition

</td><td>

Dosage specification \[sn\_hcls\_dosage\_specification\]

</td><td>

Before insert and update

</td><td>

Creates a dosage definition for a dosage specification.

</td></tr><tr><td>

Create dosage variables

</td><td>

Dosage specification \[sn\_hcls\_dosage\_specification\]

</td><td>

Before insert and update

</td><td>

Creates dosage variables for specification characteristics.

</td></tr><tr><td>

Patient access to allergy table

</td><td>

Allergy intolerance \[sn\_hcls\_allergy\]

</td><td>

Before query

</td><td>

Runs the `Allergies - authorized to view` before query when a patient queries the Allergy intolerance \[sn\_hcls\_allergy\] table in the list or form view.

</td></tr><tr><td>

Patient access to appointment table

</td><td>

Appointment \[sn\_hcls\_appointment\]

</td><td>

Before query

</td><td>

Runs the `Allergies - authorized to view` before query when a patient queries the Allergy intolerance \[sn\_hcls\_allergy\] table in the list or form view.

</td></tr><tr><td>

Patient access to case table

</td><td>

Healthcare case \[sn\_hcls\_case\]

</td><td>

Before query

</td><td>

Runs the `Healthcare cases - authorized to view` before query when a patient queries the Healthcare case \[sn\_hcls\_case\] table in the list or form view.

</td></tr><tr><td>

Patient access to claim header table

</td><td>

Claim header \[sn\_hcls\_claim\_header\]

</td><td>

Before query

</td><td>

Runs the `Claim headers - authorized to view` before query when a patient queries the Claim header \[sn\_hcls\_claim\_header\] table in the list or form view.

</td></tr><tr><td>

Patient access to claim line table

</td><td>

Claim line \[sn\_hcls\_claim\_line\]

</td><td>

Before query

</td><td>

Runs the `Claim lines - authorized to view` before query when a patient queries the Claim line \[sn\_hcls\_claim\_line\] table in the list or form view.

</td></tr><tr><td>

Patient access to condition table

</td><td>

Condition \[sn\_hcls\_condition\]

</td><td>

Before query

</td><td>

Runs the `Conditions - authorized to view` before query when a patient queries the Condition \[sn\_hcls\_condition\] table in the list or form view.

</td></tr><tr><td>

Patient access to encounter table

</td><td>

Encounter \[sn\_hcls\_encounter\]

</td><td>

Before query

</td><td>

Runs the `Encounters - authorized to view` before query when a patient queries the Encounter \[sn\_hcls\_encounter\] table in the list or form view.

</td></tr><tr><td>

Patient access to Immunization table

</td><td>

Immunization \[sn\_hcls\_immunization\]

</td><td>

Before query

</td><td>

Runs the `Immunization - authorized to view` before query when a patient queries the Immunization \[sn\_hcls\_immunization\] table in the list or form view.

</td></tr><tr><td>

Patient access to Medication table

</td><td>

Medication \[sn\_hcls\_medication\]

</td><td>

Before query

</td><td>

Runs the `Medication - authorized to view` before query when a patient queries the Medication \[sn\_hcls\_medication\] table in the list or form view.

</td></tr><tr><td>

Patient access to Member Plan table

</td><td>

Member Plan \[sn\_hcls\_member\_plan\]

</td><td>

Before query

</td><td>

Runs the `Member Plan - authorized to view` before query when a patient queries the Member Plan \[sn\_hcls\_member\_plan\] table in the list or form view.

</td></tr><tr><td>

Patient access to observation table

</td><td>

Observation \[sn\_hcls\_observation\]

</td><td>

Before query

</td><td>

Runs the `Observations - authorized to view` before query when a patient queries the Observation \[sn\_hcls\_observation\] table in the list or form view.

</td></tr><tr><td>

Patient access to patient table

</td><td>

Patient \[sn\_hcls\_patient\]

</td><td>

Before query

</td><td>

Runs the `Patients - represented by me` before query when a patient queries the Patient \[sn\_hcls\_patient\] table in the list or form view.

</td></tr><tr><td>

Patient access to procedure table

</td><td>

Procedure \[sn\_hcls\_procedure\]

</td><td>

Before query

</td><td>

Runs the `Procedures - authorized to view` before query when a patient queries the Procedure \[sn\_hcls\_procedure\] table in the list or form view.

</td></tr><tr><td>

Populate duration

</td><td>

Encounter \[sn\_hcls\_encounter\]

</td><td>

Before insert and update

</td><td>

Calculates and sets the duration of the encounter from the start\_time and end\_time values of the Encounter \[sn\_hcls\_encounter\] table.

</td></tr><tr><td>

Populate managing org field

</td><td>

Location \[sn\_hcls\_location\]

</td><td>

Before insert and update

</td><td>

Sets the managing organization from the parent location, if it is not already set.

</td></tr><tr><td>

Populate Name

</td><td>

Patient \[sn\_hcls\_patient\]

</td><td>

Before insert and update

</td><td>

Fills the **Name** field value from the prefix, given name, family name, or suffix field when the **Name** field in the Patient \[sn\_hcls\_patient\] table is not set.

</td></tr><tr><td>

populate primary member plan

</td><td>

Update insurance information \[sn\_hcls\_insurance\_info\_task\]

</td><td>

Before insert

</td><td>

Populates the member plan information from the **Primary member plan** field of the Update insurance information \[sn\_hcls\_insurance\_info\_task\] table.

</td></tr><tr><td>

Populate valid until from validity dur

</td><td>

Policy consent \[sn\_hcls\_policy\_consent\]

</td><td>

Before insert and update

</td><td>

Sets the valid until value for a policy consent based on the date when the consent was given and the validity duration of the policy.

</td></tr><tr><td>

Practitioner NPI is unique

</td><td>

Practitioner \[sn\_hcls\_practitioner\]

</td><td>

Before insert and update

</td><td>

Aborts the insert or update operation in case of duplicate Practitioner ID or NPI field value.

</td></tr><tr><td>

Set consumer in healthcare case

</td><td>

Healthcare case \[sn\_hcls\_case\]

</td><td>

Before insert and update

</td><td>

Sets the **Consumer** field in the Healthcare case \[sn\_hcls\_case\] to a patient associated with the case when a healthcare case is created or updated.

</td></tr><tr><td>

Set consumer in healthcare sold product

</td><td>

Healthcare sold product \[sn\_hcls\_sold\_product\]

</td><td>

Before insert and update

</td><td>

Sets the **Consumer** field in the Healthcare sold product \[sn\_hcls\_sold\_product\] table to the patient’s consumer name.

</td></tr><tr><td>

Set Date Enrolled

</td><td>

Enrolled program service \[sn\_hcls\_enrolled\_program\_service\]

</td><td>

Before update

</td><td>

Sets the **Date enrolled** field value to the current date and time when the enrolled program service state changes to **Enrolled**.

</td></tr><tr><td>

Set Date Enrolled

</td><td>

Enrolled program \[sn\_hcls\_enrolled\_program\]

</td><td>

Before update

</td><td>

Sets the **Date enrolled** field value to the current date and time when the enrolled program state changes to **Enrolled**.

</td></tr><tr><td>

Set Date Fulfilled

</td><td>

Enrolled program service \[sn\_hcls\_enrolled\_program\_service\]

</td><td>

Before update

</td><td>

Sets the **Date fulfilled** field value to the current date and time when the enrolled program service state changes to **Fulfilled**.

</td></tr><tr><td>

Set dosage details from variables

</td><td>

Medication Prescription \[sn\_hcls\_medication\_prescription\]

</td><td>

Before insert and update

</td><td>

Copies variable values from a dosage characteristic on a medication prescription to the actual field on the dosage details on the medication prescription as mapped by the DosageCharacteristicsMapper script include.

</td></tr><tr><td>

Set display name

</td><td>

Medication product model \[sn\_hcls\_medication\_product\]

</td><td>

Before insert and update

</td><td>

Sets the display name of a medication product to the product model name appended with the Form code.

</td></tr><tr><td>

Set managing org to location's org

</td><td>

Practitioner location \[sn\_hcls\_practitioner\_facility\]

</td><td>

Before insert and update

</td><td>

Sets the **Organization** field in the Service Organization \[sn\_customer\_service\_organization\] table to the location’s managing organization.

</td></tr><tr><td>

Set patient self pay

</td><td>

Update insurance information \[sn\_hcls\_insurance\_info\_task\]

</td><td>

After update

</td><td>

Sets the **Patient self pay**, **Insurance verified**, and**Pre-authorization completed** field values to `true` when the case state changes to **Closed complete** and the payment type is selected as **Self pay**.

</td></tr><tr><td>

Set policy consents inactive by policy

</td><td>

Patient \[sn\_hcls\_patient\]

</td><td>

After update

</td><td>

Sets the policy consent record to inactive when the status of a policy is updated to inactive.

</td></tr><tr><td>

Set user from practitioner user

</td><td>

Practitioner location \[sn\_hcls\_practitioner\_facility\]

</td><td>

Before insert

</td><td>

Sets the **User** field in the Service Organization Member \[sn\_csm\_service\_organization\_member\] table to the practitioner’s **User** field.

</td></tr><tr><td>

Trigger document flow for HC case

</td><td>

Healthcare case \[sn\_hcls\_case\]

</td><td>

After insert and update

</td><td>

Evaluates all document decisions that have the case reference configured as input and when the decision conditions are satisfied, initiates the document workflow for the associated document template.

</td></tr><tr><td>

Update consumer info from patient

</td><td>

Patient \[sn\_hcls\_patient\]

</td><td>

After update

</td><td>

Sets the **Phone number** and **Email** fields in the consumer record from the associated patient record.

</td></tr><tr><td>

Update docs generated

</td><td>

Attachment \[sys\_attachment\]

</td><td>

After insert

</td><td>

Updates the **Documents generated** field in the Healthcare case \[sn\_hcls\_case\] table with the name of the documents that are generated or attached.

</td></tr><tr><td>

Update fields with dosage specification

</td><td>

Medication Prescription \[sn\_hcls\_medication\_prescription\]

</td><td>

Before insert and update

</td><td>

Updates the primary, secondary, and tertiary diagnosis field values from a dosage specification on a medication prescription.

</td></tr><tr><td>

Update patient on policy consent

</td><td>

Patient \[sn\_hcls\_patient\]

</td><td>

After insert

</td><td>

Updates the patient name in the policy consent record for a newly created patient record.

</td></tr><tr><td>

Validate unique doc template for policy

</td><td>

Policy \[sn\_hcls\_policy\]

</td><td>

Before insert and update

</td><td>

Validates that only one active policy is associated with a document template.

</td></tr><tr><td>

Validate and set patient

</td><td>

Healthcare Task \[sn\_hcls\_task\]

</td><td>

Before insert

</td><td>

Sets the patient value on the Healthcare Task \[sn\_hcls\_task\] table.

</td></tr><tr><td>

Validate and set SSN

</td><td>

Patient \[sn\_hcls\_patient\]

</td><td>

Before insert and update

</td><td>

Validates that only the last four digits are set in the **Social security number** field in the Patient \[sn\_hcls\_patient\] table and prepends with `*** - **` to set the value in the database.

</td></tr><tr><td>

Validate relation and update subscriber

</td><td>

Member Plan \[sn\_hcls\_member\_plan\]

</td><td>

Before insert and update

</td><td>

Sets subscriber to the patient if the relationship is set to Self. Validates the relationship field value if the subscriber is set.

</td></tr></tbody>
</table>**Note:** To learn about before query business rules, see [Before Query business rules](https://www.servicenow.com/docs/access?context=bp-before-query-business-rules&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

