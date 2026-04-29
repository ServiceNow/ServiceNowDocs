---
title: Define a category and measurement unit for an exposure type
description: Define a category and measurement unit for an exposure type. If needed, you can also associate a subcategory with an exposure type category.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Define a category and measurement unit for an exposure type

Define a category and measurement unit for an exposure type. If needed, you can also associate a subcategory with an exposure type category.

## Before you begin

Verify that the application scope is selected as Health and Safety Risk Management. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Create an exposure category or update an existing one.

    1.  Select to open the Exposure type \[sn\_hs\_rm\_exposure\_type\] table.

    2.  In the **Columns** tab, select `Exposure category` from the list.

    3.  In the **Choices** tab, select **New**.

    4.  Fill in the fields.

        The value set in the **Value** field is used to associate a sub-category or a measurement unit with this category.

    5.  Select **Submit**.

3.  Associate a subcategory with an exposure category.

    1.  In the **Columns** tab of the Exposure type \[sn\_hs\_rm\_exposure\_type\] table, select the `Exposure sub-category` from the list.

    2.  In the **Choices** tab, select **New** and fill in the fields.

    3.  In the **Dependent value** field, copy the exposure category's **Value** field defined in step 2d.

        This associates the subcategory with the required category.

    4.  Select **Submit**.

    The subcategory is listed as a choice in the **Sub-category** field for the associated exposure category when creating an exposure type. For more information, see [Define an exposure type](hs-define-exposure-type.md).

4.  Add a measurement unit for an exposure category.

    1.  Select to open the Measurement \[sn\_hs\_rm\_measurement\] table.

    2.  In the **Columns** tab, select `Measurement unit` from the list.

    3.  In the **Choices** tab, select **New** and fill in the fields.

    4.  In the **Dependent value** field, copy the exposure category's **Value** field defined in step 2d.

        The value in the **Dependent value** field links the measurement unit with the required exposure category.

    5.  Select **Submit**.

    The measurement unit is listed as a choice in the **Measurement unit** field during an exposure assessment for the exposure type. For more information, see [Add a measurement and exposure source for an exposure assessment](hs-add-measurement-exposure-assessment.md).


**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)

