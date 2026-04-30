---
title: JavaScript connector methods
description: Execute custom JavaScript with the Execute method as part of an automation in the RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [JavaScript, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# JavaScript connector methods

Execute custom JavaScript with the Execute method as part of an automation in the RPA Desktop Design Studio.

## Execute

Executes the custom JavaScript you have written. Before executing,

-   Configure the JavaScript connector before executing the method. To configure, see [Configure the JavaScript connector](../task/configure-javascript-connector.md).
-   Configure the Execute method.

## Configure the Execute method

1.  Click the method settings icon \(![Method settings icon](../image/component-settings-icon.png)\).
2.  Select the class from the **Classes** list as set in the custom JavaScript you had written.
3.  Select the method from the **Methods** list as set in the custom JavaScript you had written.
4.  Click **OK**.

    A Data In port is created to accept the value for the function you have created.


|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Function value|Accepts the value for the function you have created.|Data in|Object|None|Yes|
|Result|Returns the output of the custom JavaScript execution.|Data out|String|None|Not applicable|

**Parent Topic:**[JavaScript](../concept/javascript.md)

