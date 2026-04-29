---
title: Configure a content UI section
description: Use the content UI section type to display text, images, and videos as campaign cards at the top of your screen. Use these campaigns to deliver messages and important information to your users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a content UI section

Use the content UI section type to display text, images, and videos as campaign cards at the top of your screen. Use these campaigns to deliver messages and important information to your users.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the Record type list, select **Content Section \[sys\_sg\_content\_section**, and then select **New**.

5.  On the form, fill in the fields.

<table id="table_vsr_tz1_gmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

A title for the content UI section. This title is not displayed in the mobile UI.

</td></tr><tr><td>

Active

</td><td>

Select whether to display the campaign in your mobile instance.

</td></tr><tr><td>

Stream containers

</td><td>

Stream containers are a way to group item streams and show them in a content UI section carousel.

 Select **Choose** to use an existing stream container or select **New** to create one.

</td></tr><tr><td>

Access control type

</td><td>

The type of control that determines when a user can access the content section.

 Select one of the following options:

-   **User roles**

Controls access to the content section based on the roles that a user has.

-   **User criteria**

Controls access to the content section based on specific criteria a user must meet.

</td></tr><tr><td>

Role access

</td><td>

This option appears when you select **User roles** for **Acess control type**. Select **Choose** to pick a user role/

</td></tr><tr><td>

User criteria access

</td><td>

This option appears when you select **User criteria** for **Access control type**. Select **Choose** to pick a user criteria.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  Add your UI section to a launcher screen:

    1.  At the top of the Content Section form, select the more menu \(![More menu image](../image/button-more-ios.png)\), and then select **Open in platform**.

    2.  In the web UI, navigate to **System Mobile** &gt; **Launcher screens** &gt; **.**

    3.  Open the launcher screen record for the launcher where you want to add your content UI section.

    4.  Select the **Body** tab.

    5.  In the **Launcher section mappings** list, select **Insert a new row**.

        **Note:** If the **Insert a new row** link does not appear, you might not be in the same application as the launcher screen record you are editing. Switch to the appropriate application and reload the form.

    6.  In the **Order** field, enter a number representing the order in which the UI section is displayed on the launcher screen.

        UI sections appear on the launcher from the lowest order to the highest.

    7.  Press the Tab key to move to the **UI Section** field.

    8.  In the **UI Section** field, search for your content UI section, select it, and then select the green check.

    9.  After you have added your UI section, click **Update** to save the launcher screen record.


## What to do next

The content UI section you created can now contain a mobile campaign. For full instructions, see [Configure mobile campaign components](mobile-campaign-create.md).

After creating content UI sections, you must associate the UI sections to a launcher screen so they're displayed. For more information, see [Add a UI section to the launcher screen](ui-section-to-launcher-screen.md).

