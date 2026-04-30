---
title: Configure an empty state for search results
description: Configure a customized empty state for search results to provide users with information and actions to help improve their search criteria. This information will replace the default empty state that is provided for search results.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Global search for mobile, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an empty state for search results

Configure a customized empty state for search results to provide users with information and actions to help improve their search criteria. This information will replace the default empty state that is provided for search results.

## Before you begin

You should have an empty state for the following situations:

-   When a search for a term does not produce any results.
-   When a search using a navigation tab does not produce any results.

For more information, see [Configure an empty state](empty-state-default.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Create an empty state record, then use the bridge to Mobile Card Builder \(MCB\) to configure the card that is referenced by the search config:

    1.  Select **All mobile records** from the menu.
    2.  From the Record type drop-down menu, select **Empty state \[sys\_sg\_empty\_state\]** and then select **New**.
    3.  In the Empty State form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|Title for the record.|
        |Description|Optional description of the record.|
        |Active|Option for enabling the display of the card setup within the empty state. Select the toggle to make the empty state record active.|

4.  In the Card section of the Empty State form, select **New**.

    You are taken to Mobile Card Builder where you can select and configure the card for the empty state.

5.  On the Choose a card template page, search for a card template to use.

    **Note:** Any card template can be used, including custom templates. The default template for empty states is used here to demonstrate the configuration steps.

6.  Select the **Default Empty State Template** and then select **Use this card template**.

7.  In the **Card properties** dialog box, enter:

    1.  **Name** for the card.
    2.  **Short description** that will help you identify the card.
    3.  Leave the **Table** field set to **-- None --**.
    4.  Select **Save**.
8.  In the card template select the **Image** placeholder on the card, and then perform the following configurations:

    1.  Turn off the **Use mapped field** toggle.
    2.  Select **Choose image**, and then select an image from your file system.
    The selected image is inserted in your empty state card.

9.  Select the **Value** placeholder on the card, and then perform the following configurations:

    1.  From the **Field type** drop-down list, select **Static text**.
    2.  In the **Text value** box, enter the message you want to display on the screen if a search does not return any results.
    3.  Select **Save**.
    The mobile card with the image and static text might look like this:

    ![Mobile Card Builder empty state template](../image/empty-state-in-mcb.png)

10. Select the **Action** placeholder on the card, which adds a button to the screen, and then perform the following configurations:

    1.  Enter a **Label** for the button.
    2.  Under **Actions** in the menu on the side of the screen, select a **Function**.
    3.  Under **Button appearance**, select the colors for your background, text, and borders.
11. Select **Save**.

12. Select the **X** next to **Return to Mobile App Builder**.

13. In Mobile App Builder, select **Save**.


