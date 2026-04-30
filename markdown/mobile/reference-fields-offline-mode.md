---
title: Configure reference inputs for input form screens in offline mode
description: Configure reference inputs so that users can see a list of records in offline mode on their Mobile Agent.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Offline mode, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure reference inputs for input form screens in offline mode

Configure reference inputs so that users can see a list of records in offline mode on their Mobile Agent.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Input form screen \[sys\_sg\_parameter\_screen\]** and then either select **New** or an existing record.

5.  If you are creating a new input form screen, enter a name for the input form screen and complete the fields as required.

6.  In the Settings area, select the **Available offline** to true.

7.  In the Inputs area, select **New** and configure the input fields that your users use to enter information.

    For an explanation of the fields, see [Configure input form screen inputs](param-screen-config-inputs.md).

8.  In the Settings area, select the **Input type** for users to use within the input form screen.

9.  In the Input attributes area of the Input form, select **New** to open the Input Attribute form.

10. Select the name and value of the input attributes you want to use in offline mode.

    The options available in these fields correspond to the selection made in the **Input type** field from the Input form.

    **Note:** For a list of the attributes to use in offline mode, see [Reference field attributes for input form screens in offline mode](../reference/reference-fields-offline-attributes.md).

11. Select **Save**.


-   **[Reference field attributes for input form screens in offline mode](../reference/reference-fields-offline-attributes.md)**  
Configure the fields that you want to use and the data you want to display in offline mode by using various input attributes.

**Parent Topic:**[Offline mode](../concept/mobile-offline-mode.md)

