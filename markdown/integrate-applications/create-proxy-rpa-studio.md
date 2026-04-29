---
title: Create a proxy in RPA Desktop Design Studio
description: Create a proxy at a component level in RPA Desktop Design Studio to extract the additional properties of that component.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Create a proxy in RPA Desktop Design Studio

Create a proxy at a component level in RPA Desktop Design Studio to extract the additional properties of that component.

## Before you begin

Configure a component. For more information, see [Use a component in RPA Desktop Design Studio](configure-components.md).

Role required: none

## About this task

Use the **Create Proxy** option to add or modify some functionalities of an already-existing class.

## Procedure

1.  In the RPA Desktop Design Studio, on the Design surface, right-click either the Data In or Data Out port of a component and select **Create Proxy**.

    For example, the proxy of the DateTime component appears as shown in the example.

    ![Proxy component.](../image/proxy-component.png "Proxy component")

2.  Double-click the proxy component title bar to open the CHOOSE PROPERTIES dialog box.

3.  In the CHOOSE PROPERTIES dialog box, select the applicable check boxes for the properties to be used.

    For example, select the Day and DayOfWeek properties as shown in the example.

    ![Choose properties window appears to select the applicable proxy properties.](../image/choose-properties-proxy.png "Choose Properties dialog box")

4.  Click **OK**.

    If you hover over the Data Out port of the DateTime component after executing the component, you can see the Day as 27 and the DayOfWeek as Saturday in the following examples.

    ![Day as 27 in the DateTime component.](../image/data-proxy-day.png "Day as 27 in the DateTime component")

    ![DayOfWeek as Saturday in the DateTime component.](../image/data-proxy-dayofweek.png "DayOfWeek as Saturday in the DateTime component")


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

