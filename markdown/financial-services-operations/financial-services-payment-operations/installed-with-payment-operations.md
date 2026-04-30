---
title: Components installed with Financial Services Payment Operations
description: Several types of components are installed with the installation of the Financial Services Payment Operations application, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.
locale: en-US
release: xanadu
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Financial Services Payment Operations reference, Financial Services Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Payment Operations

Several types of components are installed with the installation of the Financial Services Payment Operations application, including tables and user roles. The application also installs related plugins and store applications if they are not already installed.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

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
|Financial Services Operations Core|Stores the customer data that is needed to make payment requests. For more information, see .|

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Payment admin \[sn\_bom\_payment.admin\]

</td><td>

Application-specific system administrator role that can:-   Grant payment operations roles
-   Delete payment cases and tasks

 **Note:** The sn\_bom.admin role contains the sn\_bom\_payment.admin role when the Financial Services Payment Operations application is installed.

</td><td>

-   sn\_bom\_payment.inquiry\_agent
-   sn\_bom\_payment.inquiry\_viewer
-   sn\_bom\_payment.claim\_agent
-   sn\_bom\_payment.claim\_viewer

</td></tr><tr><td>

Claim agent\[sn\_bom\_payment.claim\_agent\]

</td><td>

-   View the overall status of claim cases
-   Create claim cases
-   Work on claim cases, debit approvals, and claim tasks
-   Record interactions

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom\_payment.inquiry\_viewer
-   sn\_esm\_agent
-   sn\_bom\_payment.claim\_viewer

</td></tr><tr><td>

Payment contributor\[sn\_bom\_payment.contributor\]

</td><td>

-   Submit payment inquiry requests
-   Submit payment claim requests for internal claims
-   View the status of payment inquiry and claim cases

 **Important:** For the contributor role to work, it must be combined with one of the CSM Contributor users roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_sla\_definition\_read
-   sn\_bom.b2c\_contributor
-   sn\_bom.account\_data\_viewer
-   sn\_bom\_payment.inquiry\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_bom.b2b\_contributor
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_payment.claim\_viewer

</td></tr><tr><td>

Claim agent connector\[sn\_bom\_payment.claim\_agent\_connector\]

</td><td>

-   Create claim cases
-   Work on claim cases, debit approvals, and claim tasks for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.agent
-   sn\_bom\_payment.inquiry\_viewer
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_payment.claim\_viewer

</td></tr><tr><td>

Inquiry agent connector\[sn\_bom\_payment.inquiry\_agent\_connector\]

</td><td>

-   Create inquiry cases
-   Work on payment inquiry cases and inquiry tasks for accounts managed by them

 **Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

</td><td>

-   sn\_bom.ref\_data\_viewer
-   sn\_sla\_definition\_read
-   sn\_bom.viewer
-   sn\_bom.account\_data\_viewer
-   sn\_bom.agent
-   sn\_bom\_payment.inquiry\_viewer
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom\_payment.claim\_viewer

</td></tr><tr><td>

Claim viewer\[sn\_bom\_payment.claim\_viewer\]

</td><td>

View claim cases and related data

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Inquiry agent\[sn\_bom\_payment.inquiry\_agent\]

</td><td>

-   View the overall status of payment inquiry cases
-   Work on payment inquiry cases and inquiry tasks
-   Record interactions

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom\_payment.inquiry\_viewer
-   sn\_esm\_agent
-   sn\_bom\_payment.claim\_viewer

</td></tr><tr><td>

Inquiry viewer\[sn\_bom\_payment.inquiry\_viewer\]

</td><td>

View inquiry cases and related data

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom.ref\_data\_viewer
-   sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Payment manager\[sn\_bom\_payment.manager\]

</td><td>

-   View the Payment Operations dashboard
-   Use Process Mining for Payment Operations processes

</td><td>

-   sn\_bom\_payment.inquiry\_agent
-   pa\_viewer
-   sn\_bom\_payment.claim\_agent

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Payment Base\[sn\_bom\_payment\_base\]

</td><td>

Claim, Payment Inquiry Case, and Payment Service tables extend the Payment Base table.

</td></tr><tr><td>

Claim\[sn\_bom\_payment\_claim\]

</td><td>

Stores all payment claim cases.

</td></tr><tr><td>

Claim Task\[sn\_bom\_payment\_claim\_task\]

</td><td>

Stores all claims tasks.

</td></tr><tr><td>

Debit Instruction\[sn\_bom\_payment\_debit\_instruction\]

</td><td>

Stores all debit instructions for all refunds.

</td></tr><tr><td>

Payment Inquiry Case\[sn\_bom\_payment\_inquiry\]

</td><td>

Stores all payment inquiry cases.

</td></tr><tr><td>

Inquiry Task\[sn\_bom\_payment\_inquiry\_task\]

</td><td>

Stores all payment inquiry tasks.

</td></tr><tr><td>

Receiving Transaction\[sn\_bom\_payment\_m2m\_receiving\_transaction\]

</td><td>

Stores all financial transactions that the receiving customers and accounts received.

</td></tr><tr><td>

Sender Transaction\[sn\_bom\_payment\_m2m\_sender\_transaction\]

</td><td>

Stores all financial transactions \(deposit\) that sender customers sent.

</td></tr><tr><td>

Payment Service\[sn\_bom\_payment\_service\]

</td><td>

Stores all payment service cases for debit approvals.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Payment Operations reference](../concept/payment-operations-reference.md)

