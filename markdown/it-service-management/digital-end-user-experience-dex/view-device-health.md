---
title: View device health
description: View information on battery health, storage space, top five applications by CPU and memory usage in the last hour, and the last computer restart.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/view-device-health.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Desktop Assistant, Solve issues, Digital End-User Experience, IT Service Management]
---

# View device health

View information on battery health, storage space, top five applications by CPU and memory usage in the last hour, and the last computer restart.

## Before you begin

Confirm that the DEX Desktop Assistant \[sn\_dex\_desktop\] application has been installed. For more information, see [Install Application and Device Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/install-app-device-health.md) and [Download and install Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/download-desktop-experience.md).

Role required: sn\_dex\_desktop.user or sn\_dex\_desktop.admin

## Procedure

1.  On the Desktop Assistant home page, select the **Device Health** card.

    \[Omitted image "view-device-health.png"\] Alt text: The Device Health page that provides information on battery health, storage space, top 5 applications by CPU and memory usage in the last hour, and the last computer restart.

    For more information on system activities, select **Open Activity Monitor**.

    **Note:**

    The Desktop Assistant and the macOS system report used storage differently due to different calculation methods. The Desktop Assistant includes temporary storage like cache, resulting in slightly higher usage. The `df -h` command, a standard Linux command for storage reporting, excludes cache and thus shows lower usage. This discrepancy is expected given these distinct approaches to handling storage data.

    On Windows, battery health information isn’t displayed, and you can find more details on system activities by selecting **Open Task Manager**.


