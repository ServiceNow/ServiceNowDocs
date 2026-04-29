---
title: Properties of Actions \(UI\) components
description: Learn about the properties of the Actions \(UI\) group components. All components under the Actions \(UI\) group have both unique and common properties.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Properties of Actions \(UI\) components

Learn about the properties of the Actions \(UI\) group components. All components under the Actions \(UI\) group have both unique and common properties.

|Property|Description|
|--------|-----------|
|Delay after execution|Option to specify a delay in seconds after the component executes. The automation will wait until the specified time elapses before executing the next component.|
|Delay before execution|Option to specify a delay in seconds before the component executes. The automation will wait until the specified time elapses before executing the component.|
|Name|Name of the component.|
|X|Location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) on the component along the X-axis.|
|Y|Location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) on the component along the Y-axis.|
|Enable Timeout|Option to set a timeout value.|
|Timeout|Number of seconds that the operation ends after if not completed. To apply this value, you must set the **Enable Timeout** property.|
|Scaled Search|Option to specify whether the component will scale the target image before trying to match the source image. The scaling is done in an increment of 10% each between 100% and 150%. The default option is False.|
|Search As Gray Scale Image|Option to define and search the captured area as a grayscale image. By default, the option is enabled.|
|Target Platform|Option to select the application platform.|
|Threshold|Specifies the accuracy in matching the image captured before the component performs an action. The value of 1 defines a 100% match while 0.5 defines 50% match. The default value is 0.9 or 90% match.|
|Max Wait Time in Seconds|Defines the number of seconds to wait for the image or application to appear on the screen.|
|Wait After Image Found|Specifies the wait time \(in seconds\) after the image or application appears on the screen.|
|Wait For Create|Option to specify if the component will wait for the image to appear on the screen. The default value is True.|

**Parent Topic:**[Actions \(UI\)](../concept/actions-ui.md)

