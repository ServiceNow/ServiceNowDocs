---
title: Create advanced log alert filters
description: Add advanced log alert filters to scan alerts for conditions that you specify. The filters reduce noise by dropping alerts that do not indicate a significant issue. While developing a filter, you can test, update, publish, or activate the filter at any time.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reducing noise by using advanced log alert filters, Using Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Create advanced log alert filters

Add advanced log alert filters to scan alerts for conditions that you specify. The filters reduce noise by dropping alerts that do not indicate a significant issue. While developing a filter, you can test, update, publish, or activate the filter at any time.

## Before you begin

Role required: admin

The Disable Alert Rule Engine feature and the Disable Detection Rule Engine feature must be in the OFF state. You set the values by navigating to **Health Log Analytics** &gt; **Health Predictive AI Ops Administration** &gt; **Features**.

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Navigate to **Health Log Analytics** &gt; **Log Anomaly Detection** &gt; **Advanced Log Alert Filter**.

2.  Select **New**.

3.  Enter a unique and descriptive name for the filter.

4.  Enter a description of the operation of the filter.

5.  In the **Script template** field, select the script that most closely matches your intended logic.

    The template can act as a starting point for your custom script code.

    After you select a template, the Custom JS function text box is populated with the appropriate JavaScript function. The JavaScript function applies the filter to the alert payload data and either allows or drops the alert. The alert payload is the text and metadata for the kind of alert that the filter will analyze.

6.  Save the record by selecting **Submit**.

    To continue modifying the filter, you must reopen the record from the [filters list](hla-op-search-queries-manage.md). You can then edit, test, publish, and activate the filter.

7.  Edit the default **Alert payload** text in preparation for testing your intended logic.

    To remove your changes and revert to the default text for the Alert payload text box, click **Reset**.

    For your convenience, Health Log Analytics provides sample alerts with preconfigured payloads. Select a sample alert in the **Example alert** field to display its payload in the Alert payload text box.

8.  Save the current values of the filter without testing by selecting **Update**.

9.  When your content for the alert payload and your JavaScript function are complete, select **Test**.

    To simulate the alert operation, the system saves the filter values, applies the filter to the **Alert payload** text, and then displays one of the following results:

    -   `Alert will be dropped.`
    -   `Alert will be allowed.`
    ![Testing the JavaScript to determine whether to allow or drop the alert.](../image/advanced-alert-filter-process1.png "Testing the JavaScript to determine whether to allow or drop the alert")

    **Note:** If your new JavaScript function is not behaving as expected, you can revert to the last published one by selecting the **Revert JS Function** related link.

10. Repeat the process of updating the alert payload and testing the JavaScript function as often as needed.

11. When you are satisfied with the filter, save its values and determine whether to apply it to the log stream.

    -   To save the values and apply the filter to the log stream, make sure the **Active** check box is selected and select **Publish**.
    -   To save the filter without applying it to the log stream, clear the **Active** check box and select **Publish.**
    **Note:** If you modify a published filter, you must publish the modified filter to apply it to the log stream.


## Result

The values of the active filter are saved. If you selected the Active option, the filter is applied to the log stream.

**Parent Topic:**[Reducing noise by using advanced log alert filters](../concept/hla-op-adv-alert-filtering.md)

