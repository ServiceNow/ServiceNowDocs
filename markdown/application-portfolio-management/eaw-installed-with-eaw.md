---
title: Components installed with Enterprise Architecture Workspace
description: Several types of components are installed with Enterprise Architecture Workspace including user roles, scheduled jobs, tables, and scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-installed-with-eaw.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [Install Enterprise Architecture Workspace, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Components installed with Enterprise Architecture Workspace

Several types of components are installed with Enterprise Architecture Workspace including user roles, scheduled jobs, tables, and scripts.

## Roles installed with Enterprise Architecture Workspace

The following roles are available in Enterprise Architecture Workspace. After access is granted to a role, all users and groups assigned to that role inherit the permissions. Roles can contain other roles, and any access granted to a role is also granted to any role that includes it. For the full breakdown of which roles are required for each functional area, see [Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-access-roles.md).

|Role|Description|Typical persona|
|----|-----------|---------------|
|sn\_apm.apm\_admin|Full administrative access to configure and manage Enterprise Architecture Workspace settings, including Setup page configuration for all functional areas. Includes all permissions of sn\_apm.apm\_analyst.|EA administrator, IT architect lead|
|sn\_apm.apm\_analyst|Create and manage key portfolio records such as business applications and digital integrations. Approve or reject requests when assigned to the Enterprise Architect group. Includes all permissions of sn\_apm.apm\_user.|Enterprise architect, solution architect|
|sn\_apm.apm\_user|Create and update portfolio data across business architecture, information portfolio, technology portfolio, modeling, and data certification. Includes all permissions of sn\_apm.apm\_read.|Application owner, business analyst, portfolio manager|
|sn\_apm.apm\_read|Read-only access to all pages and records in Enterprise Architecture Workspace. Cannot create or update data. For more information, see [Business stakeholder role for Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-business-stakeholder-role.md).|Business stakeholder, executive, auditor|

## Scheduled jobs installed with Enterprise Architecture Workspace

<table id="table_w43_ssf_vzb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update Capability Hierarchies In Grid

</td><td>

Updates business capabilities hierarchy in the Business Portfolio page. A hierarchy ID is assigned to the newly created capability.

</td></tr><tr><td>

Populate Number field in TPM Discovered Technologies

</td><td>

Populates missing Technology Lifecycle Management \(TLM\) lifecycle record identifiers for TPM Discovered Technology records created with TPM plug-in versions earlier than 1.9.0.

</td></tr><tr><td>

Populate Technology Lifecycle Risks

</td><td>

Populates the TPM technology lifecycle risks data in the TPM Technology Lifecycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.

</td></tr><tr><td>

Populate TPM Discovered Technologies and Lifecycles

</td><td>

Populates the technology lifecycle data in the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table. The data includes end of support date, end of extended support date, and end of life date for your software and hardware models.**Note:** The data for the software products is displayed only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

</td></tr><tr><td>

Populate TRM technical debts in the EA Workspace

</td><td>

Populates the latest technical debt data for your application portfolio the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table.**Note:** The **Populate TRM technical debts in the EA Workspace** scheduled job will be available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

</td></tr><tr><td>

Populate TRM Technical debt for production applications

</td><td>

 

</td></tr><tr><td>

Delete Archived Tech Debts

</td><td>

Runs automatically on the first day of every month and deletes Archived technical debt records whose **Updated** value is older than the retention period set in the system property **sn\_apm\_tpm.monthsToDeleteArchivedTechDebt**. The default retention period is 12 months. You can run this job manually to apply a retention period change immediately.

</td></tr><tr><td>

CSDM Product Model Assignment

</td><td>

Generates the Model ID for existing business applications with empty Model ID fields. An application model is a structured representation of a business application's components and their relationships and interactions within your application landscape.

</td></tr><tr><td>

Sync TRM Product Names with Software Products

</td><td>

Syncs the names of Technology Reference Model \(TRM\) products of type Software with the names of their linked Software Asset Management \(SAM\) software products in the TRM Products \[sn\_apm\_trm\_standards\_product\] table. This scheduled job is inactive by default and runs on demand.

</td></tr><tr><td>

Update Score Range in Indicator Score Table

</td><td>

Populates the TCO score range field on existing Indicator Score \[apm\_app\_indicator\_score\] records. Run this job on upgraded instances so the **Business applications by TCO score** widget on the **Portfolio TCO** dashboard displays TCO score bands instead of **\(empty\)**. The job is inactive by default and must be run on demand.

</td></tr></tbody>
</table>## Tables installed with Enterprise Architecture Workspace

<table id="table_i4z_t1w_dwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BA Product Model Map \[sn\_apm\_ws\_ba\_product\_model\_map

\]

