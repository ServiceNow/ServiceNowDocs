---
title: Check which plugin contains a required pattern
description: Since ServiceNow releases discovery patterns using two different plugins, you may need to check which plugin to install or upgrade.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Pattern Designer and related applications, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Check which plugin contains a required pattern

Since ServiceNow releases discovery patterns using two different plugins, you may need to check which plugin to install or upgrade.

## Before you begin

Role required: service\_mapping\_admin

## About this task

ServiceNow releases all discovery patterns using the following applications:

-   **Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)**

    This application provides the latest versions of discovery patterns the original version of which ServiceNow released on ServiceNow Store.

-   **Visibility Content \(sn\_pattern\_design\)**

    This application supplies the updated version of the patterns that were part of the family releases up until Tokyo.


## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  Display the **Application** column.

    1.  Click **Personalize List**.

    2.  In the Personalize List Columns dialog box, select **Application** under **Available**, and click the right arrow.

3.  You can filter out shared libraries to see only patterns in the list.

4.  Search for the relevant pattern in the list.

5.  Check to which application it belongs.

    **Global** stands for Visibility Content.

    ![View the supporting application for patterns.](../image/pattern-list-check-plugin.png)


**Parent Topic:**[Configuring Pattern Designer and related applications](../reference/configuring-pattern-designer-plugins.md)

