---
title: Edit a question in Catalog Builder
description: Edit an existing question if you want to improve it by adding dynamic form behavior.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Creating or editing catalog item template, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a question in Catalog Builder

Edit an existing question if you want to improve it by adding dynamic form behavior.

## Before you begin

Role required: catalog\_builder\_editor, catalog\_admin, or admin

## About this task

Set values for the fields and condition-based field messages. Make the question mandatory, visible, or read-only based on your requirements. You can also deactivate the question.

You can’t edit the questions that belong to single-row and multi-row variable sets.

-   If the question is used in a published catalog item, you can’t delete it but you can mark it as inactive. You can include such questions again in the catalog item by using the **Insert De-activated questions** option.
-   Removing a new question that has never been published deletes the question.
-   You can’t remove questions of types that aren't allowed in the template or supported in the Catalog Builder.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  Select the **Catalog items** tab.

3.  Select a catalog item and navigate to the **Questions** tab.

4.  Deactivate a question.

    1.  Point to the question and select the deactivate icon \(![Deactivate icon.](../image/deactivate-quest.png)\).

    2.  In the dialog box, select **Deactivate**.

5.  Edit a question.

    1.  Point to the question and select the edit icon \(![Edit icon.](../image/edit-quest-builder.png)\).

    2.  Make the required changes and select **Save**.

6.  Add dynamic form behavior to a question.

    1.  Point to the question and select the UI policies icon \(![UI policies icon.](../image/dyn-beh-quest.png)\) for defining dynamic behavior.

    2.  In the Dynamic behavior dialog box, select **Define new behavior**.

    3.  On the **Actions** tab, fill in the required information.

<table id="table_zm4_jp2_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Outcome

</td></tr><tr><td colspan="2">

Specify the behavior of this question when the trigger conditions are met

</td></tr><tr><td>

Make the question mandatory

</td><td>

Specifies how the dynamic behavior setting affects the mandatory state of the field. Available options:

 -   No action
-   Yes
-   No


</td></tr><tr><td>

Make the question visible

</td><td>

Specifies how the dynamic behavior setting affects the visible state of the field. Available options:

 -   No action
-   Yes
-   No


</td></tr><tr><td>

Make the question read-only

</td><td>

Specifies how the dynamic behavior setting affects the read-only state of the field. Available options: -   No action
-   Yes
-   No


</td></tr><tr><td class="sub-head" colspan="2">

Value

</td></tr><tr><td colspan="2">

Specify the value that should be set for this question when the condition is met.

</td></tr><tr><td>

Do this action

</td><td>

Select any of the actions that you want to set for this question.

-   No action.
-   Clear value: Option to clear the question value.
-   Set value: Option to set a value for the question.


</td></tr><tr><td>

Set this value to the question

</td><td>

Option to set a value for the question. For example, if you have a question related to storage with the question type **Choice**, and you set the available choices of storage as 1 TB, 256 GB, and 512 GB, then this field shows these values. You can select any one of these values for the question.

 This field appears only when you select **Set value** from the Do this action list.

</td></tr><tr><td class="sub-head" colspan="2">

Field message

</td></tr><tr><td colspan="2">

Specify the type and message that should be shown under this question when the condition is met.

</td></tr><tr><td>

Set this field message type

</td><td>

Select any of these field message types.

 -   Info
-   Warning
-   Error
 **Note:** If you don’t want a message, select **None**.

</td></tr><tr><td>

Set this message under the field

</td><td>

Option to set a message that you want to show when the condition is met.

</td></tr></tbody>
</table>    4.  On the **Conditions** tab, add conditions that trigger the action on this question.

    5.  On the **Settings** tab, fill in the required information.

        |Field|Description|
        |-----|-----------|
        |Applicability|
        |Scenarios where this dynamic behavior applies|
        |Applies when the item is being requested|Option to specify if the dynamic behavior applies when the item is being requested.|
        |Applies while viewing the catalog tasks after the request is submitted|Option to specify if the dynamic behavior applies while viewing the catalog tasks after the request is submitted.|
        |Applies while viewing the requested item record after the request is submitted|Option to specify if the dynamic behavior applies while viewing the submitted record.|

    6.  Select **Add behavior**.

    **Note:** When dynamic behavior is added, a catalog UI policy and action is created and a short description is automatically generated.


**Parent Topic:**[Creating or editing catalog item template](create-cat-item-template-cat-builder.md)

