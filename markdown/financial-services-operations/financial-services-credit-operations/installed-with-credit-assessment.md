---
title: Components installed with Financial Services Credit Operations
description: Several types of components are installed with the installation of the Financial Services Credit Operations application, including tables and user roles.
locale: en-US
release: australia
product: Financial Services Credit Operations
classification: financial-services-credit-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Credit Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Credit Operations

Several types of components are installed with the installation of the Financial Services Credit Operations application, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

This application is automatically installed when you install any of the following Financial Services Operations applications. Financial Services Credit Operations manages the Credit tasks that are used in workflows across Financial Services Operations applications.

-   Financial Services Card Operations
-   Financial Services Business Loan Operations
-   Financial Services Personal Loan Operations

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Credit admin\[sn\_bom\_credit\_asmt.admin\]

</td><td>

Application-specific system administrator role that can grant access to all credit data.Users with this role have read, write, and create access to the Financial Services Credit Operations tables.

</td><td>

-   sn\_bom.service\_definition\_admin
-   sn\_bom\_credit\_asmt.b2b\_agent
-   sn\_bom\_credit\_asmt.b2c\_agent

</td></tr><tr><td>

Credit agent – Business\[sn\_bom\_credit\_asmt.b2b\_agent\]

</td><td>

-   View the overall status of credit tasks for business services
-   Work on credit tasks

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.account\_data\_viewer
-   sn\_bom\_loan\_b2b.viewer
-   sn\_bom.b2b\_agent
-   sn\_esm\_agent

</td></tr><tr><td>

Credit contributor – Business \[sn\_bom\_credit\_asmt.b2b\_contributor\]

</td><td>

-   Submit credit service requests
-   View the status of credit assessment cases and tasks
-   Work on credit case for accounts managed by them till the Initiate stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom\_clo\_b2b.contact\_lifecycle\_viewer
-   sn\_bom\_kyc.b2b\_account\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_clo\_b2b.account\_lifecycle\_viewer
-   sn\_bom\_kyc.b2b\_contact\_viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom\_loan\_b2b.viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor
-   sn\_bom.deposit\_account\_viewer

</td></tr><tr><td>

Credit contributor – Personal \[sn\_bom\_credit\_asmt.b2c\_contributor\]

</td><td>

-   Submit credit service requests
-   View the status of credit assessment cases and tasks
-   Work on credit case for consumer accounts managed by them till the Initiate stage

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom\_loan.b2c\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_kyc.b2c\_customer\_viewer
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.b2c\_contributor
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.deposit\_account\_viewer

</td></tr><tr><td>

Credit agent connector – Business \[sn\_bom\_credit\_asmt.b2b\_agent\_connector\]

</td><td>

-   Submit credit service requests
-   Work on credit cases and tasks to fulfil requests for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom\_clo\_b2b.contact\_lifecycle\_viewer
-   sn\_bom\_kyc.b2b\_account\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_clo\_b2b.account\_lifecycle\_viewer
-   sn\_bom\_kyc.b2b\_contact\_viewer
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom\_loan\_b2b.viewer
-   sn\_bom.agent
-   sn\_bom.deposit\_account\_viewer

</td></tr><tr><td>

Credit agent connector – Personal \[sn\_bom\_credit\_asmt.b2c\_agent\_connector\]

</td><td>

-   Submit credit service requests
-   Work on credit cases and tasks to fulfil requests for consumer accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom\_loan.b2c\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom\_kyc.b2c\_customer\_viewer
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.viewer
-   sn\_bom.agent
-   sn\_bom.deposit\_account\_viewer

</td></tr><tr><td>

Credit viewer – Business\[sn\_bom\_credit\_asmt.b2b\_viewer\]

</td><td>

View credit tasks and related data for business services

</td><td>

None

</td></tr><tr><td>

Credit agent – Personal\[sn\_bom\_credit\_asmt.b2c\_agent\]

</td><td>

-   View the overall status of credit tasks for consumer services
-   Work on credit tasks

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom\_loan.b2c\_viewer
-   sn\_bom.service\_definition\_read
-   sn\_bom.customer\_data\_viewer
-   sn\_bom.b2c\_agent
-   sn\_esm\_agent

</td></tr><tr><td>

Credit viewer – Personal \[sn\_bom\_credit\_asmt.b2c\_viewer\]

</td><td>

View credit tasks and related data for consumer services

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Credit Base\[sn\_bom\_credit\_asmt\_base\]

</td><td>

Credit Service Case tables extend the Credit Base table. Credit Base table extends the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Credit Service Case\[sn\_bom\_credit\_asmt\_b2b\_service\]

</td><td>

Stores all credit cases for all Financial Services Operations applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Credit Service Case\[sn\_bom\_credit\_asmt\_loan\_b2b\_service\]

</td><td>

Stores all credit service cases for business loan services for the Financial Services Business Loan Operations application. This table extends the Credit Base \[sn\_bom\_credit\_asmt\_base\] table.

</td></tr><tr><td>

Credit Service Case\[sn\_bom\_credit\_asmt\_service\]

</td><td>

Stores all credit service cases for consumer services for all Financial Services Operations applications. This table extends the Credit Base \[sn\_bom\_credit\_asmt\_base\] table.

</td></tr><tr><td>

Credit Service Case\[sn\_bom\_credit\_asmt\_loan\_service\]

</td><td>

Stores all credit service cases for personal loan services for the Financial Services Business Loan Operations application. This table extends the Credit Base \[sn\_bom\_credit\_asmt\_base\] table.

</td></tr><tr><td>

Credit Task\[sn\_bom\_credit\_asmt\_b2b\_task\]

</td><td>

Stores all credit tasks for business services for all Financial Services Operations applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr><tr><td>

Credit Task\[sn\_bom\_credit\_asmt\_task\]

</td><td>

Stores all credit tasks for personal services for all Financial Services Operations applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>