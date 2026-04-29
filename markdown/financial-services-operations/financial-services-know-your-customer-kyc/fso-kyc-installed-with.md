---
title: Components installed with Financial Services Know Your Customer
description: Several types of components are installed with activation of the Financial Services Know Your Customer \(com.sn\_bom\_kyc\) plugin, including tables and user roles.
locale: en-US
release: australia
product: Financial Services Know Your Customer \(KYC\)
classification: financial-services-know-your-customer-kyc
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Know Your Customer, Common applications, Financial Services Operations \(FSO\)]
---

# Components installed with Financial Services Know Your Customer

Several types of components are installed with activation of the Financial Services Know Your Customer \(com.sn\_bom\_kyc\) plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

This application is automatically installed when you install any of the following Financial Services Operations \(KYC\) applications. Financial Services Know Your Customer manages the KYC tasks that are used in workflows across Financial Services Operations applications.

-   Financial Services Business Loan Operations
-   Financial Services Personal Loan Operations
-   Financial Services Client Lifecycle
-   Financial Services Business Lifecycle

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

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
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

KYC Account Task\[sn\_bom\_kyc\_account\_task\]

</td><td>

Stores Financial Services Know Your Customer account tasks pending completion. This table extends the \[Financial Task\] table.

</td></tr><tr><td>

KYC Contact Task\[sn\_bom\_kyc\_contact\_task\]

</td><td>

Stores Financial Services Know Your Customer contact tasks pending completion. This table extends the \[Financial Task\] table.

</td></tr><tr><td>

KYC Customer Task\[sn\_bom\_kyc\_customer\_task\]

</td><td>

Stores Financial Services Know Your Customer customer tasks pending completion. This table extends the \[Financial Task\] table.

</td></tr></tbody>
</table>