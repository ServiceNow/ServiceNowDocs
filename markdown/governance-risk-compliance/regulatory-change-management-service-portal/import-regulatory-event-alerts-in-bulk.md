---
title: Import the regulatory event alerts in bulk
description: Populate the Workspace with your own regulatory event alerts. You can then import multiple alerts in the Regulatory Change Management application.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Import the regulatory event alerts in bulk

Populate the Workspace with your own regulatory event alerts. You can then import multiple alerts in the Regulatory Change Management application.

## About this task

Importing the regulatory alerts in bulk offers the following benefits:

-   Savings in time and efforts.
-   Reduced errors by eliminating the need to manually enter data.
-   Improved scalability and data visibility by making the data readily available irrespective of the size.
-   Enhanced data analysis and reporting to gain insights.

## Before you begin

Role required: sn\_grc\_reg\_change.admin, sn\_grc\_reg\_change.it\_admin

## About this task

Before importing the data, you must review the following checklist:

-   Ensure that you have access and privilege to import the alerts. If you do not have the right permission, the Import data link is hidden in the UI.
-   The supported file formats are  .xls and .xlsx. All file attachments should be separated from the data. Unexpected errors may occur if the .xls and .xlsx files contain special controls such as combination filters or images embedded in them.
-   Any data for the file to be imported should not be enclosed in the &lt;script&gt; &lt;/script&gt; tags.
-   Each required \(mandatory\) field must contain a value. Ensure that you do not leave any mandatory fields blank in the import file. For example, when you are importing information, each record must include a name. You cannot proceed to the next step without mapping the mandatory fields.
-   All data values displayed in the drop-down lists must exist in the corresponding fields.
-   Ensure that the first row of data \(records\) in the source file contains the column headings or field names rather than the actual data values. These column headings or field names help you to identify the data when you map new data to the existing fields in the application.

## Procedure

1.  Log in with the admin role and navigate to the **All** &gt; **Regulatory Change Management** &gt; **Regulatory Alerts** list view.

2.  Select **Download Template**.

    It downloads the prebuilt  spreadsheet  or workbook that is already  formatted, organized, and populated with data value. The Data entry sheet of the file shows the mandatory columns to be filled such as Title and Type. The Field description sheet of the template provides detailed information about each of those field attributes. For more information, see [Create regulatory event alerts manually](submit-creation-of-regulatory-event-alerts-manually.md).

    **Note:** Before you import your regulatory alerts, you must prepare the downloaded file by filing in mandatory information.

3.  Open the downloaded template and enter the title and type in the **Title** and **Type** columns.

    When you fill in all the data, the file is ready to be imported into the application. After you have  prepared  the external data file for  data import, you can begin the import process.

4.  Navigate to the Regulatory Alerts list view and select **Import alerts** to process importing the data.

    The Load Data form is displayed that guides you on how to import the alerts as shown in the example.

    ![Load Data form.](../image/load-data-form-to-import-the-alerts-file.png)

5.  In the **Import set table** field, select **Existing table**.

    You can select the data file, configure the import options, and map the import data to application fields. You must use the existing table \(Manual Alert Staging Table\) for data processing and validation.

6.  In the **Source of the import** field, select **File**.

    You can select the saved template for importing the data.

7.  Select **Submit**.

    The data importing request is processed. You can view the import status as shown in the following example.

    ![Import status.](../image/rcm-import-status.png)


## Result

The imported regulatory event alerts are assigned to the coordinator.

## What to do next

[Assess the impact of a regulatory event alert](assess-impact-of-reg-change-using-ws.md)

