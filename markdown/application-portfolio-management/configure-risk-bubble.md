---
title: Configure script to customize risk calculation
description: Configure the risk calculation script at the extension points where the risks bubble up to the next level. With such configuration, the risk engine ignores the default logic of risk calculation and looks for the custom logic.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Configure script to customize risk calculation

Configure the risk calculation script at the extension points where the risks bubble up to the next level. With such configuration, the risk engine ignores the default logic of risk calculation and looks for the custom logic.

## Before you begin

Role required: script\_include\_admin

## About this task

There are three API extension points, at which the risks bubble up to the next level based on the script.

You can configure the script at the following levels:

-   sn\_apm.productModelCustomRiskCalculation – Product model \(hardware and software models\) risk level from the risks parameters level: The level at which the risks bubble up from the risks parameters level to the product model risk level.
-   sn\_apm.AppBusinessServicesCustomRiskCalculation – Application service risk level from the product models risk level: The level at which the risks bubble up from the product model risk level to the application service risk level.
-   sn\_apm.BusinessApplicationCustomRiskCalculation – Business application risk level from the application service risk level: The level at which the risks bubble up from the application service risk level to the business application risk level.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Filter Application Portfolio Management applications in the **Application** column.

3.  Click the API Name.

4.  Scroll down to the Implementations section and click the extension point.

5.  Click the preview this record icon \(![Information icon](../image/LegendInfoIcon.png)\) next to the **Class** field.

6.  In the Script Include pop-up, click **Open Record** button.

    By default, the sys\_id of the function returns **False** for each of the API name and the risk engine follows the APM logic in calculating the risk.

    ![Configure custom script to calculate risks at three levels of risk calculation](../image/ConfigureRiskCustomScript.png "Configure custom script to calculate risks, for example, sn_apm.AppBusinessServicesCustomRiskCalculation")

7.  Configure the function to return **True** based on the sys\_id of the API at the product model level, application service level, or business application level.

    The risk engine then calls the API for the custom logic and calculates the risk in line with this logic, which bubbles up to the next level of risk calculation.

8.  Click **Update**.


**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