</td><td>

Stores the mapping between a business application and its application model.

</td></tr><tr><td>

Business Application TRM Product Map \[sn\_apm\_ws\_business\_app\_trm\_product\_map

\]

</td><td>

Stores the mapping between a business application's discovered technology and the TRM product that governs its obsolescence status.

</td></tr><tr><td>

APM EA Configuration \[sn\_apm\_ws\_ea\_configuration

\]

</td><td>

Stores Enterprise Architecture Workspace customization and access management configuration.

</td></tr><tr><td>

EA doc page \[sn\_apm\_ws\_ea\_doc\_page

\]

</td><td>

Stores architectural document pages created from document templates in Enterprise Architecture Workspace.

</td></tr><tr><td>

Software Model Risks \[sn\_apm\_tpm\_software\_model\_risk\]

</td><td>

Stores software models that are at risk.

</td></tr><tr><td>

Software Risk Parameter Scores \[sn\_apm\_tpm\_risk\_param\_score\]

</td><td>

Stores software models that are nearing their end of life.

</td></tr><tr><td>

Hardware Model Risks \[sn\_apm\_tpm\_hardware\_model\_risk\]

</td><td>

Stores hardware models that are at risk.

</td></tr><tr><td>

Hardware Risk Parameter Scores \[sn\_apm\_tpm\_hm\_risk\_param\_score\]

</td><td>

Stores hardware models nearing their end of life.

</td></tr><tr><td>

TPM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\]

</td><td>

Stores hardware and software elements in your enterprise.

</td></tr><tr><td>

TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\]

</td><td>

Stores the technology life cycles associated with the discovered technologies.

</td></tr><tr><td>

TPM Technology Lifecycle Exception \[sn\_apm\_tpm\_technology\_lifecycle\_exception\]

</td><td>

Stores the life cycles that were approximated or couldn’t be found from ServiceNow® Software Asset Management Professional or ServiceNow® Hardware Asset Management Professional.

</td></tr><tr><td>

TPM Discovered Technology Run Log \[sn\_apm\_tpm\_discovered\_technology\_run\_log\]

</td><td>

Stores when ServiceNow® Technology Lifecycle Management \(TPM\) refreshed its contents against Software Asset Management Professional and Hardware Asset Management Professional.

</td></tr><tr><td>

TPM Technology Risk \[sn\_apm\_tpm\_technology\_risk\]

</td><td>

Stores the TPM technology risk information.

</td></tr><tr><td>

TRM Product Capability Map \[sn\_apm\_ws\_trm\_prod\_cap\_map

\]

</td><td>

Stores the mapping between product capabilities and TRM products.

</td></tr><tr><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request

\]

</td><td>

Stores requests to add a new lifecycle to an existing TRM product.

</td></tr><tr><td>

TRM Product Request \[sn\_apm\_trm\_product\_request

\]

</td><td>

Stores requests to add a new product to the TRM.

</td></tr><tr><td>

TRM Category \[sn\_apm\_trm\_standards\_category

\]

</td><td>

Stores the categories used to group TRM products.

</td></tr><tr><td>

TRM Phase \[sn\_apm\_trm\_standards\_phase

\]

</td><td>

Stores the lifecycle phases \(approved, unapproved, approved with constraints, divest, and evaluation\) that can be assigned to a TRM product lifecycle.

