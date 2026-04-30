---
title: User roles and FSO Business rules
description: This section defines the various roles within Financial Services Operations Core and explains the business rules that guide the system’s actions.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [User management, Explore, Financial Services Operations \(FSO\)]
---

# User roles and FSO Business rules

This section defines the various roles within Financial Services Operations Core and explains the business rules that guide the system’s actions.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

FSO admin\[sn\_bom.admin\]

</td><td>

Application-specific system administrator role for the Financial Services Operations \(FSO\) applications. Users with this role have read, write, and create access to the FSO tables.

</td><td>

-   sn\_bom.document.admin
-   sn\_bom\_credit\_asmt.admin
-   model\_manager

</td></tr><tr><td>

Financial services consumer contributor

\[sn\_bom.consumer\_contributor\]

</td><td>

Universal role in the FSO Core application for financial services relationship contributor that enables users to create cases for any consumer. This role inherits all other b2c contributor roles in Financial Services Operations applications and the Customer service consumer contributor role.

</td><td>

-   sn\_bom.contributor
-   sn\_bom\_payment.contributor
-   sn\_bom\_credit\_asmt.b2c\_contributor
-   sn\_ins\_indiv\_life.contributor
-   sn\_ins\_policy\_b2c.contributor
-   sn\_customerservice.consumer\_contributor
-   sn\_bom\_deposit\_b2c.contributor
-   sn\_bom\_loan.contributor
-   sn\_bom\_compl.contributor
-   sn\_bom\_clo\_b2c.contributor
-   sn\_ins\_group\_life.contributor
-   sn\_bom\_credit\_card.contributor

</td></tr><tr><td>

Financial services account contributor

\[sn\_bom.account\_contributor\]

</td><td>

Universal role in the FSO Core application for financial services relationship contributor that enables users to create cases for any account. This role inherits all other b2b contributor roles in Financial Services Operations applications and the Customer service account contributor role.

</td><td>

-   sn\_bom.contributor
-   sn\_bom\_payment.contributor
-   sn\_bom\_treasury.contributor
-   sn\_ins\_indiv\_life.contributor
-   sn\_bom\_deposit\_b2b.contributor
-   sn\_ins\_policy\_b2b.contributor
-   sn\_bom\_credit\_asmt.b2b\_contributor
-   sn\_bom\_loan\_b2b.contributor
-   sn\_bom\_compl.contributor
-   sn\_ins\_group\_life.contributor
-   sn\_customerservice.account\_contributor
-   sn\_bom\_clo\_b2b.contributor
-   sn\_bom\_credit\_card.contributor

</td></tr><tr><td>

Financial services relationship contributor\[sn\_bom.relationship\_contributor\]

</td><td>

Universal role in the FSO Core application for financial services relationship contributor that enables users to create cases for customers or accounts with whom they have established relationships. This role inherits all other contributor roles in Financial Services Operations applications and the Customer service relationship contributor role.

</td><td>

-   sn\_bom.contributor
-   sn\_bom\_payment.contributor
-   sn\_bom\_treasury.contributor
-   sn\_customerservice.relationship\_contributor
-   sn\_bom\_credit\_asmt.b2c\_contributor
-   sn\_ins\_indiv\_life.contributor
-   sn\_ins\_policy\_b2c.contributor
-   sn\_bom\_deposit\_b2b.contributor
-   sn\_ins\_policy\_b2b.contributor
-   sn\_bom\_credit\_asmt.b2b\_contributor
-   sn\_bom\_loan.contributor
-   sn\_bom\_compl.contributor
-   sn\_bom\_clo\_b2c.contributor
-   sn\_ins\_group\_life.contributor
-   sn\_bom\_clo\_b2b.contributor
-   sn\_bom\_credit\_card.contributor

</td></tr><tr><td>

Financial services agent\[sn\_bom.fs\_agent\]

</td><td>

Universal role for financial services agent. All other agent roles in Financial Services Operations applications inherit this role.

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.line\_of\_credit\_viewer
-   sn\_bom.b2b\_agent
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

Location manager contributor\[sn\_bom.location\_manager\_contributor\]

