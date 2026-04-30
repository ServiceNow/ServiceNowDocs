---
title: Add an audience to your UI Builder page
description: Add one or more audiences to your page or page variant.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add an audience to your UI Builder page

Add one or more audiences to your page or page variant.

## Before you begin

Role required: admin

The **glide.ux.user\_criteria\_enabled** property needs to be set to **true** to configure access for users based on role, department, group, location, or company. See [Enable the user criteria property](enable-user-criteria-property.md), for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open the experience with the page that you want to edit.

3.  Select **Settings** next to the page variant that you want to edit.

    ![Arrow pointing to variant settings link to edit page variant settings.](../image/audience-settings.png)

4.  In the page variant settings window, select **Edit all audiences**.

    ![Arrow pointing to edit all audiences link to add or edit audiences.](../image/audience-edit-all.png)

5.  Click **+ Add**.

    ![Arrow pointing at the add audience button.](../image/audience-add-link.png)

6.  Select an audience in the audience field.

    ![Audience field expanded to show list of available audiences.](../image/audience-select.png)

    **Note:** If an audience you need is not listed, you can choose the **Open audiences in platform** link to create one.

7.  Set the order of the audiences.

    **Note:** To give higher priority to an audience, enter a lower number. If a user is part of multiple audiences, the audience with the highest priority is used.

8.  Check **Active** if you want the audience to be able view the page.

9.  Select **Save**.

    The audience displays in the **Audiences** list.

    ![Specified audiences displayed in the audiences list.](../image/audience-result.png)

10. Select **Done**.


-   **[Enable the user criteria property](enable-user-criteria-property.md)**  
Enable the user criteria property to configure access for users based on role, department, group, location, or company in UI Builder.

**Parent Topic:**[Manage UI Builder pages and page variants](../concept/work-pages.md)