</td></tr><tr><td>

TRM Product \[sn\_apm\_trm\_standards\_product

\]

</td><td>

Stores the software and hardware products defined in the Technology Reference Model.

</td></tr><tr><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle

\]

</td><td>

Stores the lifecycle records \(version or edition, phase, and start and end dates\) associated with a TRM product.

</td></tr><tr><td>

TRM Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt

\]

</td><td>

Stores technical debt records for software in business applications that isn't aligned with approved TRM software phases.

</td></tr></tbody>
</table>## UI policies installed with Enterprise Architecture Workspace

|UI Policy|Table|
|---------|-----|
|Manage access is false|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]|
|Customization type is visualization|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]|
|Customization type is script|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]|
|Manage access is true|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]|
|Show Subscriber Subtype when type = Data| |
|Show/Hide Subscriber Company| |
|Show subtype when subscriber type = data|Digital Integration \[sn\_apm\_di\_digital\_integration\]|
|Show Hide Digital Integration Field|Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]|
|Make Provider BA read -only|Digital Integration \[sn\_apm\_di\_digital\_integration\]|
|Show subtype when subscriber type = data|Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]|
|Show/Hide Subscriber Business Application| |
|Field "Integration User \(ServiceNow\)" is editable, when the Provider Business Application of the related Digital Interface is set to Platform Host = ServiceNow|Credential \[sn\_apm\_di\_credential\]|
|Show integration name field when 'Is New Integration' is true| |
|Field "Connection and Credential Alias" is editable, when the Provider Business Application of the related Digital Interface is set to Platform Host = ServiceNow|Credential \[sn\_apm\_di\_credential\]|
|Strict hide fields for retire flow|Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]|
|show hide fields based for request new integration|Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]|
|show hide fields based for retire request|Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]|
|When Data Flow Direction is --None-- or "Bidirectional", hide the Initiating Application field|Digital Integration \[sn\_apm\_di\_digital\_integration\]|
|Hide the column Provider Digital Interface if it is empty|Digital Integration \[sn\_apm\_di\_digital\_integration\]|
|Set the field Activity Type to read only|Business Process Activity \[cmdb\_ci\_business\_process\_activity\]|
|Hide the column Value Stream if it is empty|Value Stream Stage \[cmn\_value\_stream\_stage\]|

## Client scripts installed with Enterprise Architecture Workspace

<table id="table_bl2_553_c3c"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide/Show Product Capability Related Lis

</td><td>

Business Application \[cmdb\_ci\_business\_app\]

</td><td>

Hide Product Capability related list when model\_id is empty.

</td></tr><tr><td>

Hide Type Field

</td><td>

Architectural Artifact \[sn\_apm\_architectural\_artifact\]

</td><td>

 

</td></tr><tr><td>

if manage access is false

</td><td>

APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]

</td><td>

 

</td></tr><tr><td>

if section is overview

</td><td>

APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]

</td><td>

 

</td></tr><tr><td>

Set ADR Type For Artifact Version

</td><td>

Architectural Artifact Version \[sn\_apm\_architectural\_version\]

</td><td>

 

</td></tr><tr><td>

Show hardware/software product fields

</td><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle\]

</td><td>

 

</td></tr><tr><td>

Show hardware/software product fields

</td><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

 

</td></tr><tr><td>

Auto Populate HWModel relatedFields

</td><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

 

</td></tr><tr><td>

Set Category Mandatory

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Type field change

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Enable/Disable Other Categories

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Enable/Disable Other Categories

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Handle field properties

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Handle field properties

</td><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle\]

</td><td>

 

</td></tr><tr><td>

Type field change

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

is New Product field change

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

is New Product field change

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Handle Field properties

</td><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

 

</td></tr><tr><td>

Auto Populate HWModel relatedFields

</td><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle\]

</td><td>

 

</td></tr><tr><td>

Populate Publisher from Hardware Product

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Read Only TRM product fields

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Set Category Mandatory

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Architectural Version Allowed File Types

