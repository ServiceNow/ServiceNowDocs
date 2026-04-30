---
title: Access MetricBase data using the list command
description: Use the list command on a table in the MetricBase database to view time-series data. The data reveals the behavior of the entity that supplies the data.
locale: en-US
release: xanadu
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Accessing MetricBase data, Defining and collecting MetricBase data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Access MetricBase data using the list command

Use the list command on a table in the MetricBase database to view time-series data. The data reveals the behavior of the entity that supplies the data.

## Before you begin

Role required: admin

## Procedure

1.  On the MetricBase instance, in the **application navigator**, type `<table-name>.list`, and press the Enter key.

    &lt;table-name&gt; is the name of the table in the MetricBase database that contains the metric you want to view.

2.  Click the menu icon \(![Menu icon](../../../product/configuration-management/image/menu-icon.png)\) above the metric column, and select **Time Series Chart**.

3.  Change the **Time Span** and **Transform** fields to evaluate the data.

4.  Adjust the data:

    1.  Select one of the transforms: **Add**, **Multiply**, or **Divide**.

    2.  In the **Value** field, enter the number to add, multiply, or divide the metric data by and click **Submit**.

        **Note:** The adjusted data is not saved in the MetricBase database.


