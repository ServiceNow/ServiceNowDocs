---
title: Create or update a variable CDI
description: Define variables and set their values in components, collections, and deployables.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Viewing and editing config data, Use, DevOps Config, IT Service Management]
---

# Create or update a variable CDI

Define variables and set their values in components, collections, and deployables.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_editor or cdm\_admin

## About this task

**Important:** Save your changes whenever you are confident of the changes and before you leave the **Config data** tab.

-   When you create an application, the system auto-generates an empty **vars** folder in each of the three top-level folders: **component**, **collection**, and **deployable**.
-   When you add a collection or deployable, the system adds an empty **vars** folder to the item that you created.
-   A **vars** folder can contain only variable CDIs or folders. Any subfolder can contain only variables or folders.
-   The value of a variable in a collection overrides the value of the variable in a component.
-   The value of a variable in a deployable overrides the value of the variable in a collection or component.

## Procedure

1.  Use either of the following methods to edit or add an instance of a variable while working in a changeset:

    -   Edit directly in the editing panel. Use the following format to set the value of a variable:

        ```
        "<variableName>": "<value>"
        ```

        In this example, the **dbName** variable and several others reside in the **database** folder. In addition, the **backup** folder \(a child of the **database** folder\) holds the **dbServer** variable.

        ![A var folder and its contents](../image/cdm-var-folder-example.png)

    -   Create the variable in a dialog box. Follow the procedure in the next step.
2.  Select the more actions menu icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) for the appropriate **vars** folder, select **Create variable**, and then specify its settings.

<table id="table_prr_pzv_1qb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name for the variable.

</td></tr><tr><td>

Value

</td><td>

Value that the variable has in the current context.

 **Tip:** It is often useful to define a default value for a variable in a component or collection. This is a powerful strategy because you can create a broad variety of deployables from a small set of components and collections. Deployables that inherit a component or collection can use overrides, overlays, and variable settings to meet the needs of the environment type. For example, the `Development` deployable can use the same components and collections as the `Test` deployable. `Development` uses the default *database* variable value. `Test`, in contrast, uses a different value that is appropriate for the test environment.

</td></tr><tr><td>

Encrypted

</td><td>

Option to specify that the value of the variable should be encrypted. The option appears only for users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role.

 After you create the variable, the value appears in all views as `*******`. To view the value on any tab that displays the variable, users with the CDM Secrets \[sn\_cdm.cdm\_secrets\] role can select the **View encrypted data** menu option.

</td></tr></tbody>
</table>
