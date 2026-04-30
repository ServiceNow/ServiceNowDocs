---
title: Configure a permit type
description: Create a permit type to categorize risk and safety requirements for different types of work.
locale: en-US
release: zurich
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure permit-to-work, Configure, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Configure a permit type

Create a permit type to categorize risk and safety requirements for different types of work.

## Before you begin

Role required: admin and sn\_hs\_rm.permit\_coordinator

## About this task

A permit type is a specific category of permit that addresses unique risks and safety requirements for different kinds of work. Selecting a permit type when filling out a permit to work request automatically adds related questions specific to that permit type.

## Procedure

1.  Navigate to **All** &gt; **System definition** &gt; **Tables**.

2.  Search in the **Label** column for `permits` and select the **Permits to work** table.

3.  In the **Columns** tab, search for and select **Permit type**.

4.  If the Dictionary entry for the permit type displays a message about the application scope, select **here** to be able to edit the record.

5.  Select the Choices related list and select **New**.

6.  On the Choice new record form, fill in the fields.

    For a description of the field values, see [Choice new record form](../reference/hs-choice-new-record-form.md).

7.  Select **Submit**.

    A new permit type is created which appears in the **Permit type** field of the permit-to-work request form. Repeat the steps to create multiple permit types.

8.  Automatically display questions specific to a permit type when the user selects it on the permit-to-work request form by creating a variable set for each permit type. For more information on variable sets and the layout, see [Variable set layout](https://www.servicenow.com/docs/access?context=c_DefineVariableSetLayout&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    1.  Navigate to **All** &gt; **Service catalog** &gt; **Catalog definitions** &gt; **Record producers**.
    2.  Search for and select **Request a permit to work**.
    3.  If the request form displays a message about the application scope, select **here** to be able to edit the record.
    4.  On the **Variable sets** tab of the related list, select **New**.
    5.  Create a variable set with grouped variables by selecting **Single row variable set**.
    6.  On the Variable set new record form, fill in the fields..

        For a description of the field values, see [Variable set new record form](../reference/hs-variable-set-new-record-form.md).

    7.  Select **Submit**.
    8.  Repeat these steps for each permit type.
9.  Add customized questions to the permit type.

    1.  Open a variable set.
    2.  On the Variable new record form, fill in the fields.
    3.  For a description, see [Variable new record form](../reference/hs-variable-new-record.md).
    4.  Select **Submit**.
10. Link the variable set to the permit type.

    1.  Navigate to **All** &gt; **System definition** &gt; **Decision tables**.
    2.  Search for and select **Permit type configuration**.
    3.  Select **Create Draft**.
    4.  In the **Conditions** section, select **Add new decision row**.
    5.  In the **Permit type** column, select the permit type in the **Choice input** field. Select **OK**.
    6.  In the **ariable set** column, select the variable set in the **Choice input** field. Select **OK**.
    7.  Select **Save**.
    8.  Select **Publish** and then select **Publish** again in the confirmation dialog box.
    The variable set with the questions is linked with the permit type and these questions appear on the permit-to-work request form when the permit type is selected.


**Parent Topic:**[Configure permit-to-work](../concept/hs-configure-permit-to-work.md)

