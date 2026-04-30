---
title: Discover installed software data with ITOM Content Service
description: Use ITOM Content Service and ITSM Software Asset Management to discover version-less installed software that isn't discovered automatically with Software Asset Management Core or Software Asset Management Professional or file-based Discovery.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 1
breadcrumb: [ITOM Content Service, ITOM Visibility, IT Operations Management]
---

# Discover installed software data with ITOM Content Service

Use ITOM Content Service and ITSM Software Asset Management to discover version-less installed software that isn't discovered automatically with Software Asset Management Core or Software Asset Management Professional or file-based Discovery.

## Before you begin

Ensure that the following application and plugins are installed:

-   ITOM Content Service \(sn\_smart\_content\)
-   Software Asset Management Core \(com.snc.sam.core\) or Software Asset Management Professional \(com.snc.samp\)
-   File Based Discovery \(com.snc.discovery.file\_based\_discovery\)

Ensure that ITOM Content Service is active. For more information, see [Share data on ITOM Content Service](share-data-itom-content-service.md).

Ensure that the content service suggestions in the relevant category are activated. For more information, see [Enable discovery with ITOM Content Service](ics-activate-classifiers.md).

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery Smart Content** &gt; **Smart Content Categories**.

2.  Activate the relevant category.

    1.  In the **Name** column, search for the relevant category.

    2.  Double-click \(or use the keyboard shortcut\) the **Create Installed Software** column.

    3.  In the list, select **true**.

    4.  Verify the value by selecting the green check mark.


## Result

The new installed software record is created and added to the CI Software Installations list the next time Discovery runs a schedule.

**Related topics**  


[ITOM Content Service](../concept/discovery-content-services.md)