**Note:** The Business Location plugin must additionally be activated for this role to be enabled. For more information, see [Activate business locations](https://www.servicenow.com/docs/access?context=activate-business-location&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)

</td><td>

User role for managing branch locations. This role can create a case for an account or consumer. Users with this role have read, write, and create access to the FSO tables for branches that they manage.

</td><td>

-   sn\_bom.contributor
-   sn\_customerservice.svc\_location\_manager\_contributor
-   sn\_bom\_deposit\_b2c.contributor
-   sn\_bom\_deposit\_b2b.contributor
-   sn\_bom\_loan.contributor
-   sn\_bom\_compl.contributor
-   sn\_bom\_clo\_b2c.contributor
-   sn\_bom\_clo\_b2b.contributor

</td></tr><tr><td>

Account viewer\[sn\_bom.account\_viewer\]

</td><td>

Consumer role for viewing and creating FSO Case Examples.

</td><td>

-   sn\_bom.loan\_account\_viewer
-   sn\_bom.saving\_account\_viewer
-   sn\_bom.credit\_card\_account\_viewer
-   sn\_bom.deposit\_account\_viewer
-   sn\_bom.mortgage\_viewer
-   sn\_bom.checking\_account\_viewer

</td></tr><tr><td>

Auto loan viewer\[sn\_bom.auto\_loan\_viewer\]

</td><td>

User role for viewing auto loan data.This role has read access to the Auto Loan \[sn\_bom\_auto\_loan\] table.

</td><td>

sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Checking account viewer\[sn\_bom.checking\_account\_viewer\]

</td><td>

User role for viewing checking account data. This role has read access to the following tables:

-   Personal Checking Account \[sn\_bom\_checking\_account\]
-   Business Checking Account \[sn\_bom\_b2b\_checking\_account\]

</td><td>

sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Credit card account viewer\[sn\_bom.credit\_card\_account\_viewer\]

</td><td>

User role for viewing credit card data. This role has read access to the following tables:

-   Credit Card \[sn\_bom\_credit\_card\]
-   Card Transaction \[sn\_bom\_card\_transaction\]

</td><td>

sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Customer data viewer\[sn\_bom.customer\_data\_viewer\]

</td><td>

User role for viewing customer data from FSO applications.

</td><td>

sn\_customerservice.customer\_data\_viewer

</td></tr><tr><td>

Deposit account viewer\[sn\_bom.deposit\_account\_viewer\]

</td><td>

User role for viewing deposit data.This role has read access to the following tables:

-   Deposit Account \[sn\_bom\_deposit\_account\]
-   Deposit Transaction \[sn\_bom\_deposit\_transaction\]

</td><td>

-   sn\_bom.saving\_account\_viewer
-   sn\_bom.checking\_account\_viewer
-   sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Loan account viewer\[sn\_bom.loan\_account\_viewer\]

</td><td>

User role for viewing loan data.This role has read access to the following tables:

-   Loan Account \[sn\_bom\_loan\_account\]
-   Loan Transaction \[sn\_bom\_loan\_transaction\]

</td><td>

-   sn\_bom.customer\_data\_viewer
-   sn\_bom.auto\_loan\_viewer
-   sn\_bom.mortgage\_viewer
-   sn\_bom.personal\_loan\_viewer

</td></tr><tr><td>

Mortgage account viewer\[sn\_bom.mortgage\_viewer\]

</td><td>

User role for viewing mortgage data.This role has read access to the following tables: Mortgage Account \[sn\_bom\_mortgage\_account\]

</td><td>

sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Personal loan viewer\[sn\_bom.personal\_loan\_viewer\]

</td><td>

User role for viewing personal loan data.This role has read access to the Personal Loan \[sn\_bom\_personal\_loan\] table.

</td><td>

sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Reference viewer\[sn\_bom.ref\_data\_viewer\]

</td><td>

User role for viewing reference data for financial institutions.This role has read access to the Financial Institution \[sn\_bom\_financial\_institution\] table.

</td><td>

This role does not contain other roles.

</td></tr><tr><td>

Saving account viewer\[sn\_bom.saving\_account\_viewer\]

</td><td>

User role for viewing savings data.This role has read access to the following tables:

-   Business Checking Account \[sn\_bom\_b2b\_checking\_account\]
-   Personal Saving Account \[sn\_bom\_saving\_account\]

</td><td>

sn\_bom.customer\_data\_viewer

</td></tr><tr><td>

Investment account viewer\[sn\_bom.investment\_account\_viewer\]

</td><td>

This role gives read-only access to investment data entities.

</td><td>

-   sn\_bom.account\_viewer
-   sn\_bom.security\_viewer

</td></tr><tr><td>

Security viewer\[sn\_bom.security\_viewer\]

</td><td>

This role gives read-only access to security data entities.

</td><td>

This role does not contain other roles.

</td></tr><tr><td>

FSO consumer\[sn\_bom.consumer\]

</td><td>

Consumer role for FSO customers.

</td><td>

This role does not contain other roles.

</td></tr></tbody>
</table>## Business rules installed

<table id="table_y2n_fzj_xlb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Limit account number to 4 char

</td><td>

Financial Account \[sn\_bom\_financial\_account\]

</td><td>

Business rule that prevents storing more than four characters in an **Account number** field to help with security.

</td></tr></tbody>
</table>