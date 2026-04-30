---
title: Functionality enhancements for the entities
description: You can configure some functionality enhancements for the entities as part of the GRC updates.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Functionality enhancements for the entities

You can configure some functionality enhancements for the entities as part of the GRC updates.

The following enhancements are available for the entities:

-   Email notification: When you update the entity owner value or when you assign a new owner to an entity, an email notification is sent to the entity owner about the assignment of the entity.
-   Auto-update the entity owner: You can select the **Auto-update owner** option to keep the entity owner in synchronization with the value from its reference \(source\) field. See the following example.

    ![Auto-update the entity owner.](../../grc-common-workspace/image/auto-update-owner.png "Auto-update entity owner option")

    The **Auto-update owner** option is visible only for those entities that you have created by using the entity filter and that you have enabled by using the **Use owner field** option in the filter.

    You can also view the **Auto-update owner** option on the entity form in the workspace view. See the following example.

    ![Entity form in the workspace view.](../../grc-common-workspace/image/workspace-view-entity-form.png "Entity form in the workspace view")

-   Form design changes: The following form design changes are introduced in the entity and entity filter forms.
    -   You must fill in the **Entity class** and **Default owner** fields in the form as shown in the following example.

        ![Class and owner fields in the entity form.](../../grc-common-workspace/image/entity-class-owner-fields.png "Class and owner fields in the entity form")

    -   You must fill in the **Default owner** field even if you have cleared the **Use owner field** as shown in the following example. This update ensures that every entity that has been created has an owner assigned to it.

        ![Default owner field.](../../grc-common-workspace/image/default-owner-mandatory.png "Default owner field")

    -   The **Department** field is added to the entity form. You can add context to an entity by selecting the department, location, and class fields.
    -   The **Auto-update owner** and **Source field for owner** fields are displayed in the form. The **Source field for owner** is visible only if you have enabled the **Auto-update owner** field as shown in the following example.

        ![Source field for owner.](../../grc-common-workspace/image/entity-sync-owner-with-source-field.png "Auto-update owner and Source field for owner fields")

    -   The Activity journal displays the log of the changes that are made to the fields as shown in the following example.

        ![Activity journal.](../../grc-common-workspace/image/entity-form-activity-journal.png "Activity journal on the entity form")

    -   The new **Sync owner with source field** related link is displayed in the entity form as shown in the following example. It synchronizes the owner of an entity with its source record's field value. It is visible on the form only if the value of the source field and the owner of an entity are not in synchronization.

        ![Sync owner with source field related link.](../../grc-common-workspace/image/sync-owner-with-source-field-ui-action.png "Sync owner with source field UI action")

    -   Activate the job that synchronizes the entity owner before enabling the property. You can enable the **Frequency of syncing the entity owner with the source record** property under GRC properties to synchronize the entity owner with its source record on a daily, weekly, or monthly basis.

        Activate the job that synchronizes the entity owner before enabling the property. You can enable the **Maximum batch size while syncing the entity owner with that of its source record** property under GRC properties to set the maximum batch size to an integer value. By doing this action, you synchronize the entity owner with its source record value.


**Parent Topic:**[Exploring the entities](exploring-the-entities.md)

