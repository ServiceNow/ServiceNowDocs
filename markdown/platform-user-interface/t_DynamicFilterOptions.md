---
title: Create a dynamic filter option
description: Dynamic filter options enhance filtering by allowing users to run existing script includes or JavaScript against a reference field within condition builders and dynamic reference qualifiers.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Filter admin functions, Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a dynamic filter option

Dynamic filter options enhance filtering by allowing users to run existing script includes or JavaScript against a reference field within condition builders and dynamic reference qualifiers.

## Before you begin

Role required: admin

## About this task

This task describes how to create a new dynamic filter option and an associated [script include](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Dynamic filter options "objectize" script includes/JavaScript, enabling them to be reused in multiple [condition builders](../../common-ui-elements/concept/c_ConditionBuilder.md) and dynamic [Reference qualifiers](https://www.servicenow.com/docs/access?context=c_ReferenceQualifiers&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). This type of filter enables you to modify a script once and have the changes automatically take effect everywhere the dynamic filter option is used.

When defining a dynamic filter, you can:

-   use an existing **is \(dynamic\)** dynamic filter option \(condition builder only\)
-   use an existing dynamic filter option \(OOB or custom\)
-   create a new dynamic filter option and script include/JavaScript

All condition builder dynamic filters use the **is \(dynamic\)** operator and call a dynamic filter option. In the following example, the pre-existing dynamic filter option **Me** is being used. For a list of available pre-existing condition builder dynamic filter options, see [Dynamic operators](../reference/r_UsingTheDynamicOperator.md).

**Note:** Dynamic filters are supported in scoped applications, but they are not supported in UI policy conditions.

![Dynamic operands](../image/DynamicOperands.png "Dynamic operands")

## Procedure

1.  [Create a scripted filter](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) as a client-callable script include or business rule.

2.  Navigate to **System Definition** &gt; **Dynamic Filter Options**.

3.  Select **New**.

4.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Label|Enter a descriptive name for the dynamic filter option.|
    |Script|Enter the name of the function you created, JavaScript \(no script include needed\), or the complete script include/business rule call, such as `new GlobalCanvasUtil().refQualPaTabs()`.|
    |Field type|Select **Reference**.|
    |Referenced table|Select the table to which this dynamic filter option applies.|
    |Order|Enter a number to designate the placement of this dynamic filter option in the filter option choice list.|
    |Roles|Select the role a user must have to see this option.|
    |Active|Enable or disable the option.|
    |Reference script|Optional. Select the client-callable script include or business rule you created for the scripted filter. If the **Script** field contains JavaScript, an encoded query, or the entire script include/business rule reference, this field can be empty.|
    |Available for filter|Select this option to display the dynamic filter option as a filter breadcrumb.|
    |Available for default|Select this option to allow dynamic filter option to be a default in a dictionary entry.|
    |Available for ref qual|Select this option to allow dynamic filter option to be selected as a dynamic reference qualifier.|

    **Note:** Dynamic filters using Table API GET methods in scripts only work when using the same user configured in the basic authentication profile. To allow multiple users access to the dynamic filters, use global JavaScript APIs such as GlideRecord and GlideQuery APIs instead.

5.  Select **Submit**.


**Parent Topic:**[Filter admin functions](../concept/filter-admin-functions.md)

**Related topics**  


[Create and edit filters](t_EditingSavedFilters.md)

[Delete filters](t_DeletingFilters.md)

[Create scripted filters](t_ScriptedFilters.md)

