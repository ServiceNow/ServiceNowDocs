---
title: Healthcare and Life Sciences data model
description: The Healthcare and Life Sciences Service Management Core application provides a data model that is used in the Healthcare and Life Sciences Service Management workflows.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Configuring Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare and Life Sciences data model

The Healthcare and Life Sciences Service Management Core application provides a data model that is used in the Healthcare and Life Sciences Service Management workflows.

## Overview

The Healthcare and Life Sciences data model is compatible with the Health Level Seven International \(HL7\) industry standard including the Fast Healthcare Interoperability Resources \(FHIR\) standard. The data model applies to all Healthcare and Life Sciences industry solutions including providers, life sciences, and payers. The model includes data tables for organizations, patients, practitioners, insurance, revenue cycle, and clinical data.

The data model uses a combination of tables to store data:

-   Tables that are included with the Healthcare and Life Sciences Service Management Core application.
-   Tables that are from the Customer Service Management \(CSM\) application.
-   Tables that are from the ServiceNow AI Platform application.
-   Tables that are from the Product Catalog Management Core application.

You can install the Healthcare and Life Sciences Service Management Core application to use only its data model for a basic configuration.

## Healthcare and Life Sciences data model diagram

The following diagram shows the tables and their relationships that comprise the Healthcare and Life Sciences data model.

![Data model displaying of how tables interact, For more information on these tables, refer to the Healthcare and Life Sciences.](../image/hcls-data-model.png "Healthcare and Life Sciences data model")

## Healthcare and Life Sciences Service Management Core tables for the Healthcare and Life Sciences data model

The Healthcare and Life Sciences data model uses the following tables included within the Healthcare and Life Sciences Service Management Core application to store data.

<table id="table_p3d_b42_ppb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Allergy intolerance \[sn\_hcls\_allergy\]](../reference/hcls-allergy-intolerance.md)

</td><td>

Stores the information about a clinical assessment of an allergy or intolerance; a propensity, or a potential risk to an individual, to have an adverse reaction on future exposure to the specified substance, or class of substance.

</td></tr><tr><td>

[Appointment \[sn\_hcls\_appointment\]](../reference/hcls-appointment-table.md)

</td><td>

Stores the appointment booking details for a patient in your healthcare organization.

</td></tr><tr><td>

[Appointment participant \[sn\_hcls\_appointment\_participant\]](../reference/hcls-appointment-participant.md)

</td><td>

Stores the participant details of an appointment.

</td></tr><tr><td>

[Attribute \[sn\_hcls\_characteristic\_attribute\]](../reference/hcls-attribute.md)

</td><td>

Stores the characteristics options associated with a program or program service selected by a patient when submitting a healthcare request.

</td></tr><tr><td>

[Book appointment \[sn\_hcls\_book\_appt\_task\]](../reference/hcls-book-appointment-table.md)

</td><td>

Stores the task details for booking an appointment associated with a healthcare case or its extended case types.

</td></tr><tr><td>

[Claim diagnosis \[sn\_hcls\_claim\_diagnosis\]](../reference/hcls-claim-diagnosis-table.md)

</td><td>

Stores diagnosis information for claims.

</td></tr><tr><td>

[Claim header \[sn\_hcls\_claim\_header\]](../reference/hcls-claim-header-table.md)

</td><td>

Stores the details of the main claim submitted on behalf of a patient to a payer organization.

</td></tr><tr><td>

[Claim line \[sn\_hcls\_claim\_line\]](../reference/hcls-claim-line-table.md)

</td><td>

Stores the details of the items pertaining to a claim header.

</td></tr><tr><td>

[Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\]](../reference/hcls-clinical-device-ib-item.md)

</td><td>

Stores the details of medical devices as install base items.

</td></tr><tr><td>

[Condition \[sn\_hcls\_condition\]](../reference/hcls-condition-table.md)

</td><td>

Stores the information about a condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern.

</td></tr><tr><td>

