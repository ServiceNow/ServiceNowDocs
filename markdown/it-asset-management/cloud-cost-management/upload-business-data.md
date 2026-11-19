---
title: Upload business data for unit economics
description: Upload revenue and unit count data to populate the Unit economics dashboard in the Business Insights view. This Unit economics dashboard enables you to view unit count data across applications, departments, and business units.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/upload-business-data.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-08-13"
reading_time_minutes: 2
breadcrumb: [Use, Cloud Cost Management, IT Asset Management]
---

# Upload business data for unit economics

Upload revenue and unit count data to populate the Unit economics dashboard in the Business Insights view. This Unit economics dashboard enables you to view unit count data across applications, departments, and business units.

## Before you begin

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\]

## About this task

The Unit economics dashboard requires revenue and unit count data that you provide through file upload. The Cloud Cost Management application combines this data with cloud and non-cloud costs already in the system to calculate cost per unit, margin, and margin percentage for each business application. Download the template, complete it with your data, and import it to populate the Unit economics view.

**Note:** You can upload one file at a time. Each uploaded file creates a separate upload history record.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Upload business data**.

2.  Select **New**.

3.  Upload a business data file.

    -   If you have an existing Excel or CSV file, select **Add file** and choose a file from your device.

        **Important:** You must follow the template's column structure when uploading files; deviations will cause an error.

    -   If you don't have an existing, select **Download template** to get the template.
    The following template contains the required column structure for your business data.

    |Field|Description|
    |-----|-----------|
    |Monthly unit metric|The unit type used to measure consumption for this business application. For example, API calls and number of customers. This value appears as the unit label in the Unit economics view.|
    |Currency code|The currency code for the revenue value in this row. For example, `USD` or `EUR`.|
    |Monthly revenue|The total revenue for this business application in the specified month. This value is used to calculate margin and margin percentage.|
    |Business application|The name of the business application. The value must match a business application defined in yourCMDB.|
    |Units|The total number of units consumed for this business application in the specified month. The total cost is divided by this value to calculate cost per unit.|
    |Date|The month for which the data applies. Enter the date in the required format.|

4.  Complete the template with your business data and save the file.

5.  On the New business data upload page, select **Import**.

    You must import one file at a time.

    The Cloud Cost Management application processes the file and creates an upload history record. The upload history record shows the number of validated rows, error rows, and excluded rows.

6.  Review and resolve upload errors by selecting the upload history record.

    1.  Select **Review import errors**.

    2.  Review the rows listed under the **Errors** column to identify validation issues.

    3.  For each error row, do one of the following:

        -   **Mark as reviewed**: Edit the value in the error row inline and resubmit. If the value passes validation, the row moves to the **Validated data** tab.
        -   **Exclude**: Removes the row from processing. The upload status updates to **Completed** when no error rows remain.

## Result

Validated rows are written to the unit economics table and appear in the Unit economics dashboard in the Business insights view.

**Parent Topic:**[Using Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/using-cloud-insights.md)

**Related topics**  


[Business Insights view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/business-insights-ccm-ws.md)

