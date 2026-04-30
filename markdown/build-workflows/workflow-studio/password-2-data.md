---
title: Password \(2 Way Encrypted\) design considerations
description: Store encrypted password data that can be decrypted.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow Studio input and output data variables, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Password \(2 Way Encrypted\) design considerations

Store encrypted password data that can be decrypted.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options

|Option|Description|
|------|-----------|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Default value|Specifies the value used when a flow or action designer does not provide a value.|

## General guidelines

Follow these general guidelines when designing flows containing Password \(2 Way Encrypted\) data.

-   **Assign values using existing Password \(2 Way Encrypted\) data pills.**

    You can only assign a value to a password2 variable by selecting an existing password2 data pill. Selecting values from other field types is not supported. Workflow Studio presents a warning message when invalid data pill types are selected.

    ![The warning message displayed when dragging a non-password2 data pill onto a password2 field.](../images/password2-field-warning.ong.png)

    **Note:** You cannot manually enter Password \(2 Way Encrypted\) values.

-   **Use Password \(2 Way Encrypted\) variables only for valid field types**

    Workflow Studio prevents selecting Password2 data pills as the value for invalid field types. The system presents a warning message when the field is an incompatible type.

    ![The warning shown when dragging a password2 field to a disallowed field.](../images/password2-field-warning2.png)

    Workflow Studio only allows Password2 data pills to be dragged into the following field types.

    -   Email body fields
    -   HTML fields
    -   Password 2 Fields
    -   PowerShell Input Variables
    -   REST fields
        -   Variables
        -   REST payload body
        -   Query parameters
        -   Headers
        -   REST multi-part form values
        -   Form URL-encoded values
    -   SOAP fields
        -   Headers
        -   Envelope
    **Note:** you cannot use Password \(2 Way Encrypted\) variables as conditions

    Flow Designer performs a validation check when a user saves, publishes, or tests actions and flows. This check shows that an alert for any data pills dropped in restricted field types and prevents the action or flow from executing. Update the action or flow to remove the invalid data pill and then retry the action.

-   **Set up encryption modules for decryption**

    Only users with a valid encryption module access can decrypt and view the contents of password2 variables. To specify the encryption algorithm and which roles can access encrypted data, see [Password2 encryption with KMF](https://www.servicenow.com/docs/access?context=password-2way-encrypted-fields&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) .


**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

