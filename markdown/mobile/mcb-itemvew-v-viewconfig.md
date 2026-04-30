---
title: Understanding mobile cards and legacy cards
description: Learn the differences between cards and legacy cards, and how to work with each type in Mobile Card Builder.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile Card Builder, Mobile app building tools, Building mobile apps, Mobile Platform]
---

# Understanding mobile cards and legacy cards

Learn the differences between cards and legacy cards, and how to work with each type in Mobile Card Builder.

-   **View configuration-based cards**

    Screens created in Quebec and later releases have mobile cards based on view configurations. These cards have greater flexibility, and can take advantage of card templates. More details on this type are given in the next section.

-   **Item view-based cards**

    Mobile applets created in Paris and earlier releases have mobile cards based on item views. These legacy cards can still be edited using Mobile Card Builder, but have some limitations, as described in the next section.


## Editing cards

Cards take advantage of templates to make creating your mobile cards faster and easier.

-   **Editing card templates**

    Card templates define the layout of the fields on your mobile card, as well as any display properties that affect how your card looks. To change the look or appearance of your card, you must edit its template rather than the card itself. The options to add or remove elements and select containers are not available when editing cards. For detail on templates, see [Create a card template with Mobile Card Builder](../task/mcb-create-template.md).

-   **Editing cards**

    After you have assigned a template to your card, you can edit the card in Mobile Card Builder. Here you define what information to display in the fields laid out in your selected template. For detail on this process, see [Assign field values to your mobile card](../task/mcb-assign-fields.md).


.

## Editing legacy cards

Legacy cards can be edited as described in [Mobile Card Builder user interface](mcb-stage-ui.md), with the following exceptions:

-   **Templates are not available**

    You cannot assign a card template to legacy cards. Templates that use cards, and are not compatible with legacy cards. This option appears disabled in the menu for this card type.

-   **Reset stage option is not available**

    The **Reset stage** option, which removes all elements from the current mobile card is not available for legacy cards. This option appears disabled in the menu for this card type.


Legacy cards do not have a separate template to modify. You are able to modify containers, add or remove fields, and make other changes to the card appearance directly in the mobile card rather than in a separate template record.

