---
title: Configure SLA definitions
description: Review the service level agreement \(SLA\) definitions that are installed with Financial Services Operations applications. You can update existing SLAs or add new SLAs to configure start, pause, and stop conditions on any case attributes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Configure SLA definitions

Review the service level agreement \(SLA\) definitions that are installed with Financial Services Operations applications. You can update existing SLAs or add new SLAs to configure start, pause, and stop conditions on any case attributes.

## Before you begin

Role required: Based on the application that you are configuring, you need the following roles:

-   For Financial Services Payment Operations: sn\_bom\_payment.admin and admin
-   For Financial Services Card Operations: sn\_bom\_card.admin and admin
-   For Financial Services Complaint Management: sn\_bom\_compl.admin and admin
-   For Financial Services Business Deposit Operations: sn\_bom\_deposit\_b2b.admin and admin
-   For Financial Services Personal Deposit Operations: sn\_bom\_deposit\_b2c.admin and admin
-   For Financial Services Business Loan Operations: sn\_bom\_loan\_b2b.admin and admin
-   For Financial Services Personal Loan Operations: sn\_bom\_loan.b2c\_admin and admin
-   For Financial Services Business Lifecycle: sn\_bom\_clo\_b2b.admin and admin
-   For Financial Services Client Lifecycle: sn\_bom\_clo\_b2c.admin and admin
-   For Financial Services Know Your Customer: sn\_bom\_kyc.admin and admin
-   For Financial Services Treasury Operations: sn\_bom\_treasury.admin and admin
-   Individual Life Claims: sn\_ins\_claim\_indl.admin and admin
-   Insurance claims: sn\_ins\_gen\_claim.admin and admin

## About this task

An SLA is a record that specifies the time within which a service must be provided. The Financial Services Operations applications use SLAs with cases such as payment inquiry, claim, and credit card.

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **SLA** &gt; **SLA Definitions**.

2.  Create an SLA definition or modify an existing SLA definition.

    -   To create an SLA definition, click **New**.
    -   To review an existing SLA definition, filter the list to show the SLAs for the application tables and open an SLA definition.

<table id="table_dvk_z2m_3mb"><thead><tr><th>

Application

</th><th>

Table

</th></tr></thead><tbody><tr><td>

Financial Services Payment Operations

</td><td>

-   Payment Inquiry Case \[sn\_bom\_payment\_inquiry\]
-   Claim \[sn\_bom\_payment\_claim\]


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   Credit Card Service \[sn\_bom\_credit\_card\_service\]
-   Credit Card Task \[sn\_bom\_credit\_card\_task\]
-   Card Disputes Task \[sn\_bom\_credit\_card\_disputes\_task\]
-   Card Disputes Service Case \[sn\_bom\_credit\_card\_disputes\_service\]


</td></tr><tr><td>

Financial Services Business Loan Operations

</td><td>

-   Loan Service Case \[sn\_bom\_loan\_b2b\_service\]
-   Loan Task \[sn\_bom\_loan\_b2b\_task\]
-   Credit Service Case \[sn\_bom\_credit\_asmt\_loan\_b2b\_service\]


</td></tr><tr><td>

Financial Services Personal Loan Operations

</td><td>

-   Loan Service Case \[sn\_bom\_loan\_service\]
-   Loan Task \[sn\_bom\_loan\_task\]
-   Credit Service Case \[sn\_bom\_credit\_asmt\_loan\_service\]


</td></tr><tr><td>

Financial Services Business Lifecycle

</td><td>

-   Account Lifecycle Service Case \[sn\_bom\_clo\_b2b\_account\_service\]
-   Account Lifecycle Task \[sn\_bom\_clo\_b2b\_account\_task\]
-   Contact Lifecycle Service Case \[sn\_bom\_clo\_b2b\_contact\_service\]


</td></tr><tr><td>

Financial Services Client Lifecycle

</td><td>

-   Client Lifecycle Service Case \[sn\_bom\_clo\_b2c\_service\]
-   Client Lifecycle Task \[sn\_bom\_clo\_b2c\_task\]


</td></tr><tr><td>

Financial Services Know Your Customer

</td><td>

-   KYC Account Task \[sn\_bom\_kyc\_account\_task\]
-   KYC Contact Task \[sn\_bom\_kyc\_contact\_task\]
-   KYC Customer Task \[sn\_bom\_kyc\_customer\_task\]


</td></tr><tr><td>

Financial Services Complaint Management

</td><td>

-   Complaint Case \[sn\_bom\_compl\_service\]
-   Complaint Service Task \[sn\_bom\_compl\_task\]
-   Quality Control Task \[sn\_bom\_compl\_qc\_task\]


</td></tr><tr><td>

Financial Services Treasury Operations

</td><td>

-   RDC Service Case \[sn\_bom\_treasury\_rdc\_service\]
-   Wire Service Case \[sn\_bom\_treasury\_wire\_service\]
-   Treasury Task \[sn\_bom\_treasury\_task\]


</td></tr><tr><td>

Intelligent Servicing for Fraud

</td><td>

-   Fraud Case \[sn\_bom\_fraud\_case\]
-   Fraud Task \[sn\_bom\_fraud\_task\]
-   Fraud Transaction \[sn\_bom\_fraud\_transaction\]


</td></tr><tr><td>

Individual Life Claims

</td><td>

Individual Death Claim \[sn\_ins\_claim\_indl\_death\_case\]

</td></tr><tr><td>

Insurance claims

</td><td>

-   Claim Case \[sn\_ins\_gen\_claim\_case\]
-   Claim Adjuster Task \[sn\_ins\_gen\_claim\_adj\_task\]


</td></tr></tbody>
</table>3.  On the form, fill in the fields.

    For detailed instructions and field descriptions, see Create an SLA definition.

4.  Click **Submit** or **Update**.


## Result

The SLA definition is created for the table that you specified.

## What to do next

In Workspace, you can track the SLA for a case from the **Task SLAs** tab on the case form.

