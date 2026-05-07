---
title: Add and configure participants for a contract using the Microsoft Word add-in for ServiceNow Contracts
description: As a contract configurator, configure participants and add placeholders for their signatures using the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure signatories, Add content controls, Create templates in Microsoft Word, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add and configure participants for a contract using the Microsoft Word add-in for ServiceNow Contracts

As a contract configurator, configure participants and add placeholders for their signatures using the Microsoft Word add-in for ServiceNow® Contracts.

## Before you begin

The Microsoft Word add-in for ServiceNow Contracts must have been configured. For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md).

An active contract template must exist in the Draft or Editing state where the **Signature blocks** option is not selected. For more information, see [Create a contract template to contain content controls](cncore-create-ct-word-addin.md).

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the document in which you want to mark the content controls in Microsoft Word.

2.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

3.  In the login screen, enter the credentials of the ServiceNow instance from which you downloaded the manifest file.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

4.  On the add-in screen in the **Templates** tab, select the contract template to which you want to add the metadata.

5.  In the **Signatory** tab, select **Add signatory**.

    ![Add signatory content controls that act as placeholder for signatures](../image/cmpro-waddin-participant.png "Add signatory")

6.  Add and configure the participant as either an internal or external user.

    -   While adding signatory details, if you add value in the **User** field, the participant is considered an internal signatory.
    -   While inserting content controls for signatures or signatories, ensure the font color of the tagged text matches the document’s background color.
<table id="choicetable_qfz_dkb_yyb"><thead><tr><th align="left" id="d378512e214">

Type of signatory

</th><th align="left" id="d378512e217">

Available fields

</th></tr></thead><tbody><tr><td id="d378512e223">

**Internal**

</td><td>

-   **Name** - Unique display name of the mapped signer.
-   **Order** - Unique order in which a signature has to be initiated for the participant to complete the action.
-   **User** - The field from the table associated with the contract template that acts as a placeholder for the user. For example: **Assigned to**.

**Note:**

    -   When you select a value for this field, the participant is considered to be an internal user. If values are provided for the optional fields **Participant Name** and **Participant Email** along with the **User** field, the electronic signature request is sent to participant email values rather than the **Name** and **Email** fields associated with the user record.
    -   If the **Advanced script** field is selected, the value in the **User** field is cleared when you save or update the template.
-   **Participant name** \(Optional\) - The field from the table associated with the contract template that will act as a placeholder for the participant name. For example: **Closed by**.
-   **Participant email** \(Optional\) - The field from the table associated with the contract template that acts as a placeholder for the participant email address. For example: **Closed by &gt; Email**.
-   **Participant title** \(Optional\) -

Option to specify the title when the defined participant is an external user.

**Note:**

    -   The value in the Participant title field is cleared when you save or update the template with the Advanced script field selected.
    -   This field is available only when signing type is AdobeSign or DocuSign.


</td></tr><tr><td id="d378512e320">

**External**

</td><td>

-   **Name** - Fields of the table to which the contract template is associated.
-   **Order** - Order in which a signature has to be initiated for the participant to complete the action.
-   **User** - Do not provide any value.
-   **Participant name** - The field from the table associated with the contract template that acts as a placeholder for the participant name. For example: **Closed by**.

This field is available only when the signing type is AdobeSign or DocuSign.

**Note:** The value in the **Participant name** field is cleared when you save or update the template with the Advanced script field selected.

-   **Participant email**- The field from the table associated with the contract template that acts as a placeholder for participant email. For example: **Closed by &gt; Email**.

This field is available only when the signing type is AdobeSign or DocuSign.

**Note:** The value in the Participant email field is cleared when you save or update the template with the Advanced script field selected.

-   **Participant title** \(Optional\) -

Option to specify the title when the defined participant is an external user.

**Note:**

    -   The value in the Participant title field is cleared when you save or update the template with the Advanced script field selected.
    -   This field is available only when signing type is AdobeSign or DocuSign.


</td></tr></tbody>
</table>7.  Fill in the signatory details and select **Create**.

    ![Signatory card in ServiceNow Contracts add-in](../image/cmpro-waddin-participant-added.png "Signatory card in Word Add-in")

    -   The signatory is added and the signer card is displayed.
    -   The signatory is marked as internal or external depending on the values provided.
    -   The signatory added has Sign, Sign date, Sign Title, Sign Name, Sign Email metadata.
8.  Add the signatory content controls to the placeholder text for the signature elements.

    1.  Place the cursor where you want the signature to be added.

    2.  Add placeholder text at the locations where you want to place the content controls.

        ![Add placeholder text for the signature content control](../image/cmpro-waddin-sigtext.png)

    3.  Set the font color of the placeholder text to match the document’s background color.

    4.  Select the signature tags to place the signature content controls.

        ![Add content control](../image/cmpro-waddin-signadd-tag.png)

9.  Complete the steps for the other content controls:

    -   **sign\_date**
    -   **signatory\_title**
    -   **signatory\_name**
    -   **signatory\_email**
    The signatory fields—such as Name, Title, and Email—are not pre-filled in the contract document before it is sent for signature. These fields will be populated by the electronic signature provider when the signatory access the document to sign it.

10. View the signatory details by logging in to the ServiceNow instance and navigating to the **Participants** related list of the contract template.


## Result

The signatory content controls are added and the metadata is synced to the ServiceNow instance.

![Signatory content control is added at the placeholder text](../image/cmpro-waddin-signtag-added.png "Content controls added at the placeholder text")

![View the participant added from ServiceNow Contracts add-in in your instance](../image/cmpro-waddin-view-participant-sn.png "Participants related list in your instance")

**Parent Topic:**[Configuring signatories in Contract template using Microsoft Word add-in](../concept/cncore-config-sign-addin.md)

**Related topics**  


[Add and configure signature blocks using Microsoft Word add-in for ServiceNow Contracts](cncore-addin-add-sign-block.md)

