---
title: Create a request type
description: Create a request type in the GRC: Compliance Case Management application to categorize and manage the compliance requests. After you create a request type, the compliance analysts and managers can select the required request type on the request form.
locale: en-US
release: australia
product: Compliance Case Management
classification: compliance-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Compliance Case Management, Governance, Risk, and Compliance]
---

# Create a request type

Create a request type in the GRC: Compliance Case Management application to categorize and manage the compliance requests. After you create a request type, the compliance analysts and managers can select the required request type on the request form.

## Before you begin

Role required: sn\_compliance\_case\_admin

## Procedure

1.  Navigate to **All** &gt; **Compliance Case Management** &gt; **Request types**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the field values on the request type form, see [Request type form](../reference/request-type-form.md).

4.  Open the form context menu and select **Save**.

    The Subtypes related list appears.

5.  On the Subtypes related list, select **New** to define a request subtype.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Label to be displayed for the subtype.|
    |Name|Name of the subtype. For example, Policy update.|
    |Parent|Parent request type. This field is automatically set to the parent request type.|
    |Active|Option to select the subtype as active or inactive.|
    |Case category|Category of the subtype. This field is automatically set to **Compliance case \[sn\_comp\_case\_compliance\_request\]**.|
    |Description|Description of the purpose of the subtype. This description is for the administrator to understand the request subtype.|

7.  Select **Submit**.

8.  To create a view rule instead of using the default rule, see [Create view rule](create-view-rule.md).

9.  To create an assignment rule instead of using the default rule, see [Create an assignment rule](create-assignment-rule.md).


-   **[Request type form](../reference/request-type-form.md)**  
Use the Request Type form in the Compliance Case Management application to categorize the compliance requests by their type.

**Parent Topic:**[Configuring Compliance Case Management](../concept/configure-compliance-case-management.md)

