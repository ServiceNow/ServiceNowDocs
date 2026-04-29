---
title: Components installed with Financial Services Card Operations
description: Several types of components are installed with the installation of the Financial Services Card Operations application, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.
locale: en-US
release: australia
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Card Operations

Several types of components are installed with the installation of the Financial Services Card Operations application, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this application.

## Plugins installed

<table id="table_qdc_ksw_llb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service\[com.sn\_customerservice\]

</td><td>

Enables the extension of tables from the Customer Service Management application into the Financial Services Operations applications.

</td></tr></tbody>
</table>## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the customer data that is needed to make credit card requests. For more information, see [Financial Services Operations Core](../../fso-common/reference/financial-services-operations-core-data-model.md).|
|Financial Services Credit Operations|Enables management of Credit Risk Assessment tasks that are used in the card operations workflows. For more information, see [Components installed with Financial Services Credit Operations](../../fso-common/reference/installed-with-credit-assessment.md).|
|Guided Decisions Experience|Allows customers to use Guided Decisions with Playbooks, Recommended Actions, and other features. For more information, see [Configuring Guided Decisions](https://www.servicenow.com/docs/access?context=setting-up-guided-decisions&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)|
|Document Processor|Enables management of document services tasks that are used in card operations workflows. For more information, see [Integrating with Document Processor](../../fso-common/concept/integrating-with-document-processor.md).|

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Credit card admin\[sn\_bom\_credit\_card.admin\]

</td><td>

Application-specific system administrator role that can:-   Grant card operations roles
-   Delete credit card cases and tasks
-   Has read, write, and create access to credit card data.

 **Note:** The sn\_bom.admin role contains the sn\_bom\_credit\_card.admin role when the Financial Services Card Operations application is installed.

</td><td>

sn\_bom\_credit\_card.agent

</td></tr><tr><td>

Credit card agent\[sn\_bom\_credit\_card.agent\]

</td><td>

-   View the overall status of credit card cases
-   Work on credit card cases and tasks

</td><td>

-   sn\_ind.write
-   sn\_bom\_credit\_asmt.viewer
-   sn\_bom\_credit\_card\_account.viewer
-   sn\_bom\_document.viewer
-   sn\_esm\_agent

</td></tr><tr><td>

Credit card contributor\[sn\_bom\_credit\_card.contributor\]

</td><td>

-   Submit credit card requests
-   View the status of credit card cases, credit assessment tasks, and document services tasks
-   Work on credit card case and collect inbound documents for accounts managed by them till the New stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_sla\_definition\_read
-   sn\_bom.b2c\_contributor
-   sn\_bom\_credit\_asmt.b2c\_viewer
-   sn\_bom\_credit\_card\_account.viewer
-   sn\_bom\_document.b2c\_viewer
-   sn\_customerservice.csm\_workspace\_user

</td></tr><tr><td>

Credit card agent connector\[sn\_bom\_credit\_card.agent\_connector\]

</td><td>

-   Submit credit card requests
-   Work on credit card and tasks to fulfil card requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_sla\_definition\_read
-   sn\_bom\_credit\_asmt.b2c\_viewer
-   sn\_bom.viewer
-   sn\_bom\_credit\_card\_account.viewer
-   sn\_bom.agent
-   sn\_bom\_document.b2c\_viewer
-   sn\_customerservice.csm\_workspace\_user

</td></tr><tr><td>

Credit card viewer\[sn\_bom\_credit\_card.viewer\]

</td><td>

View credit card cases and related data

</td><td>

-   sn\_ind.write
-   sn\_customerservice.case\_viewer
-   sn\_bom.credit\_card\_account\_viewer

</td></tr><tr><td>

Credit card account viewer\[sn\_bom.credit\_card\_account\_viewer\]

</td><td>

View credit card data entities.

</td><td>

 

</td></tr><tr><td>

Card dispute manager \[sn\_bom\_credit\_card.dispute\_manager\]

</td><td>

-   Manage dispute functions
-   View the Performance Analytics reports in the dashboard
-   Use Process Mining projects for dispute management processes

</td><td>

sn\_bom\_credit\_card.dispute\_agent

</td></tr><tr><td>

Card dispute agent

\[sn\_bom\_credit\_card.dispute\_agent\]

</td><td>

-   View status of dispute cases
-   Work on dispute cases and tasks

</td><td>

-   sn\_bom.customer\_data\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

Card dispute agent connector

\[sn\_bom\_credit\_card.dispute\_agent\_connector\]

</td><td>

-   Submit dispute requests
-   Work on dispute tasks to resolve requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_sla\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr><tr><td>

Card dispute viewer\[sn\_bom\_credit\_card.dispute\_viewer\]

</td><td>

View dispute cases and related data

</td><td>

-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2b\_credit\_card\_account\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Card Base\[sn\_bom\_card\_base\]

</td><td>

Credit Card Service table extends the Card Base table. Card Base table extends the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Credit Card Service\[sn\_bom\_credit\_card\_service\]

</td><td>

Stores all credit card service cases. This table extends the Card Base \[sn\_bom\_card\_base\] table.

</td></tr><tr><td>

Credit Card Task\[sn\_bom\_credit\_card\_task\]

</td><td>

Stores all credit card tasks. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Dispute Service

\[sn\_bom\_credit\_card\_disputes\_service\]

</td><td>

Stores all dispute service cases. This table extends the Card Base \[sn\_bom\_card\_base\] table.

</td></tr><tr><td>

Dispute Task

\[sn\_bom\_credit\_card\_disputes\_task\]

</td><td>

Stores all dispute tasks. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Dispute Transaction

\[sn\_bom\_credit\_card\_disputes\_transaction\]

</td><td>

Stores all dispute transactions.

</td></tr><tr><td>

Visa Dispute Intake

 \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\]

</td><td>

Stores all Visa Dispute Questionnaire questions and responses. Extends the Intake Form \[sn\_evnt\_inq\_qtn\] table.

</td></tr><tr><td>

Visa Dispute Cardholder Intake

 \[sn\_bom\_visa\_cp\_visa\_dispute\_cardholder\_intake\]

</td><td>

Stores Visa Dispute Questionnaire questions and responses submitted by consumers, such as a dispute playbook on a service portal. See [Create a dispute case with Dispute Intake in Portal](../concept/creating-an-onboarding-case-with-dispute-playbook-for-portal.md) for more information. Extends the Visa Dispute Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Card Operations reference](../concept/card-operations-reference.md)

**Related topics**  


[Overview of the Dispute Management workflow](../concept/dispute-management-workflows.md)