[Dosage definition \[sn\_hcls\_dosage\_definition\]](../reference/hcls-dosage-defn-table.md)

</td><td>

Models the Dosage specification \[sn\_hcls\_dosage\_specification\] table for use as a request definition parameter.

</td></tr><tr><td>

[Dosage specification \[sn\_hcls\_dosage\_specification\]](../reference/hcls-dosage-spec-table.md)

</td><td>

Stores the information about medication product dosage associated with a program.

</td></tr><tr><td>

[Dosage variable \[sn\_hcls\_dosage\_variable\]](../reference/hcls-dosage-var-table.md)

</td><td>

Stores the variables configured for a dosage specification displayed on the Medication Prescription form of a Healthcare and Life Sciences Service Management application.

</td></tr><tr><td>

[Encounter \[sn\_hcls\_encounter\]](../reference/hcls-encounter-table.md)

</td><td>

Stores the information about an interaction between a patient and healthcare providers for providing healthcare services or assessing the health status of a patient.

</td></tr><tr><td>

[Enrolled Program \[sn\_hcls\_enrolled\_program\]](../reference/hcls-enrolled-program.md)

</td><td>

Stores the programs that a patient has been enrolled into

</td></tr><tr><td>

[Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\]](../reference/hcls-enrolled-program-service.md)

</td><td>

Stores the program services provided to a patient as part of a program enrollment process.

</td></tr><tr><td>

[Healthcare case \[sn\_hcls\_case\]](../reference/hcls-case-table.md)

</td><td>

Stores healthcare-related cases.

**Note:** The Healthcare case \[sn\_hcls\_case\] table is an abstract table and is extendable.

</td></tr><tr><td>

[Healthcare code set \[sn\_hcls\_code\_set\]](../reference/hcls-healthcare-code-set-table.md)

</td><td>

Stores the details of code sets available in your ServiceNow instance.

</td></tr><tr><td>

[Healthcare location \[sn\_hcls\_location\]](../reference/hcls-healthcare-location-table.md)

</td><td>

Stores details of the location associated with your healthcare organization.

</td></tr><tr><td>

[Healthcare organization \[sn\_hcls\_organization\]](../reference/hcls-healthcare-organization-table.md)

</td><td>

Stores the details of a healthcare organization in your ServiceNow instance.

</td></tr><tr><td>

[Healthcare Task \[sn\_hcls\_task\]](../reference/hcls-task-table.md)

</td><td>

Stores the details of the task associated with a healthcare case or a patient in your healthcare organization.

**Note:** The Healthcare Task \[sn\_hcls\_task\] is an abstract table and is extendable.

</td></tr><tr><td>

[Immunization \[sn\_hcls\_immunization\]](../reference/hcls-immunization-table.md)

</td><td>

Stores the information about an event of a patient being administered a vaccine or a record of an immunization as reported by a patient, a clinician, or another party.

</td></tr><tr><td>

[Medication \[sn\_hcls\_medication\]](../reference/hcls-medication-table.md)

</td><td>

Stores the information about a medication for the purposes of prescribing, dispensing, and administering a medication as well as for making statements about medication use.

</td></tr><tr><td>

[Medication Prescription \[sn\_hcls\_medication\_prescription\]](../reference/hcls-medication-presc-table.md)

</td><td>

Stores the information about prescriptions ordered for a patient.

</td></tr><tr><td>

[Member Plan \[sn\_hcls\_member\_plan\]](../reference/hcls-memb-plan-table.md)

</td><td>

Stores the details of a health insurance plan associated with a patient.

</td></tr><tr><td>

[Observation \[sn\_hcls\_observation\]](../reference/hcls-observation-table.md)

</td><td>

Stores the information about measurements and simple assertions made about a patient.

</td></tr><tr><td>

[Patient \[sn\_hcls\_patient\]](../reference/hcls-patient-table.md)

</td><td>

Stores the details of a patient in your healthcare organization.

</td></tr><tr><td>

