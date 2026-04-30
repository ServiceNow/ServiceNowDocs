---
title: Components installed with Financial Services Client Lifecycle
description: Several types of components are installed with the activation of the Financial Services Client Lifecycle \(sn\_bom\_clo\_b2c\) plugin, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.
locale: en-US
release: xanadu
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Financial Services Customer Lifecycle Operations reference, Financial Services Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Client Lifecycle

Several types of components are installed with the activation of the Financial Services Client Lifecycle \(sn\_bom\_clo\_b2c\) plugin, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Plugins installed

<table id="table_qdc_ksw_llb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service\(com.sn\_customerservice\)

</td><td>

Enables the extension of tables from the Customer Service Management application into the Financial Services Operations applications.

</td></tr></tbody>
</table>## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Account Administrator\[sn\_bom\_clo\_b2c.admin\]

</td><td>

This role gives access to all Client Lifecycle data and admin privileges.-   Create users
-   Grant roles and assign users to groups
-   Configure the CLO application
-   Add, modify, and delete field options

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_clo\_b2c.agent

</td></tr><tr><td>

Account Manager\[sn\_bom\_clo\_b2c.manager\]

</td><td>

This role provides all Client Lifecycle Agent capabilities, along with Performance Analytics reports and performance optimization projects.

</td><td>

-   sn\_bom\_clo\_b2c.agent
-   pa\_viewer

</td></tr><tr><td>

CLO contributor\[sn\_bom\_clo\_b2c.contributor\]

</td><td>

-   Create CLO service cases and enter case data
-   View the overall status of cases
-   Work on CLO service cases and tasks until the Initiate and Review stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_sla\_definition\_read
-   sn\_bom\_kyc.b2c\_customer\_viewer
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.b2c\_contributor
-   sn\_bom\_document.b2c\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom\_document.b2c\_collector

</td></tr><tr><td>

CLO agent connector\[sn\_bom\_clo\_b2c.agent\_connector\]

</td><td>

-   Create CLO service cases and enter case data
-   View the overall status of cases
-   Work on CLO service cases and tasks to fulfill requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.account\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_kyc.b2c\_customer\_viewer
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.agent
-   sn\_bom\_document.b2c\_viewer
-   sn\_bom\_document.b2c\_collector

</td></tr><tr><td>

Client Lifecycle Agent\[sn\_bom\_clo\_b2c.agent\]

</td><td>

This role gives access to all Client Lifecycle data.-   Create cases and enter case data
-   Assign tasks to self or other agents
-   Enter and update applicant information
-   Perform various verification tasks
-   Approve accounts
-   Close cases

</td><td>

-   sn\_bom\_kyc.b2c\_customer\_viewer
-   sn\_bom\_document.b2c\_viewer
-   sn\_bom.b2c\_agent
-   sn\_bom\_document.b2c\_collector

</td></tr><tr><td>

Client Lifecycle Viewer\[sn\_bom\_clo\_b2c.viewer\]

</td><td>

This role gives read-only access to all Financial Services Client Lifecycle data.

</td><td>

sn\_bom.service\_definition\_read

</td></tr><tr><td>

KYC Admin\[sn\_bom\_kyc.admin\]

</td><td>

This role gives access to all Financial Services Know Your Customer operations data and grants admin privileges.

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_kyc.b2c\_customer\_agent
-   sn\_bom\_kyc.b2c\_account\_agent
-   sn\_bom\_kyc.b2c\_contact\_agent

</td></tr><tr><td>

KYC Customer Agent\[sn\_bom\_kyc.b2c\_customer\_agent\]

</td><td>

This role gives access to all Financial Services Know Your Customer client-level contact data.

</td><td>

-   sn\_bom\_clo\_b2c.viewer
-   sn\_bom\_credit\_asmt.b2c\_viewer
-   sn\_bom\_document.b2c\_viewer
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

KYC Contact Viewer\[sn\_bom\_kyc.b2c\_customer\_viewer\]

</td><td>

This role grants read-only views of account contact information.

</td><td>

sn\_bom.service\_definition\_read

</td></tr></tbody>
</table>## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the data that is needed to create customer lifecycle cases. For more information, see .|
|Financial Services Credit Operations|Enables the management of Credit service cases and tasks that are used in Financial Services Customer Lifecycle Operations workflows. For more information, see [Components installed with Financial Services Credit Operations](../../fso-common/reference/installed-with-credit-assessment.md).|
|Financial Services Document Management|Enables the management of Document Services tasks that are used in Financial Services Customer Lifecycle Operations workflows. For more information, see .|
|Financial Services Know Your Customer \(KYC\)|Enables KYC Agents to review and evaluate the eligibility of new account applicants.|
|CSM Playbook|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations.|
|CSM Contributor User|Enables middle office teams to engage in resolving customer issues and requests.|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Lifecycle Base\[sn\_bom\_clo\_b2c\_base\]

</td><td>

Customer Lifecycle Base table extends the Financial Services Base \[sn\_bom\_case\] table.

</td></tr><tr><td>

Account Lifecycle Service Case\[sn\_bom\_clo\_b2c\_service\]

</td><td>

Account Lifecycle Service Case extends the Customer Lifecycle Base \[sn\_bom\_clo\_b2c\_base\] table.

</td></tr><tr><td>

Account Lifecycle Task\[sn\_bom\_clo\_b2c\_task\]

</td><td>

Account Lifecycle Task Case extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>