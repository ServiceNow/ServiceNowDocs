---
title: Parametrized data item support for input form screens
description: Admins can configure parametrized data item screens that can return relevant records based on user inputs and variables on an input form screen.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Parametrized data item support for input form screens

Admins can configure parametrized data item screens that can return relevant records based on user inputs and variables on an input form screen.

## Before you begin

Role required: admin

## About this task

This configuration enables parametrized data item support for the following target screen types:

-   List screens
-   Map screens
-   Calendar screens
-   Record screens
-   Custom map screens

When you complete this configuration, the parametrized screen is populated with query results based on inputs or variables from an input form screen. In this scenario, the inputs and variables of the input form screen are used as part of a data item's query condition.

The parametrized data item screen isn’t supported [offline](../concept/mobile-offline-mode.md).

## Procedure

1.  Configure an input form screen that includes the inputs and variables that you want to use as part of the data item query condition.

    **Note:** The input form screen can contain only inputs, only variables, or both inputs and variables for use as part of the data item query condition.

    For information about creating an input form screen, see [Configure an input form screen](parameter-screen-config.md).

2.  Navigate to the target list, map, calendar, record, or custom map screen you want to use.

    For example, if you want to configure a parametrized data item list screen:

    1.  Enter `sys_sg_list_screen_.list` in the filter.
    2.  Select the list screen that you want to be parametrized.
    3.  In the **Input Form Screen** field, search for the input form screen that you created in Step 1.
    4.  Select **Update**.
    ![Instance showing list screen being configured to use input form screen.](../image/paramtrized-data-item-input-form-screen.png)

3.  Configure a parametrized data item in the sys\_sg\_data\_item table with a query condition that returns the relevant information to the target screen.

    For information about configuring a parametrized data item, see [Configure a parametrized data item](sg-config-parametrized-data-item.md).

4.  Navigate back to the target screen.

    For example, if you’re using a list screen as your target screen, enter `sys_sg_list_screen.list` in the filter and select the target list screen.

5.  Select the data item of the target screen that you created in Step 3.

6.  On the **Input Variable Parameter Mappings** tab of the target screen, select **New**.

7.  Map the inputs or variables created in the input form screen to the data parameter as shown in the following table.

    |Field|Description|
    |-----|-----------|
    |Variable|Input form screen variable|
    |Screen|Target screen. This field automatically populates.|
    |Application|Application scope. This field automatically populates.|
    |Input|Input label from the input form screen|
    |Data parameter|Data parameter from the target screen data item|

    ![Instance screen showing input variable parameter mapping.](../image/paramtrized-data-item-input-form-screen2.png)

8.  Select **Update**.


