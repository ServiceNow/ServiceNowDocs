---
title: Configuring Personal Data Rights request type
description: Create a request type in the Personal Data Rights application to categorize and manage the personal data rights requests. After you create a request type, the personal data rights agents and the task owners can select the required request type on the request form while working on a personal data rights request.
locale: en-US
release: yokohama
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Configuring Personal Data Rights request type

Create a request type in the Personal Data Rights application to categorize and manage the personal data rights requests. After you create a request type, the personal data rights agents and the task owners can select the required request type on the request form while working on a personal data rights request.

## Before you begin

Role required: sn\_grc\_pdr.pdr\_admin

## Procedure

1.  Navigate to **All** &gt; **Personal Data Rights** &gt; **Request Configuration** &gt; **Request type**.

    The default personal data rights request record type opens.

2.  On the form, fill in the fields.

    For a description of the field values on the request type form, see [Personal Data Rights request type form](../reference/pdr-request-type-form.md).

3.  Open the form context menu and select **Save**.

    The Subtypes related list appears.

4.  On the Subtypes related list, select **New** to define a request subtype.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Label to be displayed for the subtype. For example, `Right to delete`.|
    |Name|Name of the subtype. For example, `right_to_delete`.|
    |Parent|Parent request type. This field is automatically set to the **Personal data rights request**.|
    |Active|Option to select the subtype as active or inactive.|
    |Category|Category of the subtype. This field is automatically set to **Personal data rights request \[sn\_grc\_pdr\_request\]**.|
    |Description|Description of the purpose of the subtype. This description is for the administrator to understand the request subtype.|

6.  Select **Submit**.

7.  To add Jurisdictions that are affected by the record type, select **New** and fill in the form as required.


-   **[Personal Data Rights request type form](../reference/pdr-request-type-form.md)**  
Use the Request Type form in the Personal Data Rights application to categorize the personal data rights requests by their type.

**Parent Topic:**[Configuring Personal Data Rights](../concept/configuring-personal-data-rights.md)

