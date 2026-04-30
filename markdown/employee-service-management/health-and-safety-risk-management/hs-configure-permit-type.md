---
title: Configure a permit type
description: Create a permit type to be selected in the permit-to-work request form.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure permit-to-work, Configure settings, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Configure a permit type

Create a permit type to be selected in the permit-to-work request form.

## Before you begin

Role required: admin and sn\_hs\_rm.permit\_coordinator

## About this task

The admins must assign specific roles to the sn\_hs\_rm.permit\_coordinator role to enable the permit coordinator to perform this configuration. For more information, see [Configure permit-to-work](../concept/hs-configure-permit-to-work.md).

## About this task

A permit type is a specific category of permit that a permit requestor selects when completing the permit-to-work request form. Each permit type addresses unique risks and safety requirements for different kinds of work. Selecting a permit type in the form automatically adds related questions specific to that permit type.

## Procedure

1.  Navigate to **All** &gt; **System definition** &gt; **Tables** and select the **Permits to work** table.

2.  Select **Permit type** in the **Columns** tab of the related list.

    Opens the **Dictionary entry** for permit type.

3.  Select the **Choices** tab in the related list and select **New**.

4.  On the form, fill in the fields.

    For more information on the field description, see [Choice new record form](../reference/hs-choice-new-record-form.md).

5.  Select **Submit**.

    A new permit type is created which appears in the **Permit type** field of the permit-to-work request form. Repeat the steps to create multiple permit types.

6.  Automatically display questions specific to a permit type when the user selects it on the permit-to-work request form.

    1.  Navigate to **All** &gt; **Service catalog** &gt; **Catalog definitions** &gt; **Record producers**.
    2.  Search and select **Request a permit to work** record.
    3.  Select **New** on the **Variable sets** tab of the related list.
    4.  On the form, select **Single row variable set**.

        This creates a variable set with variables that are grouped.

    5.  On the form, fill in the fields. For more information on the field description, see [Variable set new record form](../reference/hs-variable-set-new-record-form.md).
    6.  Select **Submit**.
        -   Repeat the steps to create additional variable sets for the same record producer. These variable sets includes permit type specific questions that appear on the permit-to-work request form when the permit type is selected.
        -   For more information on variable sets and the layout, see [Variable set layout](https://www.servicenow.com/docs/access?context=c_DefineVariableSetLayout&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
7.  Add customized questions to the permit type.

    1.  Open a variable set and on the form fill in the fields. For more information on the field description, see [Variable new record form](../reference/hs-variable-new-record.md).
    2.  Select **Submit**.
8.  Link the variable set to permit type.

    1.  Navigate to **All** &gt; **System definition** &gt; **Decision tables** and select **Permit type configuration**
    2.  Select **Draft** and select **Add new decision row**.
    3.  Select the empty cell in the **permit type** column and select the permit type in the **Choice input** field. Select **OK**.
    4.  Select the empty cell in the **variable set** column and select the variable set in the **Choice input** field. Select **OK**.
    5.  Select **Save**.
    6.  Select **Publish** and then select **Publish** in the modal dialogue.
    The variable set with the questions is linked with the permit type and these questions appear on the permit-to-work request form when the permit type is selected.


**Parent Topic:**[Configure permit-to-work](../concept/hs-configure-permit-to-work.md)