</td><td>

Architectural Artifact Version \[sn\_apm\_architectural\_version\]

</td><td>

This script allows only 3 file types to choose from when creating a new Architectural Artifact version.

</td></tr></tbody>
</table>## System properties installed with Enterprise Architecture Workspace

|System property|Description|
|---------------|-----------|
|sn\_apm\_ws.appRationalizationMaximumBubbles|Maximum number of bubbles on the bubble chart to be shown|
|sn\_apm\_ws.app\_indicator\_scoring\_profile| |
|sn\_apm\_ws.app\_rationalization\_default\_filter|Application Rationalization Default Filter|
|sn\_apm\_ws.batch\_size\_ba\_lifecycle\_gantt| |
|sn\_apm\_ws.certificationPolicyTables|Default tables used to show certification policies on enterprise architecture workspace|
|sn\_apm\_ws.record\_mention\_config|Configuration for tagging other ServiceNow records with architectural artifacts in Enterprise Architecture Workspace.|
|glide.ui.sn\_apm\_trm\_product\_lifecycle\_request\_activity.fields|TRM Product Lifecycle Request activity formatter fields|
|glide.ui.sn\_apm\_trm\_product\_request\_activity.fields|TRM Product Request activity formatter fields|
|sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled|Make this property false to disable calculating level 2 technical debt.|
|sn\_apm\_trm.noOfPublishersPerTRMPage|Number of publishers to show per page.|
|sn\_apm\_tpm.configurationItemsWithSoftwareInstalls|Non hardware configuration items which have software models for TPM discovery process|
|sn\_apm\_tpm.discoveryModelProductTypesForTPM|Product types of discovery models to consider for TPM software suggestions|

## Business rules installed with Enterprise Architecture Workspace

<table id="table_efb_w33_c3c"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default title for doc page collection

</td><td>

EA doc page \[sn\_apm\_ws\_ea\_doc\_page\]

</td><td>

 

</td></tr><tr><td>

Populate default values for version note

</td><td>

Architectural Artifact Version \[sn\_apm\_architectural\_version\]

</td><td>

 

</td></tr><tr><td>

Auto business rule for Assessments

</td><td>

Business Application \[cmdb\_ci\_business\_app\]

</td><td>

 

</td></tr><tr><td>

Auto business rule for Assessments

</td><td>

Business Application \[cmdb\_ci\_business\_app\]

</td><td>

 

</td></tr><tr><td>

Auto deletion rule for Assessments

</td><td>

Business Application \[cmdb\_ci\_business\_app\]

</td><td>

 

</td></tr><tr><td>

Avoid duplicate name for TRM Categories

</td><td>

TRM Category \[sn\_apm\_trm\_standards\_category\]

</td><td>

 

</td></tr><tr><td>

Check Duplicate Product

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Check Duplicate Product Lifecycle

</td><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle\]

</td><td>

 

</td></tr><tr><td>

Check Duplicate Product Lifecycle HW

</td><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle\]

</td><td>

 

</td></tr><tr><td>

Check Duplicate Product Lifecycle Req

</td><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

 

</td></tr><tr><td>

Check Duplicate Product Lifecycle Req HW

</td><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

 

</td></tr><tr><td>

Check Duplicate Product Request

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Check Duplicate TRM Phase

</td><td>

TRM Phase \[sn\_apm\_trm\_standards\_phase\]

</td><td>

 

</td></tr><tr><td>

Date Validations

</td><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

 

</td></tr><tr><td>

Display successful message with link

</td><td>

TRM Product Lifecycle Request \[sn\_apm\_trm\_product\_lifecycle\_request\]

</td><td>

 

</td></tr><tr><td>

Display successful message with link

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Populate Name HW

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Populate Name HW

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Populate scratchpad for TRM Prod Request

</td><td>

TRM Product Request \[sn\_apm\_trm\_product\_request\]

</td><td>

 

</td></tr><tr><td>

