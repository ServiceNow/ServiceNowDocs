---
title: Healthcare and Life Sciences Service Management glossary
description: Learn about the terms and concepts that are unique to Healthcare and Life Sciences Service Management.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
breadcrumb: [Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare and Life Sciences Service Management glossary

Learn about the terms and concepts that are unique to Healthcare and Life Sciences Service Management.

**Parent Topic:**[Healthcare and Life Sciences Service Management Core reference](hcls-serv-mgmt-core-reference.md)

## B

Glossary terms are grouped alphabetically.

### B2B2C \(Business-to-Business-to-Consumer\)

A customer data model that enables ServiceNow to support business customers and third-party channel partners who in turn support end consumers. It must be manually enabled for HCLS-SM Core and requires the Customer Data Models for B2B2C plugin.

For Example, a medical device manufacturer enables B2B2C so that hospital contacts \(businesses\) can open healthcare cases on the CSM portal for their end-consumer patients.

## C

Glossary terms are grouped alphabetically.

### Case Summarization \(Now Assist\)

A generative AI capability leveraging Now Assist that provides a concise summary of any HCLS case type, including the issue, actions taken, and resolution details. Agents with the sn\_customerservice\_agent or consumer\_agent role can generate summaries from the Overview tab.

For example, an agent clicks “Summarize” on a procedure request case to quickly understand the case history, outstanding tasks, and current status before responding to the patient.

### Claim Header / Claim Line

Tables \(sn\_hcls\_claim\_header and sn\_hcls\_claim\_line\) that store the main claim submitted on behalf of a patient to a payer organization and its line-item details respectively. Claims link to patients, payers, and diagnosis information.

For example, after a procedure is completed, a claim header is created with the payer details, and individual claim lines capture each service, NDC code, and date of service.

### Cryptographic Module / Field-Level Encryption

AES-256 encryption modules installed with HCLS-SM Core that protect sensitive healthcare fields \(patient names, dates of birth, SSNs, insurance numbers, clinical dates\) at the column level. Access is controlled through module access policies tied to specific roles.

For example, the sn\_hcls.patient\_data crypto module encrypts the patient’s name, birth date, SSN, and phone numbers, requiring the sn\_hcls.patient\_data\_viewer role to decrypt and view them.

## D

Glossary terms are grouped alphabetically.

### Digest Token Authentication

An EMR Help authentication method for Epic Hyperspace and Hyperdrive integration. ServiceNow receives a username and AES-256 encrypted digest token in an HTTP header, validates the token, and logs the user in if a matching credential exists.

For example, a clinician opens EMR Help from Epic Hyperspace and is automatically logged into ServiceNow because digest token authentication validates their identity without a separate login prompt.

### Document Auto-Generation

A feature that uses decision tables to automatically trigger document fulfillment when specific conditions on a healthcare case are met. The Trigger document flow for HC case business rule evaluates configured document decisions on case insert or update.

For example, a decision table is configured so that when a Procedure Request case is created with a surgical procedure code, a procedure consent document is automatically generated and sent to the patient.

### Document Template

A reusable template \(HTML or PDF type\) used to digitize healthcare documents such as consent forms, privacy notices, and procedure agreements. Fields and variables from healthcare tables are mapped to the template, and participants \(roles\) are assigned for signatures.

For example, an administrator creates a “Privacy Consent” HTML document template that auto-populates the patient name, date, and organization, then routes it to the patient for digital signature.

### Dosage Specification

A configuration \(table: sn\_hcls\_dosage\_specification\) that defines the diagnosis details and dosage characteristics of a medication product associated with a program. Dosage specifications link to dosage definitions and control the dosage fields displayed on the Medication Prescription form.

For example, an admin creates a dosage specification for Drug X in the Diabetes Care program, setting the primary diagnosis, quantity per month, and maximum daily dose.

## E

Glossary terms are grouped alphabetically.

### EMR Help

A ServiceNow application \(sn\_ind\_rmt\_help\) that integrates an EMR system with a ServiceNow instance, allowing clinicians to submit IT service requests and healthcare cases directly from within the EMR. EMR session data \(workstation, patient, clinician\) is automatically captured.

For example, a clinician notices a patient record loading error in Epic, clicks the Help button, and submits a request that automatically creates an incident in ServiceNow with the workstation ID and patient MRN attached.

### EMR Help Service Portal

A dedicated service portal embedded within an EMR system \(such as Epic Hyperspace\) that provides clinicians a help form for submitting ServiceNow service requests. It supports incident and healthcare case request types with pre-populated EMR session data.

For example, an administrator embeds the EMR Help portal into Epic Hyperspace so clinicians can access it via a toolbar button and submit IT or healthcare case requests.

### Encounter

A record \(table: sn\_hcls\_encounter\) that stores information about an interaction between a patient and healthcare providers for delivering services or assessing the patient’s health status. Encounters are referenced from procedures, medication prescriptions, and other clinical records.

For example, when a patient visits the hospital for a consultation, an encounter record is created that links to the subsequent procedure and observation records.

### Enrolled Program / Enrolled Program Service

Records that track a patient’s enrollment into a specific program \(sn\_hcls\_enrolled\_program\) and the individual services they receive within that program \(sn\_hcls\_enrolled\_program\_service\).

For example, when a patient is enrolled in the Diabetes Care program, an enrolled program record is created and linked to enrolled program service records for each service they receive.

## H

Glossary terms are grouped alphabetically.

### HCLS Data Model

A structured set of ServiceNow tables compatible with the HL7 and FHIR standards that stores healthcare data including patients, practitioners, organizations, appointments, insurance, clinical records, and revenue cycle information. It combines tables from HCLS-SM Core, CSM, the ServiceNow AI Platform, and Product Catalog Management Core.

For example, the data model links a patient record to their appointments, conditions, medications, member plans, and claims across multiple related tables.

### Healthcare and Life Sciences Service Management Core \(HCLS-SM Core\)

The foundational ServiceNow scoped application \(sn\_hcls\) that provides the HCLS data model, Healthcare Workspace for agents, the Patient Portal, document templates, consent management, and digital documentation capabilities for healthcare workflows.

For example, a hospital installs HCLS-SM Core to give agents a 360-degree patient view and to digitize consent forms for procedure scheduling.

### Healthcare Case

An abstract, extendable case record \(table: sn\_hcls\_case\) that stores healthcare-related cases. Application-specific case types such as Procedure Request, Enrollment Case, and EMR Case extend this base table to support different healthcare workflows.

For example, an administrator extends the sn\_hcls\_case table to create a custom “Pharmacy Request” case type for medication fulfillment workflows.

### Healthcare Code Set

A record \(table: sn\_hcls\_code\_set\) that stores code sets available in a ServiceNow instance, providing standardized codes aligned with industry coding systems such as CPT, HCPCS, and ICD for use across healthcare workflows.

For example, an administrator imports CPT procedure codes into the healthcare code set table so that practitioners can select standardized codes when documenting procedures.

### Healthcare Task

An abstract, extendable task record \(table: sn\_hcls\_task\) associated with a healthcare case or a patient. Specific task types like Book Appointment and Update Insurance Information extend this table.

For example, when a patient needs to update their insurance details, a healthcare task of type Update Insurance Information is created and appears in the patient’s to-do list.

### Healthcare Workspace

A CSM Configurable Workspace used by healthcare agents to accept patient requests via chat or phone, view the Patient Information related list \(360-degree view\), create and manage healthcare cases, and access case summarization through Now Assist.

For example, an agent navigates to HCLS Service Management &gt; Healthcare workspace to accept an incoming call, verify the patient, and create a new healthcare case.

### Household Member

A CSM record \(table: csm\_household\_member\) that links patients to family members for whom they may serve as an authorized representative. Authorized representatives can view household members’ appointments, to-dos, and open requests on the Patient Portal.

For example, a parent registered on the Patient Portal can view their minor child’s upcoming vaccination appointments and pending consent forms through the Household Members section.

## I

Glossary terms are grouped alphabetically.

### Interaction

A record created when a patient contacts the healthcare organization via phone, chat, or other channels. Agents use interaction records in Healthcare Workspace to verify the patient identity, associate the patient record, and create healthcare cases.

For example, when a patient calls about a billing question, an interaction record is created and the agent clicks “Verify Patient” to look up and confirm the patient before opening a case.

## M

Glossary terms are grouped alphabetically.

### Medication Prescription

A record \(table: sn\_hcls\_medication\_prescription\) that stores prescriptions ordered for a patient, including medication product, practitioner, dosage specification, diagnosis details, and status. It links to programs and enrollment cases when applicable.

For example, a practitioner creates a medication prescription for a patient enrolled in a support program, and the dosage details auto-populate from the published dosage specification.

### Member Plan

A record \(table: sn\_hcls\_member\_plan\) that stores the details of a health insurance plan associated with a patient, including member number, group number, Rx Bin, Rx Group, Rx PCN, subscriber name, and effective dates.

For example, an agent views a patient’s member plan in the 360-degree view to confirm insurance coverage before creating a procedure request.

## P

Glossary terms are grouped alphabetically.

### Patient 360-Degree View

A comprehensive overview of a patient displayed in Healthcare Workspace on Interaction and Healthcare Case forms. It shows personal details, insurance, household members, conditions, medications, allergies, immunizations, cases overview, claims overview, recent interactions, and appointments.

For example, while on a call, an agent views the Patient Information related list to see the patient’s current medications, active insurance plan, and open cases.

### Patient Portal

A self-service web portal where patients with the sn\_hcls.patient role can register, view appointments, complete to-do tasks \(e.g., signing consent documents\), track healthcare request statuses, view household members, and access knowledge articles and Virtual Agent.

For example, a patient logs into the Patient Portal to review and digitally sign a privacy consent form that appears in their Pending to-dos section.

### Patient Self-Registration

A Patient Portal feature controlled by the sn\_hcls.enable\_self\_registration property that allows patients to create their own account, provide personal information, accept the privacy policy, and verify their identity via email confirmation.

For example, a new patient clicks “Create account” on the Patient Portal landing page, fills in their details, accepts the privacy policy, and receives a verification email to activate their account.

### Patient Support Services

An HCLS-SM application that streamlines patient onboarding, education, and engagement for programs such as discount plans, adherence programs, and chronic disease management. It provides the Enrollment Case type for patient program enrollment workflows.

For example, a patient calls to enroll in an opioid management program, and the agent creates an Enrollment Case that triggers eligibility checking, benefit investigation, and consent collection.

### Policy Consent

A record \(table: sn\_hcls\_policy\_consent\) that stores the details of a consent accepted by a patient or household member on behalf of a patient. The signed consent document is attached to this record, and the record is associated with the originating healthcare case.

For example, after a patient signs the privacy form on the Patient Portal, a policy consent record is created with the signed document attached and linked to the enrollment case.

### Practitioner

A record \(table: sn\_hcls\_practitioner\) that stores the details of a healthcare practitioner including name, specialties, associated facilities, and contact information. Practitioners are linked to appointments, procedures, prescriptions, and cases.

For example, a triage nurse is set up as a practitioner record linked to the Emergency Department, enabling them to create immunization and medication prescription records.

### Pre-Authorization Request

A record \(table: sn\_hcls\_pre\_auth\_header\) that stores authorization request details submitted to a payer organization for a healthcare service. It includes primary and secondary pre-auth numbers, diagnosis, approval status, and validity dates.

For example, before scheduling a surgical procedure, an agent creates a pre-authorization request to the patient’s insurance payer and tracks the approval status.

### Pre-Visit Management

An HCLS-SM application that streamlines the scheduling process of procedure requests and provides visibility into pre-authorization approvals prior to scheduled procedures. It extends the healthcare case table with the Procedure Request case type.

For example, a surgical coordinator uses Pre-Visit Management to submit a procedure request, which triggers automatic pre-authorization with the payer and consent document generation for the patient.

### Privacy Policy / Consent Management

A framework for managing patient consent through configurable policies \(table: sn\_hcls\_policy\). Policies can be Standard \(no signature required\) or Document template type \(requiring review and digital signature\). Consent validity durations, scheduled expiration, and reuse across cases are supported.

For example, an admin creates a Document template privacy policy with a 365-day validity. After the patient signs once, the accepted consent applies to all subsequent cases within that year.

### Program

A product catalog item \(table: sn\_hcls\_program\) offered by healthcare organizations to patients or consumers, such as a diabetes management program or opioid treatment program. Programs can include eligibility criteria, associated medication products, dosage specifications, and linked program services.

For example, a pharmaceutical company configures a “Diabetes Care” program with an eligibility checklist and two medication products, then publishes it for patient enrollment.

### Program Service

A product catalog item \(table: sn\_hcls\_program\_service\) offered within a program, representing a specific service such as benefit investigation, adherence coaching, or lab work coordination. Program services are linked to programs through program relationships.

For example, the “Diabetes Care” program includes a “Benefit Investigation” program service that verifies the patient’s insurance coverage before enrollment.

## R

Glossary terms are grouped alphabetically.

### Redox Inbound Integration

An HCLS-SM application that enables real-time bidirectional data exchange with external healthcare systems via the Redox platform, facilitating interoperability between ServiceNow and EMR systems.

For example, a hospital configures Redox Inbound Integration to automatically receive and store patient appointment data from their Epic EMR into the ServiceNow HCLS appointment table.

### Remote Request Definition

A configuration record in EMR Help that models a request type originating from an EMR system by associating a task table, data table, record producer, and REST API parameters. IT Service Request is the default definition for incidents.

For example, an admin creates an “HCLS Case” remote request definition linked to a custom EMR Case table and maps EMR parameters like workstation ID and patient ID.

### Remote Request Parameter

A configuration record in EMR Help that defines an EMR variable \(such as workstation ID, patient MRN, or clinician role\) to be captured from the EMR system and stored in the request data table. Parameters can be associated with specific source systems like Epic or Cerner.

For example, an admin creates a “workstation\_id” parameter mapped to the Epic source system, which auto-populates on the service request when a clinician submits from Epic.

### Restricted Caller Access \(RCA\)

A cross-scope access control mechanism that defines which applications can access resources of another application. When HCLS-SM applications are installed, the Document Templates application’s RCA privileges must be set to “Allowed” to enable document template functionality.

For example, after installing Pre-Visit Management, an admin navigates to Application Restricted Caller Access and sets the Document Templates RCA status from “Requested” to “Allowed”.

## S

Glossary terms are grouped alphabetically.

### Source System

A record \(table: sn\_hcls\_source\_system\) that stores the source and destination IDs of an external healthcare system \(such as a Redox-connected EMR\) in the ServiceNow instance, enabling custom integrations for bidirectional data exchange.

For example, an admin configures a source system record with the Redox source ID and destination ID to enable inbound patient data synchronization from an external EMR.

### Specification Characteristic

A configurable attribute \(stored in the sn\_prd\_pm\_specification\_characteristic table\) that defines an offering within a program or program service, such as benefit type, dosage quantity, or treatment frequency. Characteristics can include pre-set options or be left open for manual entry.

For example, a “Benefit Investigation” characteristic with option values “Commercial” and “Government” is added to a program service to capture the patient’s insurance type during enrollment.

## T

Glossary terms are grouped alphabetically.

### To-Do Item

A healthcare task visible to patients on the Patient Portal that must be completed as part of their healthcare activity. To-do items include tasks such as signing consent documents, updating insurance information, and completing questionnaires. Configurable via the sn\_hcls.to.do.tasks.list property.

For example, after a privacy consent policy is triggered, a to-do item appears in the patient’s Pending to-dos section on the Patient Portal, prompting them to review and sign the document.

## V

Glossary terms are grouped alphabetically.

### Vaccine Administration Management

An HCLS-SM application for managing vaccinations from start to finish, including scheduling, patient questionnaires, administration tracking, and COVID-19 status display on the Patient Portal.

For example, an organization deploys Vaccine Administration Management so patients can schedule flu vaccinations through the Patient Portal and clinicians can record administration details.

