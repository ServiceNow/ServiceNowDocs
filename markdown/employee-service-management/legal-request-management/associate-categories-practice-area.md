---
title: Add an intake form to a practice area
description: Add an intake form to a practice area to associate it with a record producer and define assignment rules and service level agreements.
locale: en-US
release: xanadu
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Create or modify a practice area, Setting up Legal Request Management, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Add an intake form to a practice area

Add an intake form to a practice area to associate it with a record producer and define assignment rules and service level agreements.

## Before you begin

Role required: sn\_lg\_ops.legal\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Practice Areas**.

2.  Open a practice area to which you want to add an intake form.

3.  In the Intake Forms related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_vcb_2k5_njb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the intake form.

</td></tr><tr><td>

Default subcategory

</td><td>

Default subcategory to associate with the intake form.

</td></tr><tr><td>

Practice area

</td><td>

Practice area to which the intake form belongs.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the intake form.

</td></tr><tr><td class="sub-head" colspan="2">

Record Producer section

</td></tr><tr><td>

Type

</td><td>

Type of record producers to associate with the intake form. You can select from the following options:-   **Request**: The practice area lead cannot promote requests submitted under this practice area to a legal matter.
-   **Matter**: Legal department users can submit a matter under this practice area.
-   **Request and Matter**: The practice area lead can promote requests submitted under this practice area to a legal matter. During promotion, the field values from the legal request record are copied over to the matter record.


</td></tr><tr><td>

Request record producer

</td><td>

Record producer to submit requests in the associated practice area. Select an existing request record producer or use the **Create Request record producer** related link to create one. The newly created request record producer contains default values for a few fields that will be pre-populated in the request form.

 **Note:** The **Create Request record producer** related link appears only when this field is empty.

 This field appears only when **Request** or **Request and Matter** is selected as the Type value.

</td></tr><tr><td>

Matter record producer

</td><td>

Record producer to create a legal matter.If a matter can be created directly, associate an existing matter record producer. To create and associate a new matter record producer, click the **Create Matter record producer** related link.

 **Note:** The **Create Matter record producer** related link is available when this field is empty.

 This field appears only when **Matter** is selected as the Type value.

</td></tr><tr><td>

Default matter template

</td><td>

Matter template that is selected by default while promoting the associated legal request to a matter.This field appears only when **Matter** or **Request and Matter** is selected as the Type value.

</td></tr><tr><td>

Options

</td><td>

Options to change the default behavior or flow of legal requests, legal matter, or both as per your business needs. You can select from the following predefined options:-   **Assigned To field not mandatory**: The **Assigned to** field on the Legal Request form becomes an optional field.
-   **Disable Request Adhoc Approvals**: Legal fulfiller working on the legal request cannot initiate an ad hoc approval for requests or attachments. The **Initiate Approval** button will not be available on the Legal Request form.
-   **Disable Request Reopen**: The requester cannot reopen a legal request that has been closed. The **Reopen Request** button is not available on the Standard Ticket page.
-   **Editable Assignment group in Request**: The practice area lead, group manager, and legal fulfiller \(user in the **Assigned to** field\) can change the assignment group in a legal request.

**Note:** On changing the assignment group, a member of the existing group member who is not in the updated assignment group might lose access to the request. The **Assigned to** field is also cleared.

-   **Editable Assignment group in Matter**: The practice area lead, group manager, and legal fulfiller \(user in the **Assigned to** field\) can change the assignment group in a legal matter.

**Note:** On changing the assignment group, a member of the existing group member who is not in the updated assignment group might lose access to the matter. The **Matter owner** field is also cleared.

-   **Enable External Storage for attachment**: The documents attached to legal requests and legal mattersare uploaded to a [configured external storage system](integrate-legal-ext-storage.md).

**Important:** Only one external storage provider can be configured for an intake form.

-   **Enable Legal Request creation From Universal Request**: Legal requests can be created from a [universal request](../../universal-request/concept/ur-landing-limitedaccess.md) to get the support of the Legal department for the resolution of the universal request.
-   **Make Request Fulfiller as Matter Owner**: When a legal request is promoted to a legal matter, this legal matter is automatically assigned to the legal request fulfiller.
-   **Generate Document from Template**: When a legal request for contract review is submitted, this option determines whether the document will be generated using a document template. If this option is not selected, the requester must submit the contract for review.

**Note:** The option is available only for the sn\_lg\_ops\_contract\_request table.

-   **Update request fields with variables**: When you submit a legal request for contract review or update the variables, the field values mapped to the variables are automatically updated.
-   **Initialize legal contract**: A contract request is automatically created when a legal request for contracts is submitted.


</td></tr></tbody>
</table>5.  Click **Submit**.

    An intake form is added to the practice area. The Checklist section and related lists to manage subcategories, service level agreement definitions, assignment rules, and matter templates appear.

6.  Add to-do items in the Checklist section to provide a list of activities for the request fulfiller.

    When an employee submits a new legal request through the intake form, this predefined checklist appears as the default to-do items in the corresponding request.

    1.  Click the more actions icon \(![More actions icon.](../../employee-center/images/down-arrow-icon.png)\) next to the **Checklist**.

    2.  Click **Create new**.

    3.  Enter a description for the to-do item and press the Enter key.


## What to do next

-   From the Subcategories related list, [add a new one subcategory](add-subcategories-intakeform.md) to associate it with the intake form.
-   From the SLA Definitions related list, [create a service level agreements \(SLA\) definition](https://www.servicenow.com/docs/access?context=t_CreateAnSLADefinition&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US), if required.
-   From the Assignments Rules related list, [create an assignment rule for an intake form](create-assignment-rules-intake-form.md).
-   Click the **Edit in Catalog Builder** related link to update the record producer for a legal request or matter or both based on the **Type** field value. For more information, see [Create or modify a record producer for legal services through Catalog Builder](create-record-producer-catalog-builder-legal.md).

    The admin can also [create or modify record producers for legal services](create-record-producer-legal-request.md).

-   From the Matter Templates related list, [associate a matter template with the intake form](associate-matter-template-with-intake-form.md) if a matter record producer is selected.

