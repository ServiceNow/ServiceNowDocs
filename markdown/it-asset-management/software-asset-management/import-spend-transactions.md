---
title: Import financial transactions
description: Import a Microsoft Excel spreadsheet of financial transaction data in the Software Asset Workspace to start managing software spending.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/import-spend-transactions.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management, Asset Management]
---

# Import financial transactions

Import a Microsoft Excel spreadsheet of financial transaction data in the Software Asset Workspace to start managing software spending.

## Before you begin

Role required: **sam\_user**

Have your financial transaction data ready, including vendor name, transaction description, amount, and GL account for each transaction.

**Note:** To use the AI pipeline for classifying imported transactions, install the ServiceNow Otto for Software Asset Management \(SAM\) store app. Without this store app, transactions are processed by the machine learning pipeline. For details, see [AI-powered Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md).

## Procedure

1.  Go to **Software Asset Workspace** &gt; **License operations** &gt; **Software spend detection** &gt; **Transaction imports**.

2.  Select **New**.

    The **Create New Software spend transaction import** form appears.

3.  In the **Name** field, enter a name for the import.

4.  Select **Download template**.

    The template downloads as a Microsoft Excel \(.xlsx\) file.

5.  Open the downloaded template and populate it with your financial transaction data.

    Include a value in each required column. For accurate classification results, include a GL account for every transaction.

6.  Return to the **Create New Software spend transaction import** form and select **Attach file** to upload the completed template.

7.  Select **Import**.

    The import runs and the status updates based on the outcome, such as **Completed**, **Completed with Errors**, or **Error**. The form displays counts for Total rows, Inserts, Errors, Skipped, and Ignored. A confirmation or error banner appears at the top of the form.

    The **SAM - Label Spend Transactions** scheduled job runs in the background to classify the imported transactions.


## What to do next

To see the row counts for every import, navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software spend detection** &gt; **Transaction imports**. The list view shows the total rows processed, skipped, ignored, and errored for every import. To review the transactions or errors created by a specific import, open the import record from the Transaction imports list. For details on the tabs available on an import record, see [Software Spend Detection in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-sam-workspace.md).

To review individual transaction records across all imports, navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software spend detection** &gt; **All transactions**. The list view shows every transaction record along with its assigned values.

**Parent Topic:**[Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-spend-detection.md)

**Related topics**  


[Classify and normalize software spend transactions by using ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/classify-normalize-software-spend-transactions.md)

[Software Spend Detection in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-sam-workspace.md)

[Manually create a spend transaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/manually-update-transactions.md)

