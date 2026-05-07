---
title: Customize details displayed on node map tiles using a decision table
description: Customize the details displayed on the node map tiles in the Lead-to-Cash Process Management using Decision Tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing the sales process dashboard, Lead-to-Cash Process Management, Order operations apps, Configure, Sales Customer Relationship Management]
---

# Customize details displayed on node map tiles using a decision table

Customize the details displayed on the node map tiles in the Lead-to-Cash Process Management using Decision Tables.

## Before you begin

Role required: admin

## About this task

You can add more columns to display additional lines. However, this would require you to make code changes in the UI Builder.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  In the **Name** field of the system properties table, search for and select the Business object type configuration decision table.

    You are redirected to the decision table in Workflow Studio.

3.  Change the values in the **Field 1** and **Field 2** columns depending on the information you want to display in the node map tile.

4.  Change the icon for the tile.

    1.  Access the [Icon Gallery](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-icon/gallery) to obtain the icon name corresponding to the icon you want to use.

    2.  Enter the icon name in the **Node Icon** field.

5.  Add decision rows for any additional business entities you created.

6.  Verify the changes by selecting **Test**.

7.  Select **Save**.


**Parent Topic:**[Customizing the sales process dashboard](../concept/customizing-sales-process-dashboard.md)

