---
title: Components installed with Financial Services Business Lifecycle
description: Several types of components are installed with the activation of the Financial Services Business Lifecycle \(sn\_bom\_clo\_b2b\) plugin, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.
locale: en-US
release: xanadu
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Financial Services Customer Lifecycle Operations reference, Financial Services Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Business Lifecycle

Several types of components are installed with the activation of the Financial Services Business Lifecycle \(sn\_bom\_clo\_b2b\) plugin, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.

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

Account Administrator\[sn\_bom\_clo\_b2b.admin\]

</td><td>

In addition to admin privileges, this role gives access to all Financial Services Business Lifecycle operations data.-   Create users
-   Grant roles and assign users to groups
-   Configure the CLO application
-   Add, modify, and delete field options

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_clo\_b2b.account\_lifecycle\_agent

</td></tr><tr><td>

Account Manager\[sn\_bom\_clo\_b2b.manager\]

</td><td>

This role provides all Financial Services Business Lifecycle Agent capabilities, along with Performance Analytics reports and performance optimization projects.

</td><td>

-   pa\_viewer
-   sn\_bom\_clo\_b2b.account\_lifecycle\_agent

</td></tr><tr><td>

CLO contributor\[sn\_bom\_clo\_b2b.contributor\]

</td><td>

-   Create CLO service cases and enter case data
-   View the overall status of cases
-   Work on CLO service cases and tasks until the Initiate and review stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom\_kyc.b2b\_account\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom\_kyc.b2b\_contact\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

CLO agent connector\[sn\_bom\_clo\_b2b.agent\_connector\]

</td><td>

-   Create CLO service cases and enter case data
-   View the overall status of cases
-   Work on CLO service cases and tasks to fulfill requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom\_kyc.b2b\_account\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_clo\_b2b.account\_lifecycle\_viewer
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom\_kyc.b2b\_contact\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.agent
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Account Lifecycle Agent\[sn\_bom\_clo\_b2b.account\_lifecycle\_agent\]

</td><td>

This role gives access to all Financial Services Business Lifecycle data.-   Create cases and enter case data
-   Assign tasks to self or other agents
-   Enter and update applicant information
-   Perform various verification tasks
-   Approve accounts
-   Close cases

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom\_kyc.b2b\_account\_viewer
-   sn\_bom\_clo\_b2b.contact\_lifecycle\_agent
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom\_kyc.b2b\_contact\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Contact Lifecycle Agent\[sn\_bom\_clo\_b2b.contact\_lifecycle\_agent\]

</td><td>

This role gives access to Contact Lifecycle operation data.-   Create contact cases and enter data
-   Assign tasks to self or other agents
-   Enter and update contact information
-   Perform various verification tasks
-   Close contact cases

</td><td>

-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom\_kyc.b2b\_account\_viewer
-   sn\_bom\_clo\_b2b.account\_lifecycle\_viewer
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom\_kyc.b2b\_contact\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom\_document.b2b\_collector

</td></tr><tr><td>

Account Lifecycle Viewer\[sn\_bom\_clo\_b2b.account\_lifecycle\_viewer\]

</td><td>

This role gives read-only access to all Account Lifecycle operations data.

</td><td>

-   sn\_bom\_clo\_b2b.contact\_lifecycle\_viewer
-   sn\_bom.service\_definition\_read

</td></tr><tr><td>

Contact Lifecycle Viewer\[sn\_bom\_clo\_b2b.contact\_livecycle\_viewer\]

</td><td>

This role gives read-only access to all Financial Services Business Lifecycle data.

</td><td>

sn\_bom.service\_definition\_read

</td></tr><tr><td>

Know Your Customer Admin\[sn\_bom\_kyc.admin\]

</td><td>

This role gives access to all KYC operations data and grants admin privileges.

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_kyc.b2c\_customer\_agent
-   sn\_bom\_kyc.b2b\_account\_agent
-   sn\_bom\_kyc.b2b\_contact\_agent

</td></tr><tr><td>

Know Your Customer Contact Agent\[sn\_bom\_kyc.b2b\_contact\_agent\]

</td><td>

This role gives access to all Business KYC operations contact data.

</td><td>

-   sn\_bom\_clo\_b2b.contact\_lifecycle\_viewer
-   sn\_bom\_clo\_b2b.account\_lifecycle\_viewer
-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom\_kyc.b2b\_account\_viewer
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.b2b\_agent

</td></tr><tr><td>

KYC Account Agent\[sn\_bom\_kyc.b2b\_account\_agent\]

</td><td>

This role gives access to all Financial Services Know Your Customer business-level operations, account, and contact data.

</td><td>

-   sn\_bom\_credit\_asmt.b2b\_viewer
-   sn\_bom\_clo\_b2b.account\_lifecycle\_viewer
-   sn\_bom\_document.b2b\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom\_kyc.b2b\_contact\_agent

</td></tr><tr><td>

KYC Contact Viewer\[sn\_bom\_kyc.b2b\_contact\_viewer\]

</td><td>

This role grants read-only views of Financial Services Know Your Customer account contact information.

</td><td>

sn\_bom.service\_definition\_read

</td></tr><tr><td>

KYC Account Viewer\[sn\_bom\_kyc.b2b\_account\_viewer\]

</td><td>

This role grants read-only views of Financial Services Know Your Customer account information.

</td><td>

-   sn\_bom.service\_definition\_read
-   sn\_bom\_kyc.b2b\_contact viewer

</td></tr></tbody>
</table>## Store applications installed

|Store application|Description|
|-----------------|-----------|
|Financial Services Operations Core|Stores the data that is needed to create Customer Lifecycle Operations cases. For more information, see .|
|Financial Services Credit Operations|Enables the management of Credit service cases and tasks that are used in Customer Lifecycle Operations workflows. For more information, see [Components installed with Financial Services Credit Operations](../../fso-common/reference/installed-with-credit-assessment.md).|
|Financial Services Document Management|Enables the management of Document Services tasks that are used in Customer Lifecycle Operations workflows. For more information, see .|
|Financial Services Know Your Customer \(KYC\)|Enables KYC Agents to review and evaluate the eligibility of new account applicants.|
|CSM Playbook|Provides a way to visualize business process workflows in a simple, task-oriented view, ensuring consistent responses to commonly encountered situations.|
|CSM Contributor User|Enables middle office teams to engage in resolving customer issues and requests.|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Lifecycle Base\[sn\_bom\_clo\_b2b\_base\]

</td><td>

Customer Lifecycle Base table extends the Financial Services Base \[sn\_bom\_case\] table.

</td></tr><tr><td>

Account Lifecycle Service Case\[sn\_bom\_clo\_b2b\_account\_service\]

</td><td>

Account Lifecycle Service Case extends the Customer Lifecycle Base \[sn\_bom\_clo\_b2b\_base\] table.

</td></tr><tr><td>

Account Lifecycle Task\[sn\_bom\_clo\_b2b\_account\_task\]

</td><td>

Account Lifecycle Task Case extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Contact Lifecycle Service Case\[sn\_bom\_clo\_b2b\_contact\_service\]

</td><td>

Contact Lifecycle Service Case extends the Customer Lifecycle Base \[sn\_bom\_clo\_b2b\_base\] table.

</td></tr><tr><td>

Contact Lifecycle Task\[sn\_bom\_clo\_b2b\_contact\_task\]

</td><td>

Contact Lifecycle Task extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>