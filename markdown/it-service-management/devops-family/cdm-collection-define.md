---
title: Define or update a collection in an application
description: Define or update a collection while working in a changeset of a application.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Viewing and editing config data, Using DevOps Config, DevOps Config, IT Service Management]
---

# Define or update a collectionin an application

Define or update a collection while working in a changeset of a application.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_editor or cdm\_admin

## About this task

**Important:** Save your changes whenever you are confident of the changes and before you leave the **Config data** tab.

## Procedure

1.  To add a collection to the application: While working in a changeset, select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for the **collection** node and select **Create collection**.

2.  To edit individual data items, you can either work directly in the code or select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for an item and select an action, as follows.

<table id="choicetable_hkz_r4h_tpb"><thead><tr><th align="left" id="d405134e101">

Selection

</th><th align="left" id="d405134e104">

Action

</th></tr></thead><tbody><tr><td id="d405134e110">

**Create collection**

</td><td>

Add an individual component to the collection.

</td></tr><tr><td id="d405134e119">

**Create CDI**

</td><td>

Add an individual config data item \(CDI\) and value to the collection. See the instructions in the next step.

 The CDI can have an explicit value or it can be a variable, override, or overlay.

-   Variable: The value for this CDI will set the value for an identically-named CDI in an included component.
-   Override: The value for this CDI will override the value for an identically named CDI in an included component.You can also override inherited nodes and CDIs from the child collection. Overridden nodes and CDIs are labeled as Overridden Inherited.
-   Overlay: A CDI that does not appear in any included component.


</td></tr><tr><td id="d405134e152">

**Inherit from collection**

</td><td>

Automatically inherit changes from another collection. When you select the check box and then specify a **Collection**, changes you make in the specified parent collection are reflected in all child collections.

Select **Remove inheritance** to remove the existing hereditary relationship from a collection.

**Note:** Inheritance is considered invalid when:

-   Circular, where the parent and child both inherit from each other.
-   There are more than the maximum number of collections in a chain. This number is 5 by default. Example: Collection1 is inherited by Collection2. Collection2 is inherited by Collection3. This chain of inheritance cannot continue to Collection6. You can change the valid chain length by editing the **sn\_cdm.max\_inheritance\_chain\_length** system property.


</td></tr><tr><td id="d405134e184">

**Include in deployables**

</td><td>

Include the selected collection in specified deployables.

 In the Include in deployables dialog box, select the deployables that should include the collection and then select **Include**.

 **Note:** Only deployables that do not currently include the collection appear in the list.

</td></tr><tr><td id="d405134e218">

**Rename**

</td><td>

Rename the selected collection.

</td></tr><tr><td id="d405134e227">

**Delete**

</td><td>

Delete the selected collection.

</td></tr><tr><td id="d405134e236">

**Details**

</td><td>

View the administrative information associated with the collection.

</td></tr><tr><td id="d405134e245">

**View relationships**

</td><td>

View direct relationships with the node. Direct relationships are formed between nodes by inheritance or by being included.

</td></tr></tbody>
</table>3.  Add a CDI: Select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for the item and select **Create CDI**.

<table id="table_h53_jmt_spb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name for the CDI.

</td></tr><tr><td>

Value

</td><td>

Value that the CDI has in the current context or define a variable. -   You can specify a direct `key : value` pair.
-   You can define a variable and specify its default value. Variable definitions have the following form:

    ```
@@<variableName>@@: <value>
    ```

-   You can specify a value for a variable using the following form:

    ```
"<variableName>": "<value>"
    ```

-   You can specify a contextual variable. These are variables defined out-of-the-box that use the context of the node to set the variable value. The variable uses the following form:

    ```
"<variableName>": "(#<value>#)"
    ```

-   You can use recursive variables for a CDI value. Recursive variables use other variable values as parameters to set the CDI value. For example, each of these CDI values can resolve the same due to recursive variables:

    ```
cdi1: @(favorite_food/@(person)@)@
    ```

    ```
cdi2: @(favorite_food/@(john)@)@
    ```

    ```
cdi3: waffles
    ```

</td></tr><tr><td>

Encrypted

</td><td>

Option to specify that the value of the CDI should be encrypted. This option appears only for users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role.

 After you create the CDI, the value appears in all views as `*******`. To view the value on any tab that displays the CDI, users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role can select the **View encrypted data** menu option.

</td></tr></tbody>
</table>4.  Add CDI settings that will override or overlay settings in collections.

    For more information, see [Define or update a component](cdm-component-define.md).


**Related topics**  


[CDM data model](../reference/cdm-data-model.md)

[Viewing and editing config data](../concept/cdm-editing-config-data-changesets.md)

[How encrypted data is handled](../concept/cdm-secrets-managing.md)

[Create or update a variable CDI](cdm-variables-crud.md)

