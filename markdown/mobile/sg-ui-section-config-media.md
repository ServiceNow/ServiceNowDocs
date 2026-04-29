---
title: Configure a media UI section
description: Configure a media UI section type to display images or videos on your launcher screen.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a media UI section

Configure a media UI section type to display images or videos on your launcher screen.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the Record type list, select **Media Section \[sys\_sg\_media\_section\]**, and then select **New**.

5.  On the form, fill in the fields.

<table id="table_xjd_n13_plb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title for your media UI section

</td></tr><tr><td>

Headline

</td><td>

Headline for the media UI section. This headline appears below your image or video.

</td></tr><tr><td>

Text

</td><td>

Text for the media UI section. This text appears below the text of your headline.

</td></tr><tr><td>

Type

</td><td>

Type of media UI section select one of the following:-   Image
-   Video


</td></tr><tr><td>

Active

</td><td>

Whether the record is active. Inactive records do not display in your app.

</td></tr><tr><td>

Media file

</td><td>

-   If you set the **Type** field to **Image**:

Select **Choose image** to select an image from your file system.

**Note:**

Create images optimized for use in media UI sections by using a height of 160px and a width of 1366px.

If your users primarily use iPhones, use a height of 160px and a width of 375px to 600px.

-   If you set the **Type** field to **Video**:

Enter the **Video URL**.

</td></tr><tr><td>

Media section function instance

</td><td>

Select the function instance that is used when a user taps on the media UI section. The label of your function appears below the text specified for the **Text** field.

 **Note:**

The selected function instance must meet the following requirements:

-   The Parent table field must contain entries, before selecting the Parent field.
-   The Parent table field must be set to **Screen Launcher**.
-   The Parent field of the selected function instance must be the launcher where you intend to add your media UI section.
-   The Location field of the function instance must be the Media UI Section.


</td></tr><tr><td>

Access control type

</td><td>

Option to assign either user role permissions or user criteria permissions for this launcher screen. For more information, see [User roles and user criteria permissions for mobile apps](../concept/roles-user-criteria.md).

</td></tr><tr><td>

Role access

</td><td>

Determines which user roles can access this launcher screen. If you have selected no roles, users with any role have access to the launcher screen.

 **Note:** This field is available when **User roles** is selected in the **Access control type** field.

</td></tr><tr><td>

User criteria access

</td><td>

Determines the criteria a user must meet to access the record on their mobile device. If you don't select any criteria, all users have access to the launcher screen.

 **Note:** This field is available when **User criteria** is selected in the **Access control type** field.

</td></tr></tbody>
</table>6.  Select **Save**.

    You have a configured media UI section that you can add to a launcher screen.

    ![Media section showing the positions of the Image/Video, headline, and text elements](../image/media-section-example.png)

7.  Add your UI section to a launcher screen:

    1.  Select the home icon to navigate to the Mobile App Builder home screen.

    2.  Select **Screens** in the menu.

    3.  Open the launcher screen record where you want to add your UI section.

    4.  In the **Launcher Sections** area, select **Choose**, then select the media UI section you created in Step 6, and then select **Apply**.

    5.  In the **Order** field, enter a number representing the order in which the UI section is displayed on the screen launcher, and then select the green check.

        UI sections appear on the launcher from the lowest order to the highest.

    6.  After you have added your media UI section, select **Save** to save the launcher screen record.


## What to do next

After creating media UI sections, you must associate the UI sections to a launcher screen so they're displayed. For more information, see [Add a UI section to the launcher screen](ui-section-to-launcher-screen.md).

