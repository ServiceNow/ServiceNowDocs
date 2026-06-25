---
title: Discover installed software data with ITOM Content Service
description: Use ITOM Content Service and ITSM Software Asset Management to discover version-less installed software that isn't discovered automatically with Software Asset Management Core or Software Asset Management Professional or file-based Discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/ics-sam-create-installed-software-record.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-03-12"
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

Ensure that ITOM Content Service is active. For more information, see [Share data on ITOM Content Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/share-data-itom-content-service.md).

Ensure that the content service suggestions in the relevant category are activated. For more information, see [Enable discovery with ITOM Content Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/ics-activate-classifiers.md).

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


[ITOM Content Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/discovery-content-services.md)

