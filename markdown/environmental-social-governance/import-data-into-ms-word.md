---
title: Import data in to a Microsoft Word disclosure report
description: Import and insert data and reports into a Microsoft Word disclosure report document from a ServiceNow instance. You can only import and insert the data that is configured in your reporting configurations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrating Microsoft 365 with ServiceNow reporting, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Import data in to a Microsoft Word disclosure report

Import and insert data and reports into a Microsoft Word disclosure report document from a ServiceNow instance. You can only import and insert the data that is configured in your reporting configurations.

## Before you begin

Role required: sn\_esg\_msoff\_intg.reader

## Procedure

1.  Navigate to the Microsoft Word document in which you want to insert data.

2.  On the ribbon, select **Insert Link**.

    On the right side pane, the ServiceNow log in screen appears.

3.  To log in to your ServiceNow instance, select **Log in**.

    1.  A message is displayed that states that ServiceNow Reporting will display in a new window, select **Allow**.

    2.  On the ServiceNow login screen, provide your credentials.

    3.  Select **Allow**.

4.  To insert an Operational Sustainability Management data point from a table into the document, move the cursor at the point where you want to insert data.

    1.  Select the **Data** tab on the right side pane.

    2.  The **Business domain** field is set to **Operational Sustainability Management**.

    3.  In the **Reporting Item** field, select the Microsoft 365 reporting configuration record you want to insert.

        The additional filters dynamically appear based on the configuration record selected.

    4.  In the **Value to insert** field, select the column from which you want to insert data.

    5.  Select **Add**.

5.  To insert data in HTML format move the cursor at the point where you want to insert data.

    1.  Select the **Data** tab on the right side pane.

    2.  The **Business domain** field is set to **Operational Sustainability Management**.

    3.  In the **Reporting item** field, select the configured report that you want to insert.

    4.  In the **Metric definition** field, select the Metric definition that contains the HTML content you want.

    5.  In the **Response** field, select the HTML content you want.

    6.  In the **Value to insert** field, select **Response**

    7.  Select **Add**.

    The HTML content excluding images is inserted in to the disclosure report document.

6.  To insert a report, move the cursor at the point where you want to insert data.

    1.  Select the **Table** tab on the right side pane.

    2.  The **Business domain** field is set to **Operational Sustainability Management**.

    3.  In the **Reporting item** field, select the configured report that you want to insert.

    4.  Select **Add**.

    The data is inserted in to the disclosure report document. The inserted text takes the formatting of the document. You can modify the formatting as required.

7.  To insert a chart, move the cursor at the point where you want to insert the chart.

    1.  Select the **Chart** tab on the right side pane.

    2.  The **Business domain** field is set to **Operational Sustainability Management**.

    3.  In the **Reporting item** field, select the configured report that you want to insert.

    4.  Select **Add**.

    The chart is inserted in to the disclosure report document. The inserted chart can be modified according to your preferences. For example, you can change the colors, the type of chart and so on.

8.  To copy the document ID, select the copy icon.

9.  To view the details of any record that is inserted in the document, select the content control, and then select **Open link**.

10. To view the list of all ServiceNow links that you’ve inserted in the report and obtain the latest data on the document, select **Manage Links**.

    1.  Select the check boxes for the links that you want to refresh.

    2.  Select the refresh icon.

        The data is refreshed while displaying the time of refresh and retaining the formatting of the document.

11. To identify and highlight which content control is selected on the report, select the three vertical dots or the more actions icon.

    The content control is highlighted in the right pane.

12. To create a claim to be used in the disclosure report, refer to [Create a claim from Microsoft Word](create-a-claim-from-microsoft-word.md).


-   **[Create a claim from Microsoft Word](create-a-claim-from-microsoft-word.md)**  
You can create a claim directly from Microsoft Word for use in future disclosures or reports.

**Parent Topic:**[Integrating Microsoft 365 with ServiceNow reporting](../concept/integrating-o365-with-servicenow.md)

**Related topics**  


[Add additional reporting configuration filters for a Microsoft 365 configuration record](add-additional-reporting-filters.md)

[Add related fields to a Microsoft 365 configuration record](add-related-fields-0365.md)

[Add the ServiceNow Reporting add-in into Microsoft Word](add-the-sn-esg-addin-into-ms-word.md)

