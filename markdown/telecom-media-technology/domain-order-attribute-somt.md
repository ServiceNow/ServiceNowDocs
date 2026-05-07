---
title: Define domain order attribute mappings
description: Create rules-driven attribute mappings to define the relationships and associations between and among product, service, and resource specifications, and how attribute values propagate between these mappings.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 4
breadcrumb: [Defining attribute mapping, Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Define domain order attribute mappings

Create rules-driven attribute mappings to define the relationships and associations between and among product, service, and resource specifications, and how attribute values propagate between these mappings.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_manager

## About this task

Attribute propagation enables you to define attribute mappings by setting mapping rules to do the following actions:

-   Set target and source mapping rules using conditions based on selected characteristics and characteristic options, including complex characteristics.
-   Define the attribute mapping from any specification to any other specification that is available in the product and service hierarchy. These selections include siblings and horizontal relationships.
-   Designate the same characteristic and characteristic options in both the source and target specifications, including complex characteristic hierarchies.
-   Select different characteristics and characteristic options in the source and target specifications, including complex characteristics.
-   Select a higher-level specification and lower-level specification, or a lower-level specification and a higher-level specification, in a product offering.

**Note:** If you create specification relationships and accompanying decomposition rules, the ServiceNow AI Platform performs the required validations when you attempt to create attribute mappings. These validations ensure that your attribute mappings are unique and don’t adversely impact existing decomposition rules. To learn more about specification relationships and decomposition rules, see [Create specification relationships, quantity mapping, and decomposition rules for Sales CRM for Telecommunications](create-specification-relationships-somt.md).

If a decomposition rule depends on an attribute-mapping rule, the order decomposition process isn’t able to decompose the order because it’s waiting for the attribute-mapping rule to provide the characteristic value that is required for order decomposition. The following warning appears when you save a decomposition or an attribute-mapping rule that would cause a dependent relationship with an adverse impact:`Attribute mapping rule impacts decomposition rule in {0} specification for {1} characteristic. Update this record to eliminate this rule dependency.`

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Specifications** and select a specification type.

    -   Product Specifications
    -   Service Specifications
    -   Resource Specifications
    A list of specification records is displayed.

3.  Select a record you want to modify.

4.  Navigate to the **Attribute Mappings** tab.

5.  Select **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|System-generated attribute mapping number.|
    |Target specification|Target specification that you are associating with the selected source specification and related source characteristics, and source characteristic options.|
    |Target rule|Name of the target rule, displayed after you create the mapping rules.|
    |Source rule|Name of the source rule, displayed after you create the mapping rules.|
    |Source specification|Source specification that contains the source characteristics and characteristic options to associate with the selected target specification, characteristics, and characteristic options. Based on your selection, this field auto populates the **Available columns** section with the characteristics of your selected product, service, or resource specification.|
    |Available columns|Displays one or more source characteristic options from the source specification, if available. Select the characteristics to be propagated. The characteristics display in the **Selected columns** section.|

7.  In the Conditions section, use the condition builder to specify one or more conditions using the characteristics and characteristic options selected in the Available columns for the source rule.

8.  Select **Save**.

9.  In the Available columns section, choose the target characteristics to be used as action variables in your target rule.

10. In the Actions section, select **New**.

    Fill in the dialog box to define the Configuration Rule Action.

<table id="table_q5l_md4_v3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule

</td><td>

Target rule for the attribute mapping, identified by a system-defined alpahnumeric number for the mapping.

</td></tr><tr><td>

Action variable

</td><td>

The target characteristic to be used in the rule action. In the field, select a characteristic.

</td></tr><tr><td>

Action type

</td><td>

Rule action to be performed. Select the type applicable to attribute mapping: -   Defaulting: Preselects a characteristic, option, or value, based on conditions that you specified for the target rule.
-   Exclusion: Excludes certain characteristics from the configuration because they're not applicable or invalid depending on other selections made.
-   Inclusion: Enforces the selection of certain characteristic options in a given product configuration.
-   Set value: Set the quantity on a characteristic value on a non-choice characteristic in the product configuration.
-   Validation: Checks one or more conditions


</td></tr><tr><td>

Action

</td><td>

The action to be performed for a particular characteristic. Select the field to list the available actions for the elements, such as characteristics. For example, you can: -   Copy characteristic from source
-   Select s characteristic option
-   Deselect a characteristic
-   Enable or disable a characteristic or characteristic option


</td></tr><tr><td>

Variables

</td><td>

Source characteristic that you select.

</td></tr></tbody>
</table>11. Select **Save**.


## Result

The order fulfillment process evaluates the attribute-mapping rules that you define. The attribute values are propagated from the domain orders that are associated with the source specification to the domain orders that are associated with the target specification.

## What to do next

Create and publish your offerings to a product catalog.

