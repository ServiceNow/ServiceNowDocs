---
title: Catalog Builder
description: You can create or edit a catalog item \(catalog item or record producer\) using a visual and guided experience along with specified restrictions. The Catalog Builder experience enables you to delegate the creation and maintenance of the catalog.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog Builder

You can create or edit a catalog item \(catalog item or record producer\) using a visual and guided experience along with specified restrictions. The Catalog Builder experience enables you to delegate the creation and maintenance of the catalog.

You can also create a template that can be used to create catalog items. While creating the template, you can specify values or restrictions for items created using the template, for example, restrictions to catalogs, categories, variable types, and portal settings.

From the home page of the Catalog Builder, you can do the following:

-   Create a catalog item
-   Create a catalog item template
-   View the available catalog items
-   View the available catalog item templates
-   View catalog items that are recently updated
-   View the configured content that describes the catalog building process in your organization.

## How does the Catalog Builder work

Catalog administrator creates templates for a business or service group. The business owner or service owner gathers catalog requirements and creates catalog items from these templates. All advanced capabilities are added by the catalog administrators or developers.

## Catalog item states

A catalog item goes through various states during the item creation and maintenance process.

<table id="table_r12_k1t_h4b"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

A catalog item is in the Draft state in one of these scenarios: -   A new item is being created in Catalog Builder.
-   An existing published item has been checked out for editing in Catalog Builder. When the item is being edited, Catalog Builder checks out the item and creates a copy of the item and its associated records\(variables, UI policies, client scripts\). The item copy is in the Draft state. The published item remains in the Published state and the **Checked out** field is set to **True**. Once the editing is done and the item is submitted, the edits to the draft item are merged with the associated published item and the draft item is deleted.

 **Note:**

-   You can only edit a draft item but not a published item that has been checked out.
-   A draft item is always inactive and does not show up in the search or browse experience.
-   You cannot modify the **Active** flag of a draft item.
-   Any changes to the draft item are not available until it is submitted.

</td></tr><tr><td>

Publishing

</td><td>

A catalog item is in this transient state for a while just after its submission and before its state changes to Published. You cannot check out an item in the Publishing state.

</td></tr><tr><td>

Published

</td><td>

When a new item is submitted, the item finally moves to the Published state. This state indicates that it is the item version being used by the application and available in the catalog. When you edit a published item, it is checked out in Catalog Builder and the item’s draft copy is created.

</td></tr></tbody>
</table>## Limitations

Catalog Builder is designed to support the most common and simple use cases so that it can easily be used by business users, while the complex functionality can be added to the item in ServiceNow AI Platform by catalog administrators.

When creating a record producer in a specific scope, you can select tables in that scope and tables in other scope if the objects from the other application scope are given read and create access for selecting a record submission table. For more information on making a table accessible to other applications, see [Table design and runtime settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/r_TableApplicationAccessFields.md).

Catalog Builder does not allow creation and editing of the following entities, but they can be set in ServiceNow AI Platform either for a draft item or a published item that has not been checked out.

-   Catalog item
    -   Meta tags
    -   Execution plans. If an item is assigned an execution plan, the process engine cannot be changed in the Catalog Builder.
    -   Price settings
-   Variable settings
    -   Tool tips
    -   Advanced and dynamic reference qualifiers. If a variable has advanced or dynamic reference qualifiers, then the reference qualifier cannot be edited in the Catalog Builder.
    -   Attributes
    -   Permissions
    -   Availability
    -   Lookup label field \(defaults to lookup value field\)
    -   Lookup price fields
    -   Unique values only
    -   Always expanded help
    -   Help text
    -   Advanced reference qualifiers
-   Question types. The following questions are supported in Catalog Builder, and they are grouped into types and subtypes. For the unsupported question types, you can view the questions but not edit them:
    -   Text
        -   Single-line. This is the Single-line text variable type in ServiceNow AI Platform.
        -   Multi-line. This is the Multi-line text variable type in ServiceNow AI Platform.
        -   Rich text. This is the HTML variable type in ServiceNow AI Platform
    -   Option
        -   Check box. This is the Check box variable type in ServiceNow AI Platform.
        -   Yes/No. This is the Yes/No variable type in ServiceNow AI Platform.
    -   Choice
        -   Dropdown \(fixed values\). This is the Select Box variable type in ServiceNow AI Platform.
        -   Dropdown \(values from a table\). This is the Lookup Select Box variable type in ServiceNow AI Platform.
        -   Record reference. This is the Reference variable type in ServiceNow AI Platform.
        -   Radio. This is the Multiple Choice variable type in ServiceNow AI Platform.
        -   Multi-select. This is the List Collector variable type in ServiceNow AI Platform.
    -   Date/Time
        -   Date. This is the Date variable type in ServiceNow AI Platform.
        -   Date &amp;Time. This is the Date and time variable type in ServiceNow AI Platform.
    -   Display label
        -   Plain text. This is the Label variable type in ServiceNow AI Platform.
        -   Rich text. This is the Rich Text Label variable type in ServiceNow AI Platform
-   Catalog UI policy
    -   **On Load** field \(defaults to true\)
    -   **Script** field. When a catalog UI policy has a script, it does not show up in the question's behavior settings list in the Catalog Builder.
    -   **Reverse if false** field. By default, it is set to true.
    -   Multiple actions. When a catalog UI policy has multiple actions, it does not show up in the question's behavior settings list in the Catalog Builder.
-   For a catalog item, the questions cannot be viewed and edited in the Catalog Builder in the following scenarios:
    -   It has more than two levels of containers.
    -   It has a two-column question set or two-column container within a container.
-   Catalog client scripts
-   Data lookup rules

-   **[Setting up the Catalog Builder](../task/set-up-cat-builder.md)**  
Set up the catalog item building process.
-   **[Creating or editing catalog item template](../task/create-cat-item-template-cat-builder.md)**  
Pre-specify values or provide restrictions for attributes such as catalogs, categories, variable types, and portal settings, which are applicable during the catalog item creation or editing process. You can create a template for a catalog item or record producer.

**Parent Topic:**[Service Catalog](service-catalog.md)

**Related topics**  


[Set up a service catalog](../task/t_SetUpAServiceCatalog.md)

