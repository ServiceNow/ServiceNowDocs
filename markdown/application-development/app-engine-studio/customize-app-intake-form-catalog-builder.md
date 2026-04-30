---
title: Customize the App Intake form in Catalog Builder
description: Create a custom app intake experience for your organization by editing the fields and questions on the App Engine Studio \(AES\) App Intake form in Catalog Builder.Customize the App Intake form by changing the order in which questions appear.Define dynamic behavior for a question on the App Intake form based on answers to other questions.Deactivate a question from the App Intake form if it's no longer needed.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Application Intake configuration tasks, Configure Application Intake, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Customize the App Intake form in Catalog Builder

Create a custom app intake experience for your organization by editing the fields and questions on the App Engine Studio \(AES\) App Intake form in Catalog Builder.

## Before you begin

Role required: admin

## About this task

The Out of the Box variables associated with this catalog item are set to read-only. To edit the App Intake form, you must create a copy of the existing **Apply for Citizen Development** catalog item. Then, disable the original catalog item, and continue editing the **Copy of Apply for Citizen Development** catalog item. For more information, see [Copy a catalog item](https://www.servicenow.com/docs/access?context=t_DefineACatalogItem&version=yokohama&pubname=yokohama-servicenow-platform&section=t_CopyACatalogItem&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  On the **Catalog Items** tab, select the copy of the **Apply for Citizen Development** item you created.

3.  Select **Edit**.

4.  Define the questions on the App Intake form on the **Questions** tab.

    |Action|For more information|
    |------|--------------------|
    |**Insert a new question**|[Create a question for a catalog item in Catalog Builder](https://www.servicenow.com/docs/access?context=create-question-cat-builder&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|
    |**Edit an existing question**|[Edit a question in Catalog Builder](https://www.servicenow.com/docs/access?context=edit-question-cat-builder&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|
    |**Change the order of the questions**|[Change the order of the questions](customize-app-intake-form-catalog-builder.md#)|
    |**Define dynamic behavior for an existing question**|[Define dynamic behavior for an existing App Intake form question](customize-app-intake-form-catalog-builder.md#)|
    |**Deactivate or remove a question**|[Deactivate a question from the App Intake form](customize-app-intake-form-catalog-builder.md#)|

5.  Edit any other settings on the form that you want to change.

6.  On the **Review and submit** tab, review the form preview and make any needed corrections by selecting **Preview**.

7.  Save your changes.

    -   To save your changes without submitting the form, select **Save**.
    -   To submit the form, select **Submit**.

**Parent Topic:**[Application Intake configuration tasks](../reference/app-intake-config-tasks.md)

## Change the order of the questions in the App Intake form

Customize the App Intake form by changing the order in which questions appear.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  On the **Catalog Items** tab, select **Apply for Citizen Development** from the list of catalog items.

3.  Select **Edit**.

4.  On the **Questions** tab, point to the question you want to move.

5.  On the left side of the question, select the Row drag and drop gripper icon \(![Row drag and drop gripper icon](../image/drag-icon.png)\) and drag the question to a new position.


## Define dynamic behavior for an existing App Intake form question

Define dynamic behavior for a question on the App Intake form based on answers to other questions.

### Before you begin

Role required: admin

### About this task

Sometimes, if a user gives a specific answer to one question on the App Intake form, you might need a follow-up question to gather more information. For example, if you ask if they have taken any ServiceNow training, and the answer is "no", the user goes to the next visible question. If the answer is "yes", another question appears asking which training courses they have completed. Use the following steps to define this type of dynamic behavior.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  On the **Catalog Items** tab, select **Apply for Citizen Development** from the list of catalog items.

3.  Select **Edit**.

4.  On the **Questions** tab, point to the question you want to update.

5.  Select the Add dynamic behavior icon \(![Add dynamic behavior](../image/dynamic-behavior-icon.png)\) next to the question that you want to update.

6.  Select **Define new behavior**.

7.  On the **Actions** tab, specify the behavior of the question when certain conditions are met.

<table id="table_zm4_jp2_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Specify the behavior of this question when the trigger conditions are met

</td></tr><tr><td>

Make the question mandatory

</td><td>

Specifies how the dynamic behavior setting affects the mandatory state of the field, with the following options:

 -   No action
-   Yes
-   No


</td></tr><tr><td>

Make the question visible

</td><td>

Specifies how the dynamic behavior setting affects the visible state of the field, with the following options:

 -   No action
-   Yes
-   No


</td></tr><tr><td>

Make the question read-only

</td><td>

Specifies how the dynamic behavior setting affects the read-only state of the field, with the following options: -   No action
-   Yes
-   No


</td></tr><tr><td>

Clear value

</td><td>

Option to clear the question value.

</td></tr></tbody>
</table>8.  On the **Conditions** tab, specify the conditions that trigger the action on the question. For more information about building condition statements, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

9.  On the **Settings** tab, specify the scenarios where the behavior setting applies.

    |Field|Description|
    |-----|-----------|
    |Applicability|
    |Scenarios where this dynamic behavior applies|
    |Applies when the item is being requested|Option to specify if the dynamic behavior applies when the item is being requested.|
    |Applies while viewing the catalog tasks after the request is submitted|Option to specify if the dynamic behavior applies while viewing the catalog tasks after the request is submitted.|
    |Applies while viewing the requested item record after the request is submitted|Option to specify if the dynamic behavior applies while viewing the submitted record.|

10. Select **Add behavior**.


## Deactivate a question from the App Intake form

Deactivate a question from the App Intake form if it's no longer needed.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  On the **Catalog Items** tab, select **Apply for Citizen Development** from the list of catalog items.

3.  Select **Edit**.

4.  On the **Questions** tab, point to the question you want to remove.

5.  Remove the question from the form by selecting the Deactivate question icon \(![Deactivate question icon](../image/deactivate-question-icon.png)\).

6.  Select **Deactivate**.


