---
title: Create a card template with Mobile Card Builder
description: Use Mobile Card Builder to create a card template to use for cards in your mobile screens.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile Card Builder, Building tools, Building mobile apps, Mobile Platform]
---

# Create a card template with Mobile Card Builder

Use Mobile Card Builder to create a card template to use for cards in your mobile screens.

## Before you begin

Role required: admin or delegated developer

For more information about the delegated developer role, see [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

## About this task

**Note:** Use these steps to create a new card template from scratch, and then associate the new card template to an existing screen. Card templates can only be applied to screens created in Quebec of later releases using mobile card views.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Card Builder**.

2.  In the open screen pop-up, select **Create blank template** button in the upper right corner.

    The **Template properties** pop-up window displays.

3.  In the **Name** field, enter a name for your card template.

4.  In the **Short description** field, enter a description of your card template.

    Use your short description to indicate the type of record best suited to your card template, for example, incidents, or user records.

5.  Select **Save**.

    The Mobile Card Builder opens, displaying an empty mobile card.

    ![Mobile Card Builder with a blank card template.](../image/mcb-blank-template.png)

6.  Add elements to your card template using the card builder interface.

    For details on using the card builder UI, see [Mobile Card Builder user interface](../reference/mcb-stage-ui.md)

7.  Open the screen where you want to apply your card template by using the following methods.

    1.  Open Card builder from the web-based UI.
    2.  In Card builder, select **Menu** &gt; **Open**.
    3.  Use the **Application** and **Screen** lists to select your screen, then select the **Open** button in the bottom-right corner of the window.
8.  To apply your card template to the screen, select **Menu** &gt; **Change Template**.

9.  If you want to assign field values to your card, you can do that at this point.

    For details on that process, see [Assign field values to your mobile card](mcb-assign-fields.md).

10. Select **Save**.


