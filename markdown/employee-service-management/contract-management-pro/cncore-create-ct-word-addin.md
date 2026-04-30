---
title: Create a contract template to contain content controls
description: Create a contract template using the Microsoft Word add-in for ServiceNow Contracts to which you can then add content controls.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Create a contract template to contain content controls

Create a contract template using the Microsoft Word add-in for ServiceNow Contracts to which you can then add content controls.

## Before you begin

Verify that the application scope is set to **Global** by selecting the Application scope icon \(![Application scope icon](../../workplace-calendar-synchronization/image/application-scope-globe-icon.png)\) in the header of your homepage.

If you’re creating a contract template for a non-task table, verify that the non-task table is added in the extension script. For more information, see [Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md).

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_qfw_c4s_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the contract template.

</td></tr><tr><td>

Table

</td><td>

Table to which you want to associate the contract template.

</td></tr><tr><td>

Category

</td><td>

Document category to which you want to associate the contract template.

</td></tr><tr><td>

Document

</td><td>

Upload a Microsoft Word document of type `.docx`. This document will be replaced with an updated version containing content controls for metadata, signatory, and clauses using Microsoft Word add-in for ServiceNow Contracts.

</td></tr><tr><td>

State

</td><td>

The initial state is automatically set to Draft.

</td></tr><tr><td>

Application

</td><td>

Application to which the contract template belongs. This field is automatically set to the application scope in which you’re creating the contract template.

</td></tr><tr><td>

Active

</td><td>

Option to make the template active and available for use.

</td></tr><tr><td>

Signature blocks

</td><td>

Option to enable signature blocks in the contract template based on the number of signatories in the contract request.When this option is selected:

-   You can’t upload a participant-based template.
-   The **Participants** related list isn’t available.
For more information, see [Add and configure signature blocks using Microsoft Word add-in for ServiceNow Contracts](cncore-addin-add-sign-block.md).

</td></tr><tr><td>

Start date

</td><td>

Date on which the Word document template becomes valid. Providing a start date helps when maintaining multiple versions of same template.

</td></tr><tr><td>

End date

</td><td>

Date until which the Word document template is valid. Providing an end date helps when maintaining multiple versions of same template.

 If the values in the **Start date** and **End date** fields are empty the template will be always valid.

 **Note:**

If you specify an end date, you must also specify a start date.

</td></tr></tbody>
</table>4.  In the **Contract Type** field, select only one category of the contract type.

    For example, if you’re creating a template for a non-disclosure agreement, select **Non Disclosure Agreement** as the contract type.

    **Note:** Only active contract types are displayed in the list.

5.  Select **Save**.


## Result

The contract template is saved in the Draft state.

## What to do next

[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

**Parent Topic:**[Creating a contract template using Microsoft Word add-in for ServiceNow Contracts](../concept/cncore-setup-ct-add-in.md)

**Related topics**  


[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

[Upload and parse a Microsoft Word document that includes content controls](cncore-upload-doc-addin.md)

[Complete clause mapping to build a clause library](cncore-clause-map-addin.md)

[Add conditions for a contract table mapping](cncore-add-filter-table-map.md)

