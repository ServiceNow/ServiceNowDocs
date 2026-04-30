---
title: Populate the homepage migration status table
description: The Homepage migration status table enables you to address homepage retirement and conversion. Run a scheduled workflow to populate the homepage migration status table with information about the homepages on your instance.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Homepage migration status table, Homepage deprecation, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Populate the homepage migration status table

The Homepage migration status table enables you to address homepage retirement and conversion. Run a scheduled workflow to populate the homepage migration status table with information about the homepages on your instance.

## Before you begin

Role required: admin.

The populate flow has a limit of 1000 sys\_portal\_pages per execution. You can leave the populate flow running for multiple days. The flow adds more records to the Homepage migration status table in batches of 1000.

**Note:** In domain separated instances, the flow to populate the homepage migration status table runs only on the global instance.

## Procedure

1.  Navigate to **All** &gt; **Homepage deprecation help tool** &gt; **Overview**.

2.  Select the link labeled **Populate Homepage migration status table** to open the flow that populates the table.

    ![Homepage deprecation dashboard with Populate homepage migration link outlined](../image/hpm-populate-hpm-status-link.png)

3.  In the Flow Designer, select the trigger to specify when you want the populate flow to run.

    The default trigger is daily at 23:00:00.

4.  Select **Activate**.

5.  Select **Test** to run the flow.

    ![Flow designer showing Homepage migration status table flow with the Test button outlined](../image/hpm-populate-fd.png)

6.  Select **Run Test**.

    When you see the message `Your test has finished running`, close the Test Flow window and return to the **Overview** tab.


## Result

The Overview tab of the Homepage deprecation help tool is populated with the number of homepages not deprecated.![Homepage deprecation dashboard with four homepage single score reports showing nine not deprecated and zero converted, zero retired, zero restored](../image/hp-dep-overview1.png)

