---
title: Define or update a component
description: Define or update a component while working in a changeset.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Viewing and editing config data, Use, DevOps Config, IT Service Management]
---

# Define or update a component

Define or update a component while working in a changeset.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_editor or cdm\_admin

## About this task

**Important:** Save your changes whenever you are confident of the changes and before you leave the **Config data** tab.

## Procedure

1.  Follow this procedure to add a component to an application:

    1.  While working in a changeset, select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for the **components** node and select **Create component**.

    2.  Enter a unique and meaningful name and then select **Create**.

2.  To perform other actions, select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for a component and select the action, as follows.

<table id="choicetable_hkz_r4h_tpb"><thead><tr><th align="left" id="d385812e127">

Selection

</th><th align="left" id="d385812e130">

Action

</th></tr></thead><tbody><tr><td id="d385812e136">

**Create component**

</td><td>

Add a component as described above.

</td></tr><tr><td id="d385812e145">

**Create CDI**

</td><td>

Add an individual config data item \(CDI\) and value to the collection. See the instructions in the next stepThe CDI can have an explicit value, or it can be a variable, override, or overlay.

-   Variable: The value for this CDI will set the value for an identically-named CDI in an included component.
-   Override: The value for this CDI will override the value for an identically-named CDI in an included component.You can also override inherited nodes from the child collection.
-   Overlay: A CDI that does not appear in any included component.


</td></tr><tr><td id="d385812e172">

**Include in collections**

</td><td>

Include the selected component in specified collections.In the Include in collections dialog box, select the collections that should include the component and then select **Include**.

 **Note:** Only collections that do not already include the component appear in the list.Inclusion of a node takes precedence over inheritance. If a node is both included and inherited, it is instead considered included.

</td></tr><tr><td id="d385812e192">

**Add file**

</td><td>

Add a file as a file node.You can attach a MIME-type file with a maximum file size of 5 MB.

For more information on adding files, see [Manage files in the config data model using file nodes](cdm-manage-file-config-data-file-node.md).

</td></tr><tr><td id="d385812e216">

**Exclude from inheritance**

</td><td>

Removes the inherited node and all child objects from the current collection.You can see excluded nodes in the changeset tree when you access the More actions menu \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) and select **View excluded data**. Excluded nodes are appended with the label "Excluded".

Select **Include in inheritance** from the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) to stop excluding the node and re-add it to the changeset.

</td></tr><tr><td id="d385812e247">

**Rename**

</td><td>

Rename the selected component.

</td></tr><tr><td id="d385812e256">

**Delete**

</td><td>

Delete the selected component.

</td></tr><tr><td id="d385812e265">

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
</table>
**Related topics**  


[Create or update a variable CDI](cdm-variables-crud.md)

[Manage files in the config data model using file nodes](cdm-manage-file-config-data-file-node.md)

[CDM data model](../reference/cdm-data-model.md)

[Viewing and editing config data](../concept/cdm-editing-config-data-changesets.md)

[How encrypted data is handled](../concept/cdm-secrets-managing.md)

