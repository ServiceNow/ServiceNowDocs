---
title: Configure a card descriptive element for input form screens
description: Add a card descriptive element before an input ﬁeld, within an input form screen. This additional on-screen information provides a context to your users, enabling them to better understand what is required as they enter data into an input form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure descriptive elements, Data sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a card descriptive element for input form screens

Add a card descriptive element before an input ﬁeld, within an input form screen. This additional on-screen information provides a context to your users, enabling them to better understand what is required as they enter data into an input form.

## Before you begin

**Note:** Card descriptive elements are configured in the ServiceNow AI Platform, whereas image, text and rich text descriptive elements are configured in the Mobile App Builder. For the configuration of image, text, or rich text descriptive elements see, [Configure descriptive elements for input form screens](descriptive-elements-script.md).

Role required: admin

To use a mobile card within a descriptive element, a mobile card must be configured. For more information, see [Mobile Card Builder](../concept/mobile-card-builder.md).

When using a preconfigured mobile card, consider the following:

-   If the card you select for the descriptive element contains a button, the button text is visible, but the button isn't enabled.
-   If the card you select for the descriptive element contains an image, the image doesn't display.
-   The card you use from the Card \[sys\_sg\_view\_config\] table must be set to **Active**, so that the text elements defined in the text slots display.

## About this task

<table id="table_sw1_f1b_cgc"><tbody><tr><td>

You can add card descriptive elements to input ﬁelds, sections that contain input ﬁelds, or input form sections without any inputs. Descriptive elements can be a selection of simple text, rich text, an image or a mobile card that precedes an input. This topic deals with the configuration of descriptive element of type card. For the configuration of image, text, or rich text descriptive elements see, [Configure descriptive elements for input form screens](descriptive-elements-script.md).

</td><td>

![Input form screen with a card descriptive element at the top.](../image/desc-element-card.png)

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_descriptive\_element.list**.

2.  Select **New** in the Descriptive element list.

3.  In the **Name** field, enter a unique name for your descriptive element.

4.  In the **Label** field, enter a name that displays above your descriptive element.

5.  In the **Type** field, select **Card**.

6.  In the **Parent table** field, either select:

    -   **Input** for the card to precede the input.
    -   **Input form section** for the card to exist within the specific section.
7.  In the **Parent** field, select an input or input section that is on your input form screen by selecting the lookup \(![Reference lookup icon.](../image/reference-lookup-icon.png)\) icon.

8.  Select the relevant input and then select **OK**.

9.  In the Attributes area of the Descriptive element list, enter the name `ViewId` in the **Name** column.

10. Enter the ViewId of the card in the **Value** column.

    **Note:** The ViewId is the sys\_id of your view config record.

    To obtain the ViewId of your card, do the following.

    1.  Navigate to **All** &gt; **sys\_sg\_view\_config.list**.
    2.  Select the card that you want to display as a descriptive element.
    3.  Select and hold \(or right-click\) the menu icon \(![Context menu icon.](../image/mobile-more-icon.png)\) and then select **Copy sys\_id**.
    4.  Paste the sys\_id into the **Value** column.
11. Select **Update**.


