---
title: Import risk data in to a Microsoft Word
description: Import and insert data such as Risk data points and reports into a Microsoft Word report document from a ServiceNow instance. You can only import and insert the data that is configured in your reporting configurations.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating Microsoft 365 with Management Reporting of Risk, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Import risk data in to a Microsoft Word

Import and insert data such as Risk data points and reports into a Microsoft Word report document from a ServiceNow instance. You can only import and insert the data that is configured in your reporting configurations.

## Before you begin

Role required: sn\_risk\_advanced.ara\_reader

## Procedure

1.  Navigate to the Microsoft Word document in which you want to insert data.

2.  On the ribbon, select **Insert Link**.

    On the right side pane, the ServiceNow login screen appears.

3.  To log in to your ServiceNow instance, select **Log in**.

    1.  A message is displayed that states that ServiceNow Reporting will display in a new window, select **Allow**.

    2.  On the ServiceNow login screen, provide your credentials.

    3.  Select **Allow**.

4.  To insert a Risk data point from a table into the document, move the cursor at the point where you want to insert data.

    1.  Select the **Data** tab on the right side pane.

    2.  The **Business domain** field is set to **Risk**.

    3.  In the **Reporting Item** field, select the reporting configuration you want to insert.

        The additional filters dynamically appear based on the configuration record selected.

    4.  In the **Name** field, select the name of the configuration record.

    5.  In the **Value to insert** field, select the column from which you want to insert data.

    6.  Select **Add**.

5.  To insert a table into the report, move the cursor at the point where you want to insert data.

    1.  Select the **Table** tab on the right side pane.

    2.  The **Business domain** field is set to **Risk**.

    3.  In the **Reporting item** field, select the reporting configuration that you want to insert.

    4.  Select **Add**.

    The data is inserted in to the report document. The inserted text takes the formatting of the document. You can modify the formatting as required.

6.  To insert a chart, move the cursor at the point where you want to insert the chart.

    1.  Select the **Chart** tab on the right side pane.

    2.  The **Business domain** field is set to **Risk**.

    3.  In the **Reporting item** field, select the reporting configuration that you want to insert.

    4.  Select **Add**.

    The chart is inserted in to the report document. The inserted chart can be modified according to your preferences. For example, you can change the colors, the type of chart and so on.

7.  To view the details of any record that is inserted in the document, select the content control, and then select **Open link**.

    It takes you to the ServiceNow instance, where you can access the data.

8.  To view the list of all ServiceNow links that you’ve inserted in the report and obtain the latest data on the document, select **Manage Links**.

    1.  Select the check boxes for the links that you want to refresh.

    2.  Select the refresh ![Refresh icon.](../image/refresh-icon.jpg) icon.

        The data is refreshed while displaying the time of refresh and retaining the formatting of the document.

9.  To identify and highlight which content control is selected on the report, select the three vertical dots or the more actions icon.

    The content control is highlighted in the right pane.


