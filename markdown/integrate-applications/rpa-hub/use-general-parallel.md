---
title: Use the Parallel component
description: Execute multiple components in a sequence to perform multiple actions. The Parallel component exposes multiple threads that can execute multiple components as part of a Robotic Process Automation in the RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Parallel component

Execute multiple components in a sequence to perform multiple actions. The Parallel component exposes multiple threads that can execute multiple components as part of a Robotic Process Automation in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

For example, you can set two threads. In thread 1, the component launches the Google Chrome window with the START APP component and in thread 2, the component uses the Send Keys component to enter a URL.

You can configure the properties for the Parallel component. For more information about these properties, see [Properties of the General components](../reference/Properties-general-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **Parallel**.

2.  Drag the Parallel component to the Design surface.

3.  Click the add thread icon \(![Add thread icon](../image/add-image-icon.png)\).

    The Control Out port of the thread passes the control and executes the next component.

4.  Repeat the step to add more threads.

5.  Create multiple workflows by connecting one or more components with the threads.

6.  Connect the data and control ports of the Parallel component to the corresponding ports of the other component as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Control Out|Thread|Not applicable|Passes the control to the next component from the thread.|Yes|

    When you use the parallel component to run tasks across multiple threads, do not share the same global object instance across threads. This can cause the following issues such as:

    -   Race conditions: Concurrent access and modifications to the same object can lead to inconsistent or unpredictable results.
    -   Data corruption: Multiple threads changing shared data can overwrite or corrupt the object's state, resulting in incorrect behavior.
    -   Unexpected behavior: Without proper synchronization, actions by one thread may interfere with or conflict with those of another, causing errors or system instability.
    To ensure thread safety, create a separate instance of the object for each thread. This prevents threads from modifying shared state and ensures that each thread operates on its own independent object.

7.  To test the component, under the **DESIGN** tab, click **Run**.

    **Note:** The Send Keys and the Mouse components under the Utilities category don't work with the Parallel component.


**Parent Topic:**[General](../concept/general-component.md)