[Policy \[sn\_hcls\_policy\]](../reference/hcls-policy.md)

</td><td>

Stores the details of a policy shared with patients in the Healthcare and Life Sciences applications.

</td></tr><tr><td>

[Policy consent \[sn\_hcls\_policy\_consent\]](../reference/hcls-policy-consent-table.md)

</td><td>

Stores the details of a consent accepted by a patient or a household member on behalf of the patient.

</td></tr><tr><td>

[Practitioner \[sn\_hcls\_practitioner\]](../reference/hcls-practitioner-table.md)

</td><td>

Stores the details of a practitioner in your healthcare organization.

</td></tr><tr><td>

[Practitioner location \[sn\_hcls\_practitioner\_facility\]](../reference/hcls-practitioner-location-table.md)

</td><td>

Stores the details of the location at which a practitioner provides healthcare services.

</td></tr><tr><td>

[Practitioner location specialty \[sn\_hcls\_pract\_location\_specialty\]](../reference/hcls-practitioner-loc-spec-table.md)

</td><td>

Stores the details about types of services that a practitioner can provide for an organization at a specific location.

</td></tr><tr><td>

[Practitioner specialty \[sn\_hcls\_practitioner\_specialty\]](../reference/hcls-practitioner-specialty-table.md)

</td><td>

Stores the association details of a specialty with a practitioner.

</td></tr><tr><td>

[Pre-authorization diagnosis \[sn\_hcls\_pre\_auth\_diagnosis\]](../reference/hcls-pre-auth-diagnosis-table.md)

</td><td>

Stores diagnosis information pertaining to a pre-authorization for healthcare services.

</td></tr><tr><td>

[Pre-authorization item \[sn\_hcls\_pre\_auth\_item\]](../reference/hcls-pre-auth-item-table.md)

</td><td>

Stores the details of items pertaining to a pre-authorization request for healthcare services.

</td></tr><tr><td>

[Pre-authorization request \[sn\_hcls\_pre\_auth\_header\]](../reference/hcls-pre-auth-header-table.md)

</td><td>

Stores the authorization request details for a healthcare service provided by a payer organization.

</td></tr><tr><td>

[Procedure \[sn\_hcls\_procedure\]](../reference/hcls-procedure-table.md)

</td><td>

Stores the information about an action that is or was performed on or for a patient. An action can be a physical intervention like an operation, or less invasive like long-term services, counseling, or hypnotherapy.

</td></tr><tr><td>

[Program \[sn\_hcls\_program\]](../reference/hcls-program.md)

</td><td>

Stores the programs offered by healthcare organizations.

</td></tr><tr><td>

[Program relationship \[sn\_hcls\_program\_relationship\]](../reference/hcls-program-relation.md)

</td><td>

Stores the association details between a program and program service.

</td></tr><tr><td>

[Program service \[sn\_hcls\_program\_service\]](../reference/hcls-program-service.md)

</td><td>

Stores the program services associated with a program.

</td></tr><tr><td>

[Source system \[sn\_hcls\_source\_system\]](../reference/hcls-source-system.md)

</td><td>

Stores the source and destination IDs of an external healthcare system in your ServiceNow instance.

</td></tr><tr><td>

[Update insurance information \[sn\_hcls\_insurance\_info\_task\]](../reference/hcls-insurance-info-task-table.md)

</td><td>

Stores the task details for updating the insurance information of a patient in your healthcare organization.

</td></tr></tbody>
</table>## ServiceNow AI Platform, Customer Service Management \(CSM\), and Product Catalog Management Core tables for the Healthcare and Life Sciences data model

The Healthcare and Life Sciences data model uses the following tables included within the ServiceNow AI Platform, Customer Service Management \(CSM\), and Product Catalog Management Core applications to store data.

<table id="table_q2y_mtg_2qb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Application

</th></tr></thead><tbody><tr><td>

Business location \[sn\_csm\_business\_location\]

</td><td>

Provides the business location records.

