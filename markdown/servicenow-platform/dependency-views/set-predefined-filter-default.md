---
title: Set a predefined filter as default
description: You can set a custom predefined filter as the default predefined filter for viewing maps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/dependency-views/set-predefined-filter-default.html
release: australia
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set a predefined filter as default

You can set a custom predefined filter as the default predefined filter for viewing maps.

## Before you begin

Role required: sn\_cmdb\_admin or admin

## Procedure

1.  Create the custom predefined filter to be used as the default predefined filter.

2.  On the predefined filter form, click the context menu and select **Copy sys\_id**.

3.  Navigate to **User Administration** &gt; **User Preferences**.

4.  Click **New** and create a new user preference record using these values:

    -   **Name**: ecmdb.ciview
    -   **Type**: String
    -   **Value**: Paste the sys\_id of the custom predefined filter
    -   **User**: Leave blank to create a system-wide setting
    -   **Description**: Description of the predefined filter
    -   **System**: Selected
5.  Click **Submit**.


## What to do next

In **Map Settings**, when you select the `Default` option for **Predefined Filters**, the custom predefined filter that was set, will be applied.

**Parent Topic:**[Administer Dependency Views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map indicators]()

[Create or modify map icons]()

[Create a predefined filter]()

[Create or modify Map Related Items]()

[Create or modify Dependency Views menu actions]()

[Condition and script parameters for menu actions]()

[Create or edit a dependency type]()

[Filter the view of a Dependency Views map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/t_FilterViewNGBSMMap.md)

