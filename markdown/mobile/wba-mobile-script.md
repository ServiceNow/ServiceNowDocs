---
title: Write-back action support
description: Mobile scripting can use write-back actions and write-back-action steps, so data from multiple tables can be manipulated while offline and online.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/wba-mobile-script.html
release: australia
topic_type: reference
last_updated: "2026-11-02"
reading_time_minutes: 1
breadcrumb: [Components that support mobile scripts, Mobile scripting in offline, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Write-back action support

Mobile scripting can use write-back actions and write-back-action steps, so data from multiple tables can be manipulated while offline and online.

Before the Brazil version, offline logic could only be written within a write-back action step. From the Brazil version, you can also write offline logic as a mobile script in a write-back action that runs both on offline and online.

For write-back action configuration information, see [Configure action items and action steps in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/configure-action-item-offline.md).

Consider the following offline and online considerations when using navigation commands in the ServiceNow AI Platform:

-   **Write-back actions**

    When using the navigation command sys\_sg\_write\_back\_action\_item.list it opens the Action items table. When you select **Script** in the **Type** field, the script text box opens. Add your mobile script syntax which runs both online and offline.

-   **Write-back action steps**

    When using the navigation command sys\_sg\_write\_back\_action\_step.list it opens the Action steps table. In this record a Writeback action item must be selected as it associated with its parent item. When you select **Script** in the **Type** field, you must also choose a value in the **Applicable for** field, either Online, Offline, or Both. Your choice determines which syntax to use:

    -   Online: Use regular script syntax, which supports broader GlideRecord capabilities.
    -   Offline: Use mobile script syntax only, as it is the only syntax that supports offline.
    -   Both: Use mobile script syntax only, because other scripts can’t mix mobile and non-mobile syntax.

**Parent Topic:**[Components that support mobile scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/components-mobile-scripts.md)