Populate scratchpad for TRM Product

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Restrict emptying category

</td><td>

TRM Product \[sn\_apm\_trm\_standards\_product\]

</td><td>

 

</td></tr><tr><td>

Update product lifecycle exist flag

</td><td>

TRM Product Lifecycle \[sn\_apm\_trm\_standards\_product\_lifecycle\]

</td><td>

 

</td></tr><tr><td>

Validate Parent Category Hierarchy

</td><td>

TRM Category \[sn\_apm\_trm\_standards\_category\]

</td><td>

 

</td></tr><tr><td>

TPM Audit on TPM Lifecycle Exception

</td><td>

TPM Technology Lifecycle Exception \[sn\_apm\_tpm\_technology\_lifecycle\_exception\]

</td><td>

Fetches the life cycles that were approximated or couldn't be found from Software Asset Management \(SAM\) Professional or Hardware Asset Management \(HAM\) Professional.

</td></tr><tr><td>

Populate TPM Technology Lifecycle table

</td><td>

TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\]

</td><td>

Fetches the technology life-cycle data for your hardware and software elements in your enterprise.

</td></tr><tr><td>

Update Technology Lifecycle Info

</td><td>

TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\]

</td><td>

Updates technology life-cycle data for your hardware and software elements.

</td></tr><tr><td>

Active From/Until Date Validation

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Avoid DI subscribers with duplicate name

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Avoid DI with duplicate name

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Avoid duplicate dis submit request

</td><td>

Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]

</td><td>

 

</td></tr><tr><td>

Avoid duplicate retire request

</td><td>

Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]

</td><td>

 

</td></tr><tr><td>

Avoid invalid Subscriber BA

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Avoid making a circular relationship

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Avoid Same Subscriber and Provider BA

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Avoid Same Subscriber and Provider BA

</td><td>

Digital Integration Request \[sn\_apm\_di\_digital\_integration\_request\]

</td><td>

 

</td></tr><tr><td>

Avoid update of some fields

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Avoid update of some fields

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Bidirectional Data Flow - clear field

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Check Provider references

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Check Subscribers

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Create Relationship Record

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Create Relationship Record

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Delete Relationship Record

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Delete Relationship Record

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Restrict update of invalid Subscrber ifa

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Set BA in Digital Interface Record

</td><td>

Digital Integration \[sn\_apm\_di\_digital\_integration\]

</td><td>

 

</td></tr><tr><td>

Stop delete if linked to digital integra

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Validate Provider BA

</td><td>

Digital Interface \[sn\_apm\_di\_digital\_interface\]

</td><td>

 

</td></tr><tr><td>

Verify Duplicate API to DIG INTF-insert

</td><td>

Digital Interface to API \[sn\_apm\_di\_dintf\_api\]

</td><td>

 

</td></tr><tr><td>

Verify Duplicate API to DIG INTF-update

</td><td>

Digital Interface to API \[sn\_apm\_di\_dintf\_api\]

</td><td>

 

</td></tr><tr><td>

Verify Duplicate Information Object

</td><td>

Digital Integration Information Object \[sn\_apm\_di\_information\_objects\]

</td><td>

 

</td></tr><tr><td>

Verify Duplicate Information Object

</td><td>

Digital Interface Information Object \[sn\_apm\_di\_dintf\_information\_object\]

</td><td>

 

</td></tr><tr><td>

Verify Duplicate SDLC Component

</td><td>

Digital Interface SDLC Component \[sn\_apm\_di\_dintf\_sdlc\_component\]

</td><td>

 

</td></tr><tr><td>

Avoid duplicate entity configurations

</td><td>

Entity Configuration \[sn\_apm\_mdtl\_com\_entity\_configuration\]

</td><td>

 

</td></tr><tr><td>

Deleting entity value records

</td><td>

Architectural Artifact Version \[sn\_apm\_architectural\_version\]

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Install Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/install-ea-workspace.md)

**Related topics**  


[Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-access-roles.md)

[Install Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/install-ea-workspace.md)

