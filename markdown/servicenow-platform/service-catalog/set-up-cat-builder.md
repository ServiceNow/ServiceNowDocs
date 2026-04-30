---
title: Setting up the Catalog Builder
description: Set up the catalog item building process.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Setting up the Catalog Builder

Set up the catalog item building process.

## Before you begin

Role required: admin

## Procedure

1.  To direct users from the Catalog Builder homepage to your organization-specific catalog building process documentation, perform the following steps.

    1.  Navigate to sys\_properties.list.

    2.  Select the **glide.sc.builder.content\_url property**.

    3.  On the System Property form, in the **Value** field, specify the URL for the documentation of your choice.

        You can include both absolute and relative URLs. Following are the examples:

        -   Absolute URL: https://www.youtube.com
        -   Relative URL: sp?id=kb\_article&amp;sysparm\_article=KBXXXXXX
    4.  Click **Update**.

2.  To preview a catalog item in a specific portal, perform the following steps.

    1.  Navigate to sys\_properties.list.

    2.  Select the **glide.sc.builder.preview\_portal\_id**.

    3.  On the System Property form, in the **Value** field, specify the portal name.

        The default value is `swp`.

    4.  Click **Update**.

3.  Create or duplicate catalog item templates.

    For information on creating a template, see [Creating or editing catalog item template](create-cat-item-template-cat-builder.md).

4.  To allow users with access to a catalog item template to edit all items created using that template, perform the following steps.

    1.  Navigate to sys\_properties.list.

    2.  Select the **glide.sc.builder.template\_access**.

    3.  On the System Property form, in the **Value** field, set the value to `true`.

        The default value is `false`.

    4.  Click **Update**.

5.  Define and configure a pre-publish subflow that is triggered after submitting the catalog item in Catalog Builder.

    This subflow is run after the catalog item has been submitted but before it gets published. For example, an approval flow after submitting the edited catalog item in Catalog Builder.

    1.  Create a pre-publish subflow by specifying the following input and output parameters.

        You can also copy the Template: Catalog Builder - Item review subflow and then define your subflow. For information about subflows, see [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

        |Parameter|Type|Description|
        |---------|----|-----------|
        |catalog\_item|String|sys\_id of the draft version of the catalog item.|

<table id="table_ctr_qhd_jpb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

state

</td><td>

String

</td><td>

State of the pre-publish subflow. Possible values are:-   completed: Publishing process is triggered for the item in the **In review** state.
-   failed: Reverts the state of the item from **In review** to **Draft**.
 **Note:** The **completed** and **failed** values are case sensitive and must be selected the same way.

</td></tr></tbody>
</table>        For information about subflow field types, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    2.  Create the **glide.sc.builder.item\_review\_flow** property.

        1.  Navigate to sys\_properties.list.
        2.  Click **New**.
        3.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Unique identifier of the property. Specify**glide.sc.builder.item\_review\_flow**.|
            |Type|Type of the property. Specify **string**.|
            |Value|sys\_id of the review subflow.|

        4.  Click **Submit**.
6.  To modify the content in feedback panels for Catalog Builder steps, perform the following steps.

    1.  Navigate to sc\_wizard\_feedback.list.

    2.  From the list of catalog wizard feedbacks, select the feedback panel content that you want to edit.

    3.  On the Catalog Wizard Feedback form, in the **Content** field, edit the content.

    4.  Click **Update**.

7.  To determine which users can view and edit catalog items, specify a value in the **glide.sc.builder.item\_filter\_mode** property.

    1.  Navigate to sys\_properties.list.

    2.  Select the **glide.sc.builder.item\_filter\_mode** property.

    3.  On the System Property form, in the **Value** field, specify one of the following values:

        -   **default**: All the catalog items for which the user has read access will be displayed. When set to **default**, the user cannot edit a catalog item unless the user has write access for that item.
        -   **catalog\_editor**: All the items where the user is the catalog editor or catalog manager are displayed and can be edited.
        -   **owner\_only**: All the items for which the user is the owner are displayed and can be edited.
        **Note:** If the user has the catalog\_admin role, the user can view and edit all catalog items irrespective of what is selected in the property.


-   **[Configure a step-based service fulfillment flow](configure-flow-sf-flow.md)**  
Define service fulfillment steps while creating a catalog item in Catalog Builder.
-   **[Create a service fulfillment step type](create-sf-step-type.md)**  
Expand the coverage of service fulfillment use cases beyond those supported by step types in base system. Using a service fulfillment step type, catalog item owners can define multiple steps that are part of the request fulfilment process.
-   **[Add a step, section, or question to a catalog item wizard](configure-the-catalog-builder-experience.md)**  
Add a step, section, or question to a catalog item wizard so catalog item editors can enter custom details while creating catalog items.

**Parent Topic:**[Catalog Builder](../concept/catalog-builder.md)

