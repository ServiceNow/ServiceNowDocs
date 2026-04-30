---
title: Create a field recommendation in Recommended Actions
description: Create a field recommendation that you can select when configuring a recommended action. Field recommendations auto-fill a value or suggest a value for a field. For example, this type of action can recommend the assignment group based on the text in the case short description.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Creating guidance and field recommendation in Recommended Actions, Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Create a field recommendation in Recommended Actions

Create a field recommendation that you can select when configuring a recommended action. Field recommendations auto-fill a value or suggest a value for a field. For example, this type of action can recommend the assignment group based on the text in the case short description.

## Before you begin

Use the CSM default record page or the CSM Interaction record page to display field recommendations in CSM Configurable Workspace. For setting the CSM default record page or the CSM Interaction record page as default page, see [Set record page order](config-csm-ws-set-record-page-order.md).

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## About this task

Creating a field recommendation involves two main steps:

-   Creating inputs for the field recommendation.
-   Creating instructions about how to recommend values by configuring a definition for each field.

Depending on the configuration, the recommended field values are auto-filled or shown as messages underneath the fields for the new records. The recommended field values are shown as messages only underneath the fields for the existing records. For an example implementation of field recommendation setup, see [Create a field recommendation for recommending assignment group field value](ex-create-field-recommendation-assg-grp.md).

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Action Types** &gt; **Field Recommendations**.

2.  Click **New** on the Field Recommendations list.

3.  In the **Name** field, enter a name for the field recommendation.

4.  In the **Table** field, select a table.

    This table includes the field for which you’re configuring a recommended value.

5.  Save the record to display the related lists.

6.  In the Field Recommendation Inputs related list, select **New** to create an input.

    1.  In the **Type** field, select the field type for the input.

    2.  In the **Label** field, enter a label for the input.

    3.  In the **Column name** field, enter a column name.

        This name should use lower case letters and underscores. For example, `confidence_score`.

    4.  Configure the settings for the input in the related lists.

        These settings and related lists are determined by the selection in the **Type** field. For example, if you select Reference as the input type, you must configure:

        -   The table and any conditions for the reference field.
        -   The type of list to use.
        -   A default value.
    5.  Click **Submit**.

7.  In the Field recommendation definitions related list, select **New** to create a definition.

    1.  In the **Name** field, enter a name for the definition.

    2.  Select the **Field** to be recommended and save the record to see additional details.

    3.  In the **Recommendation message** field, add the message that is recommended underneath the field on the form.

        You can include the recommended value as part of the message by using the pill-picker.

        **Note:** If the resource generator returns an empty field value, the recommendation message is not displayed.

    4.  In the **Recommended value** field, use the pill-picker to select a value.

    5.  In the **Recommendation Method** list, select one of the options that auto-fills the value or recommends the value as a message.

<table id="table_uqj_twc_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommend only

</td><td>

Displays a recommendation message for the field.

</td></tr><tr><td>

Autofill as per the confidence threshold

</td><td>

-   **Confidence**: Field that provides the confidence score.

Enter a static value or use the pill-picker to select an input that you configured in the Field recommendation inputs related list.

-   **Confidence threshold for direct assignment**: Confidence threshold for the recommendation. If the confidence score is more than the threshold value, the recommended value is auto-filled. Otherwise, a message is displayed.


</td></tr><tr><td>

Autofill as per the resource generator preference

</td><td>

**Recommendation Preference**: Field that has "true" or "false" value for preference. If this value is true, the recommended value for the field is auto-filled. Otherwise, a message is displayed.Enter a static value or use the pill-picker to select an input that you configured in the Field recommendation inputs related list.

</td></tr></tbody>
</table>    6.  Click **Submit**.


