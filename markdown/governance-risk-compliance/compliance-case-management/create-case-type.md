---
title: Create a case type
description: Create a case type in the GRC: Compliance Case Management application to categorize the compliance cases by the type of occurrence. For example, you can create a case type, such as a financial case, code of conduct, or HR case.
locale: en-US
release: zurich
product: Compliance Case Management
classification: compliance-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Compliance Case Management, Governance, Risk, and Compliance]
---

# Create a case type

Create a case type in the GRC: Compliance Case Management application to categorize the compliance cases by the type of occurrence. For example, you can create a case type, such as a financial case, code of conduct, or HR case.

## Before you begin

Role required: sn\_compliance\_case\_admin

## About this task

You can set up a case type to categorize the compliance cases by the type of occurrence. After you define the case type, the compliance analyst and compliance manager can select the case type on the case form. A case type is mapped with a state model that specifies the workflow states and transition conditions for the compliance case. To define the workflow states and transitions, see [Create a compliance state model](create-state-model.md).

## Procedure

1.  Navigate to **All** &gt; **Compliance Case Management** &gt; **Case types**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the field values on the case type form, see [Case Type form](../reference/case-type-form.md).

4.  Open the form context menu and select **Save**.

    The Case subtypes related list appears.

5.  On the Case subtypes related list, select **New** to define a case subtype.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Label to be displayed for the case subtype.|
    |Name|Name of the case subtype. For example, Conflict of interest.|
    |Parent|Parent case type. This field is automatically set to the parent case type.|
    |Active|Option to select the case subtype as active or inactive.|
    |Description|Description of the purpose of the case subtype. This description is for the administrator to understand the case subtype.|

7.  Select **Submit**.

8.  To create a view rule instead of using the default one, see [Create view rule](create-view-rule.md).

9.  To create an assignment rule instead of using the default one, see [Create an assignment rule](create-assignment-rule.md).


-   **[Case Type form](../reference/case-type-form.md)**  
Use the Case Type form in the Compliance Case Management application to categorize the compliance cases by their type.
-   **[Create view rule](create-view-rule.md)**  
Define the view rules for the workspace and default view in the GRC: Compliance Case Management application. By defining the rules, you can control how the compliance case or request form appears.
-   **[Create an assignment rule](create-assignment-rule.md)**  
Create an assignment rule and apply it to a compliance case type or request type by using the Compliance Case Management application. By using an assignment rule, you can determine the appropriate person or group to handle a compliance case.

**Parent Topic:**[Configuring Compliance Case Management](../concept/configure-compliance-case-management.md)

