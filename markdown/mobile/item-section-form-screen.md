---
title: Configure a record UI section for a record screen
description: Enrich your record screen with the addition of record UI sections displayed in a card format. This capability presents content and users can trigger actions without the need to navigate to an additional list screen.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a record UI section for a record screen

Enrich your record screen with the addition of record UI sections displayed in a card format. This capability presents content and users can trigger actions without the need to navigate to an additional list screen.

## Before you begin

At least one pre-configured record UI section must be created. For more information, see [Configure a record UI section](sg-ui-section-config-item.md).

Role required: admin

## Procedure

1.  Create a UI section screen.

    1.  In the web-based UI, enter `sys_sg_sections_screen.list` in the filter navigator.

    2.  Select **New**.

    3.  On the Item Sorting form, fill in the fields.

        1.  **Name**: Enter a title for the UI section screen.
        2.  **Icon**: Select the reference lookup icon \(![Reference lookup icon](../image/reference-lookup-icon.png)\) and select an icon from the list.

            **Note:** The icon selected is not displayed in this configuration.

        3.  **Fetch Type**: Select either `Prefetch`, `On-demand`, or `Background` as required according to your setup. For more information about these options, see [Mobile fetch types](../reference/applet-fetch-types.md).
    4.  Right-click in the header and select **Save**.

2.  Add record UI sections to the selected section screen.

    1.  Select the **Sections screen sections** tab and click **New**.

    2.  On the Sections screen sections form, fill in the fields.

        1.  **Order**: Enter a number to define where to display this record UI section.
        2.  **UI section**: Select the reference lookup icon and select a pre-configured record UI section.
        3.  **Section screen**: This field defaults to the UI section screen name you created earlier.
    3.  Select **Submit**.

3.  Map configured header and footer functions to the selected screen.

    1.  Select the **Functions instances belonging to the screen** tab and click **New**.

    2.  On the Function instance form, fill in the fields.

        1.  **Name**: Enter a title for the function.
        2.  **Function**: Select the reference lookup icon and from the menu and select a function to add to the screen.
        3.  **Label**: Enter a title for the function.
        4.  **Location**: Select either `Header` or `Footer`.
        5.  **Button emphasis**: Select an appearance for your footer function button, either `Primary`, `Secondary` or `Destructive`.
    3.  Select **Submit**.

4.  Map the record UI sections to a record screen and display it as a tab element.

    1.  Enter `sys_sg_form_screen.list` in the filter navigator.

    2.  Select the record screen to contain the record UI section.

    3.  Select the **Record screen segments** tab.

    4.  Select **New**.

    5.  From the Select record segment type menu, select **Record screen segment**and then select **OK**.

    6.  On the Record screen segment form, fill in the fields.

        1.  **Record screen**: This field defaults to the record screen you created earlier.
        2.  **Embedded Screen**: Select the embedded screen displayed when the user selects the tab within the record screen.
        3.  **Order**: Enter a number to define where to display the tab in the record screen.
    7.  Select **Submit**.


