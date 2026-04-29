---
title: Components installed with the item generation process
description: Several types of components are installed with the item generation process, including tables, scheduled jobs, and action handlers.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use the item generation process, Common GRC features, Governance, Risk, and Compliance]
---

# Components installed with the item generation process

Several types of components are installed with the item generation process, including tables, scheduled jobs, and action handlers.

The following components are installed with the item generation process in version 13.x.x.

<table id="table_cgt_f4d_ftb"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Table

</td></tr><tr><td>

Item Generation Action Event Queue table \(sn\_grc\_item\_generation\_action\_event\_queue\)

</td><td>

Table that lists the actions that are generated during the item generation process.

</td></tr><tr><td class="sub-head" colspan="2">

Scheduled job

</td></tr><tr><td>

Item generation action queue processor

</td><td>

Scheduled job to process the action queue. The job runs every five seconds by default.

</td></tr><tr><td class="sub-head" colspan="2">

Action handlers

</td></tr><tr><td>

ItemGenerationV2Action

</td><td>

Single view of all the action handlers that are used for item generation.

</td></tr><tr><td>

IGContentToEntityTypeActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Add control objectives and risk statements to the entity type.
-   Remove control objectives and risk statements from the entity type.

</td></tr><tr><td>

IGDocumentToEntityTypeActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Add policies and risk frameworks to an entity type.
-   Remove policies and risk frameworks from an entity type.

</td></tr><tr><td>

IGEntityTypeActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Activate entity type.
-   Delete entity type.
-   Deactivate entity type.

</td></tr><tr><td>

IGEntityToEntityTypeActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Add an entity to an entity type.
-   Remove an entity from an entity type.

</td></tr><tr><td>

IGContentActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Activate control objectives and risk statements.
-   Deactivate control objectives and risk statements.
-   Create control objectives and risk statements.
-   Set an auto-control create flag.
-   Add control objectives to risk statements.
-   Remove control objectives from risk statements.
-   Delete control objectives and risk statements.

</td></tr><tr><td>

IGDocumentActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Activate policies and risk frameworks.
-   Deactivate policies and risk frameworks.
-   Add control objectives and risk statements to policies and risk frameworks.
-   Delete control objectives and risk statements from policies and risk frameworks.

</td></tr><tr><td>

IGEntityActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Activate an entity.
-   Deactivate an entity.

</td></tr><tr><td>

IGContentToAddtlEntityActionHandler

</td><td>

Handler to be called when you perform one of the following actions: -   Add control objectives and risk statements to an additional entity.
-   Remove control objectives and risk statements from an additional entity.

</td></tr><tr><td>

IGItemActionHandler

</td><td>

Handler to be called when you perform one of the following actions:-   Activate an item.
-   Deactivate an item.
-   Delete an item.

</td></tr><tr><td>

IGItemToEntityActionHandler

</td><td>

Handler to be called when you perform one of the following actions:-   Add entity to item.
-   Activate entity to item.
-   Remove entity from item.
-   Deactivate entity to item.

</td></tr><tr><td>

IGItemToEntityTypeActionHandler

</td><td>

Handler to be called when you perform one of the following actions:-   Add entity type to item.
-   Remove entity type from item.

</td></tr></tbody>
</table>**Note:** For more information on the item generation process for common controls, see [the new action types in generation of items](item-gen-action-types.md#table_w4r_n4y_2wb).

## Roles and users for the new item generation process

Users with the sn\_grc.admin or sn\_risk.manager role role can access the sn\_grc\_item\_generation\_action\_event\_queue.list table in an instance and view the item generation action queue.

The compliance and risk user roles and their associated tasks that trigger the item generation process are listed in the following table.

**Note:** The compliance and risk user roles that are listed in the table are available with version 12.x.x and earlier releases.

<table id="table_wvc_11q_gtb"><thead><tr><th>

Compliance and risk user roles

</th><th>

Associated tasks

</th></tr></thead><tbody><tr><td>

-   sn\_compliance.admin
-   sn\_risk.admin

</td><td>

-   Delete policies.
-   Delete risk frameworks.
-   Delete control objectives and risk statements.
-   Delete an entity.
-   Delete an entity type.

</td></tr><tr><td>

-   sn\_compliance.manager
-   sn\_risk.manager

</td><td>

-   Associate policies or risk frameworks to an entity.
-   Delete policies or risk frameworks from an entity.
-   Associate policies or risk frameworks to an entity type.
-   Delete policies or risk frameworks from an entity type.
-   Activate an entity type.
-   Deactivate an entity type.
-   Associate an entity to an entity type.
-   Delete an entity from an entity type.
-   Add control objectives to a risk statement.
-   Delete control objectives from a risk statement.

</td></tr><tr><td>

-   sn\_compliance.manager
-   sn\_risk.manager
-   Entity owner

</td><td>

-   Activate an entity.
-   Deactivate an entity.

</td></tr><tr><td>

-   sn\_compliance.user
-   sn\_risk.user

</td><td>

-   Create control objectives and risk statements.
-   Enable the **Creates controls automatically** option.

</td></tr><tr><td>

sn\_risk.manager

</td><td>

-   Add risk statements to a risk framework.
-   Modify risk statements that are added to a risk framework.

</td></tr></tbody>
</table>**Parent Topic:**[Using the item generation process to generate controls and risks](../concept/item-generation-process.md)

