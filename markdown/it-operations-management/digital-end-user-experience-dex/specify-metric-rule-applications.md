---
title: Specify the configuration item for a metric rule
description: Choose an application or device and define filter conditions for the metric rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/specify-metric-rule-applications.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 2
keywords: [metric rule ci, configuration item, metric rule filter, zscore]
breadcrumb: [DEX metric rule creation, Managing alert rules, Configure, Digital End-User Experience, IT Operations Management]
---

# Specify the configuration item for a metric rule

Choose an application or device and define filter conditions for the metric rule.

## Before you begin

Confirm that the DEX plugin \(sn\_dex\) is installed.

Role required: sn\_dex.admin

## Procedure

1.  In the primary navigation pane, select the DEX Administration icon \(\[Omitted image "icon-administration.png"\] Alt text:\).

2.  Select **Configure** on the Alert rules card.

    The list of alert rules appears.

3.  Select **Create new rule** &gt; **Metric rule**.

    A new tab opens for the Create metric rule window, with the **Select the CI** option preselected in the navigation pane.

4.  Select one of the following types of configuration items that you want to monitor.

    -   Device
    -   Saas/web application
    -   Installed application \(.exe, .app, and so on\)
5.  For **Saas/web application** or **Installed application**, select the application to monitor.

    **Note:** If you select **Device**, the option to choose an application isn’t available.

6.  Select the **Applicable for Non-persistent VDIs** toggle switch to apply this metric rule to all the non-persistent virtual desktop infrastructures \(VDIs\).

    **Note:** When this toggle switch is on, only the **Location** option is available in the **Apply filtering for devices** field.

7.  Apply conditional filtering on the configuration items.

    The predetermined filtering choices include Device, Department, Location, OS, User, and Version, with the Version option available for installed applications.

    To add more filters, select **+ New condition set**.

    **Note:**

    -   You can filter by selecting any available column from the Device \(`cmdb_ci_computer`\) or User \(`sys_user`\) tables. After a column is used as a filtering condition in any metric rule, it automatically becomes an enriched field.
    -   Enriched fields are already synced to end-user devices. However, if you select a non-enriched field as a filter condition, the data might take up to 24 hours to sync across all devices.
    -   You can select up to 15 non-enriched fields beyond the default enriched values.
8.  Select **Next**.

    The **Add criteria** option is selected in the navigation pane.

    -   Static metric rule: This metric rule processes real-time data. Lists all metric rules that are stored on the server.
    -   Zscore \(Running average\): Zscore is a measurement that indicates how many deviations a data point is away from the mean value of its dataset. It’s a dynamic value specific for each device or user. Data is evaluated from the end-user computer. Data from the last 7 days is collected. The default values are 5 to -5.

        **Note:** When you select Zscore, the alert is triggered only for the sampled value. Alerts for the average of sample are not available.


## What to do next

For the next step, see [Define alert criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/define-alert-metric-criteria.md).

