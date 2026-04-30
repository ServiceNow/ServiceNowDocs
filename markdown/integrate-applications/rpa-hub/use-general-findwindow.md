---
title: Use the Find Window component
description: Set the focus back on various windows that are inactive or running in the background as part of a Robotic Process Automation workflow in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Find Window component

Set the focus back on various windows that are inactive or running in the background as part of a Robotic Process Automation workflow in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The Find Window component identifies one or more rules associated with a Window and later uses the rules to set the focus back on the window. The component also returns the window handle of the window.

You can configure the properties for the Find Window component. For more information about these properties, see [Properties of the General components](../reference/Properties-general-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Find Window**.

2.  Drag the Find Window component to the Design surface.

3.  Click the component settings icon \(![Component settings icon](../image/component-settings-icon.png)\).

4.  Click and drag the capture window icon \(![Capture window icon.](../image/drag-window.png)\) and drop it on the window that you want to find.

    The POTENTIAL MATCH RULES window shows the rules matching the window.![Rules matching a window](../image/find-window.png)

5.  Select a rule by clicking the rule.

    **Tip:** To select more than one rule, press Shift and click the rules.

6.  In the POTENTIAL MATCH RULES window, click **OK**.

    The FIND WINDOW MATCH RULES window displays the rules matching the captured windows.

7.  In the FIND WINDOW MATCH RULES window, click **OK**.

8.  Connect the data and control ports of the Find Window component to the corresponding ports of the other components.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data in|Set Focus|Boolean|If True, the focus is set on the window else, the window continues to run in the background.|Yes|
    |Control out|Fail|Not applicable|If the component fails to execute, passes the control to the next component.|No|
    |Data out|Window Handle|Integer|Returns the window handle.|Not applicable.|

9.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[General](../concept/general-component.md)

