---
title: Add custom fields for a planning tool integration
description: Add custom fields into your planning tool integration to improve configurability and access business-specific information, which facilitates more informed decision-making.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Add custom fields for a planning tool integration

Add custom fields into your planning tool integration to improve configurability and access business-specific information, which facilitates more informed decision-making.

## Before you begin

Role required: sn\_devops.admin

## About this task

You can add custom fields to a planning tool integration by using record transformers. Create record transformers for each tool action, and add record transformer rules to map fields in your tool to fields in the DevOps data model. For example, consider a scenario where the Azure DevOps work item Id is defined as "adoid" during the import process. If you want to align it with the ServiceNow work item Id, you can achieve this by creating a record transformer for the import action. Within this transformer, you must establish rules to map the "adoid" field to the corresponding ServiceNow work item Id field. After the field mapping is created, every time an inbound event is received from Azure DevOps to bring in work items, the data will be processed through the configured transformer into the transformed payload.

**Note:** This feature is available only for the base system plan type tool integrations except for ServiceNow Agile Development 2.0.

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** &gt; **Administration**.

2.  Select **Integrations &gt; Tool integrations** from the Lists tab.

3.  Select the planning tool integration for which you want to add custom fields, and then select **Edit field mappings**. ![Tool integration record](../image/custom-fields-1.png)

    **Note:** Verify that the application scope is selected as DevOps Integrations.

4.  In the Edit field mappings page, select the **Create a record transformer** button in the Planning capability transformation section.

    **Note:** You must create a record transformer for each tool action. In this procedure, a record transformer is created for the Import action.

    1.  On the Create New Record Transformer page, select **Create transformer sequence**. ![Create New Record Transformer page](../image/custom-field-2.png)
    2.  In the Create New Record Transformer Rule Sequence page, enter the name of the rule sequence in the **Name** field, and select the type of sequence in the **Type** field. ![Create new record transformer rule sequence page](../image/custom-field-3.png)
    3.  Select **Save**.
5.  Navigate to the transformer record page, and select the **Record Transformer Rules** tab, and then select **New**. ![Record Transformer Rules tab in the record transformer record](../image/custom-field-4.png)

6.  In the Create New Record Transformer Rule page, fill in the following fields. ![Create new record transformer rule page](../image/custom-field-5.png)

    |Field|Description|
    |-----|-----------|
    |Name|Name of the rule in the sequence.|
    |Symbol|Name of the field in the transformed payload to where the custom field value is extracted to.|
    |Path|Payload path from where the custom field value is retrieved.|
    |Order|Order in which the rule must be run in the sequence.|
    |Description|Text explaining the rule.|

    **Note:** Multiple rules can also be added to a custom column from the JSON payload and more fields can be mapped. All the transformations added are considered in the transformed payload.

7.  Select **Save**.

8.  Navigate to the Details section of the transformer record, and fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the record transformer.|
    |Base Path|Path to read from for the incoming payload.|
    |Description|Text explaining the record transformer.|
    |Record Path|Path to write to for the transformed payload.|
    |Record Transformer Rule Sequence|Rule sequence that you want to associate with this record transformer.|
    |Active|Option to make the record transformer active.|

9.  Select **Save**.

10. Navigate to the **Edit field mappings** page and select **Add mapping**. ![Edit field mappings page](../image/custom-field-6.png)

    1.  Select the record transformer for the tool action.
    2.  Set the sequence in which the mapping of the record is processed in the **Order** field.
    3.  Select a symbol if you want to map the record transformer to different entities.

        **Note:** The Symbol field here is different from the Symbol field in the Create New Record Transformer Rule form in step 6.

    4.  Select **Save**.
    **Note:** You can add multiple field mappings for an action as per your requirement.


**Parent Topic:**[User-created integrations in DevOps Change Velocity](../concept/dev-ops-tool-integration.md)

**Related topics**  


[Transformer - Scoped, Global](https://www.servicenow.com/docs/access?context=TransformerScriptedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

