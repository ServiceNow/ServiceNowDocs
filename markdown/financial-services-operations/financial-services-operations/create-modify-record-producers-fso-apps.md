---
title: Create or modify record producers
description: Review the record producers that are installed with Financial Services Operations applications. You can modify the predefined record producers or add new ones to define how the request forms appear in the Banking Service catalog or Consumer Service portal, or both.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Create or modify record producers

Review the record producers that are installed with Financial Services Operations applications. You can modify the predefined record producers or add new ones to define how the request forms appear in the Banking Service catalog or Consumer Service portal, or both.

## Before you begin

Ensure that the scope is selected for the application for which you are creating a record producer. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: Based on the application that you are configuring, you need the following roles:

-   For Financial Services Payment Operations: sn\_bom\_payment.admin and admin
-   For Financial Services Card Operations: sn\_bom\_card.admin and admin
-   For Financial Services Complaint Management: sn\_bom\_compl.admin and admin
-   For Financial Services Business Deposit Operations: sn\_bom\_deposit\_b2b.admin and admin
-   For Financial Services Personal Deposit Operations: sn\_bom\_deposit\_b2c.admin and admin
-   For Financial Services Business Loan Operations: sn\_bom\_loan\_b2b.admin and admin
-   For Financial Services Personal Loan Operations: sn\_bom\_loan.b2c\_admin and admin

## About this task

A record producer enables users to submit banking requests from the Banking Service catalog and Consumer Service portal and stores the requested information as a record in the associated table.

For information on record producers that are available with Financial Services Operations, see [Record producers for Financial Services Operations applications](../reference/record-producers-fso-applications.md).

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Record Producers**.

2.  Create a record producer or modify an existing one.

    -   To create a record producer, click **New**.
    -   To customize a predefined record producer, open the record producer that you want to customize.
    For information about the record producer form fields, see [Create a record producer](https://www.servicenow.com/docs/access?context=t_DefRecProdInSCat&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

3.  On the form, fill in the fields.

<table id="table_n3z_2vb_jmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record producer.

</td></tr><tr><td>

Table name

</td><td>

Table that the record producer is associated with. These tables store the request form data. -   Select Credit Card Service \[sn\_bom\_credit\_card\_service\] table for credit card requests.
-   Select Payment Inquiry Case \[sn\_bom\_payment\_inquiry\] table for payment inquiry requests.
-   Select Claim \[sn\_bom\_payment\_claim\] table for payment claim requests.
-   Select Loan Service Case \[sn\_bom\_loan\_b2b\_service\] table for business loan requests.
-   Select Loan Service Case \[sn\_bom\_loan\_service\] table for personal loan requests.
-   Select Complaint Case \[sn\_bom\_compl\_service\] table for complaint service requests.


</td></tr><tr><td>

Application

</td><td>

Application to which the record producer form belongs. This field is automatically set when you select the application scope in which the record producer should be created.

</td></tr><tr><td>

Active

</td><td>

Option to activate the record producer for use.

</td></tr><tr><td class="sub-head" colspan="2">

What it will contain tab

</td></tr><tr><td>

Short description

</td><td>

Brief description of the record producer.

</td></tr><tr><td>

Description

</td><td>

Full description of the record producer.

</td></tr><tr><td>

Script

</td><td>

Script that dynamically assigns values to specific fields on the created record.

</td></tr><tr><td class="sub-head" colspan="2">

Accessibility tab

</td></tr><tr><td>

Catalogs

</td><td>

Name of the catalog to which the record producer belongs. Select **Banking Services** or **Consumer Service**.

</td></tr><tr><td>

Category

</td><td>

Name of the catalog category in which the record producer should appear.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.

5.  In the Variables or Variable Sets related lists, configure variables as appropriate.

    Variables collect information from the user when the user submits a request through the record producer. Variables also map predefined answers to the fields. You can add as many variables as you need to the record producer. For more information, see [Create a service catalog variable](https://www.servicenow.com/docs/access?context=t_CreateAVariableForACatalogItem&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

6.  In the Available For and Not Available For related lists, configure the user criteria to grant or deny users access to the record producer.

    For more information, see [Set up the user criteria](https://www.servicenow.com/docs/access?context=t_CreateAUserCriteriaRecord&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

7.  Click **Update**.


-   **[Record producers for Financial Services Operations applications](../reference/record-producers-fso-applications.md)**  
A record producer enables your users to submit banking requests from the Banking Service catalog and Consumer Service portal and stores the requested information as a record in the associated table.

**Parent Topic:**[Configuring Financial Services Operations](../concept/setting-up-fso-applications.md)

