---
title: Configure button emphasis according to function location
description: Configure button emphasis in different locations within your mobile app to help users identify the type of functions they can activate.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Button emphasis, Legacy theming, Configuring the Mobile Platform, Mobile Platform]
---

# Configure button emphasis according to function location

Configure button emphasis in different locations within your mobile app to help users identify the type of functions they can activate.

## Before you begin

Role required: admin

**Important:** Use legacy mobile theming on Tokyo and earlier ServiceNow® instances. For Utah and later releases, see [Next Experience theming for mobile](../concept/explore-ne-theming.md).

## About this task

Button emphasis configuration is performed in web-based UI. For more information, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md). Starting from San Diego additional colors are included in the release, and button emphasis is supported in additional locations. These colors are configured in the web-based UI for the listed screen locations.

## Procedure

1.  Navigate to **All**.

2.  In the filter navigator, enter `sys_sg_button_instance.list`, to open the Function instances table.

3.  Select either a new or existing record.

4.  Select a button emphasis for the chosen function location type.

<table id="choicetable_gy3_yrp_3sb"><thead><tr><th align="left" id="d106064e119">

Function location

</th><th align="left" id="d106064e122">

Action

</th></tr></thead><tbody><tr><td id="d106064e128">

**Swipe action**

</td><td>

1.  In the **Location** field, select either **Trailing swipe** or **Leading swipe**.
2.  In the **Button emphasis** field, select either **Destructive** or **Positive**.

**Note:** If you select **None** the color is dynamically assigned based on the swipe button location. This color can be defined as either primary, secondary, or tertiary.

3.  Configure the other fields in the table as required.
4.  Select **Submit**.


</td></tr><tr><td id="d106064e178">

**Top menu action or Quick action function**

</td><td>

1.  In the **Location** field, select either **Top** or **Quick Action**
2.  In the **Button emphasis** field, select either **Destructive** or **Positive**.

**Note:** If you select **None**, the color is the primary theme color.

3.  Configure the other fields in the table as required.
4.  Select **Submit**.


</td></tr><tr><td id="d106064e227">

**Footer function or Media section**

</td><td>

1.  In the **Location** field, select **Footer**.
2.  In the **Button emphasis** field, select either **Primary**, **Destructive**, **Secondary**, or **Positive**.

**Note:** If you select **None**, the color is the primary theme color.

3.  Configure the other fields in the table as required.
4.  Select **Submit**.

![Button emphasis options for footer functions.](../image/button-emphasis-footer.png "Button emphasis options for footer functions")

</td></tr></tbody>
</table>
