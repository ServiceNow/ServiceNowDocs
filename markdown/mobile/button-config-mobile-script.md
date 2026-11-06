---
title: Button condition support enablement
description: Use mobile scripts to update data across multiple tables and to control button visibility and behavior, whether users are online or offline.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/button-config-mobile-script.html
release: australia
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 1
breadcrumb: [Components that support mobile scripts, Mobile scripting in offline, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Button condition support enablement

Use mobile scripts to update data across multiple tables and to control button visibility and behavior, whether users are online or offline.

## Before you begin

Role required: mobile\_admin

## About this task

Mobile scripts can serve as the functional component behind a button condition, so button visibility and behavior can be driven by script logic when both offline and online. By default, the mobile offline capabilities for button conditions aren't enabled for existing records. You must explicitly opt in to the new Mobile Scripts framework capabilities.

**Note:** Enabling mobile scripting capabilities for offline button functions takes place in the ServiceNow AI Platform. All other button function configuration occurs in MAB. For more information, see [Configure offline mode properties for action functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/config-offline-properties-action-funct.md).

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_button.list**.

    The Functions list displays.

2.  Either select **New** to create a button record or select an existing record.

3.  In the record select the **Offline Properties**tab.

4.  Select the **Offline** option.

5.  Select the option **Enable advanced mobile scripting capabilities**.

6.  Select all other options relevant for your configuration.

7.  Select **Submit**.


**Parent Topic:**[Components that support mobile scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/components-mobile-scripts.md)