</td><td>

CSM

</td></tr><tr><td>

Case \[sn\_customerservice\_case\]

</td><td>

Provides the cases for patients associated with customer contact records.

</td><td>

CSM

</td></tr><tr><td>

Characteristic \[sn\_prd\_pm\_characteristic\]

</td><td>

Provides the attributes available for a product.

</td><td>

Product Catalog Management Core

</td></tr><tr><td>

Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td><td>

Provides the options for attributes available for a product.

</td><td>

Product Catalog Management Core

</td></tr><tr><td>

Consumer \[csm\_consumer\]

</td><td>

Provides patient records associated with consumer records.

</td><td>

CSM

</td></tr><tr><td>

Consumer profile \[sn\_csm\_consumer\_profile\]

</td><td>

Provides multiple consumer profiles.

</td><td>

CSM

</td></tr><tr><td>

Document template \[sn\_doc\_template\]

</td><td>

Provides document templates to generate standard letters or documents.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Household Member \[csm\_household\_member\]

</td><td>

Provides records of the patient members who have been added to a household.

</td><td>

CSM

</td></tr><tr><td>

Install Base Item \[sn\_install\_base\_item\]

</td><td>

Provides the products installed or in use by an account or a customer.

</td><td>

CSM

</td></tr><tr><td>

Location \[cmn\_location\]

</td><td>

Provides addresses associated with a patient.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Medical insurance model \[sn\_ent\_medical\_insurance\_model\]

</td><td>

Classifies medical insurance models, including health insurance plans and government insurance programs such as Medicare or Medicaid.

</td><td>

Expanded Model and Asset Classes Store

</td></tr><tr><td>

Product Specification \[sn\_prd\_pm\_specification\]

</td><td>

Defines, at a functional level, a product a service provider sells to the customer.

</td><td>

Product Catalog Management Core

</td></tr><tr><td>

Request Definition \[sn\_ind\_request\_definition\]

</td><td>

Associates a task type and a workflow with a request data table.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Service organization \[sn\_customer\_service\_organization\]

</td><td>

Provides records for service organizations, including business locations and internal business locations.

</td><td>

CSM

</td></tr><tr><td>

Sold product \[sn\_install\_base\_sold\_product\]

</td><td>

Provides the product purchased by a patient as a customer and references the Product Model \[cmdb\_model\] table or Service Model \[cmdb\_service\_product\_model\] table for a customer \(customer account or consumer\).

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Specification \[sn\_prd\_pm\_specification\]

</td><td>

Provides the base table for specifications included in the industry vertical applications.

</td><td>

Product Catalog Management Core

</td></tr><tr><td>

Specification Characteristic \[sn\_prd\_pm\_specification\_characteristic\]

</td><td>

Provides the characteristics for product, service, and resource specifications.

</td><td>

Product Catalog Management Core

</td></tr><tr><td>

Specification Relationship \[sn\_prd\_pm\_specification\_relationship\]

</td><td>

Provides the association between the product, service, and resource specifications and how a product offering is decomposed, fulfilled, and delivered after a customer order is received.

</td><td>

Product Catalog Management Core

</td></tr><tr><td>

Task \[task\]

</td><td>

Provides a series of standard fields used on each of the tables that extend it.

</td><td>

ServiceNow AI Platform

</td></tr><tr><td>

Variables \[var\_dictionary\]

</td><td>

Defines dynamic variables for a model used in an application form.

</td><td>

ServiceNow AI Platform

</td></tr></tbody>
</table>**Note:** To learn about ServiceNow AI Platform, CSM, and Product Catalog Management Core tables, see [Industry data model tables](https://www.servicenow.com/docs/access?context=csm-data-model-tables&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US), [Tables installed with Customer Service Management](https://www.servicenow.com/docs/access?context=r_TIWCustomerService&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US), [Tables installed with Model Management](https://www.servicenow.com/docs/access?context=c_InstalledWithModelManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US), and .

