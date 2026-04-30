---
title: Configure a dynamic segment to display selected data in a record screen
description: Configure a record screen with a dynamic screen segment so users can view records that correspond to selected segments, rather than view a complete list of records.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using dynamic segments to display data, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a dynamic segment to display selected data in a record screen

Configure a record screen with a dynamic screen segment so users can view records that correspond to selected segments, rather than view a complete list of records.

## Before you begin

When configuring a dynamic screen segment within a record screen, ensure that you have created the following items:

-   A record screen, used to include a dynamic screen segment within the segmented control. For more information, see [Configure a parameterized record screen](configure-param-form-applet.md).
-   An embedded list, used to display a list of records within the selected record screen. This list is selected from the **Dynamic segment item stream** field.
-   A corresponding list to be displayed when each screen segment is selected. This process should resemble the embedded list procedure, with the addition of using a target table to which you are referencing.

    For more information about embedded lists and the list to be displayed when a screen segment is selected, see [Embedded lists for a record screen](../concept/sg-embedded-list.md)


Role required: admin

## Procedure

1.  In the web-based UI, enter `sys_sg_form_screen.list` in the filter navigator.

2.  Select the record screen to which you want to add a dynamic screen segment.

3.  In the **Fetch Type** field, select **On-demand**.

4.  In the Segmented Control area, select the height and width of the segment buttons.

    For a guide to the button sizes, see [Using dynamic segments to display data in a record screen](../concept/dynamic-segment-form-screen.md).

5.  Right-click in the header and select **Save**.

6.  Configure the header segment to display within the segmented control.

    **Note:** The header segment is usually the initial button in the segmented control. If this option is not selected, the segmented control only displays the dynamic screen segment.

    1.  Select the**Record Screen Segments** tab and select **New**.

    2.  From the Select form segment type menu, select **Record Screen Segment**and then select **OK**.

    3.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Record Screen|This field is automatically set to the name of the selected record screen.|
        |Application|Scoped application associated with this record. This field defaults to the current application.|
        |Embedded Screen|List screen displayed when the user selects the header segment.|
        |Header Card|The header segment, which usually appears to the left of the segmented control. Example names are All tasks or All week.|
        |Order|Position where the header segment displays in the segmented control. This number must be lower than the dynamic screen segment, to ensure it is the first segment on the left.|
        |Sticky|Keeps the header segment in the same location when the user horizontally scrolls through the displayed dynamic screen segment records.|

    4.  Select **Submit**.

7.  Configure the dynamic screen segment and the records to display when users tap a segment record.

    1.  Select the **Record Screen Segments** tab and select **New**.

    2.  From the Select form segment type menu, select **Dynamic Record Screen Segment** and then select **OK**.

    3.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Record Screen|This field is automatically set to the name of the selected record screen.|
        |Application|Scoped application associated with this record. This field defaults to the current application.|
        |Dynamic screen segment list stream|An embedded list screen contained within the dynamic screen segment of the record screen.|
        |Active|Option for determining whether the dynamic screen segment is active. For this configuration, select this option.|
        |Embedded Screen|List screen that contains a list of records displayed to the user when they tap one of the segments from the dynamic screen segment.|
        |Order|The location where the dynamic screen segment displays in the segmented control. If you have defined a header segment, this number must be higher to ensure it is to the right of the header segment.|

    4.  Right-click in the header and select **Save**.

8.  While still in the Dynamic Form Segment Screen form, define the appropriate lists to display when selecting segments in the dynamic screen segment.

    1.  From the **Dynamic segment list stream** field, select the information icon \(![Information icon.](../image/gac-info-icon.png)\) and select **Open Record**.

    2.  Select the List Stream M2M Item Configuration to use for the dynamic section.

    3.  In the Item Configuration form, ensure that the user is not redirected to a different embedded screen by selecting **Use Card** and verifying that the **Embedded Screen** field is empty.

    4.  Select **Update**.


## What to do next

Define the appearance of selected segment buttons. See, [Customize segment button colors in the segmented control area](dynamic-segmented-control-config.md).

