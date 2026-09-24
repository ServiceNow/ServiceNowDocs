---
title: Managing software spend in the Software Asset Workspace
description: The Software Spend Detection feature is available in the Software Asset Workspace under License operations. Use Software Spend Detection in the Software Asset Workspace to import financial transactions, review labeled transactions, and track software spending across your organization.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/spend-detection-sam-workspace.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [software spend detection, software asset workspace, software asset management spend detection, transaction imports, all transactions]
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management, Asset Management]
---

# Managing software spend in the Software Asset Workspace

The Software Spend Detection feature is available in the Software Asset Workspace under License operations. Use Software Spend Detection in the Software Asset Workspace to import financial transactions, review labeled transactions, and track software spending across your organization.

**Important:** Starting with the Brazil release, the Software Spend Detection feature is no longer available in the Core UI. Existing imports and spend transactions that were created using the Core UI are preserved and available in the Software Asset Workspace. The Software Spend Detection Overview dashboard is also deprecated.

The Software Asset Workspace provides a unified experience for managing your software spend detection activities. Under **License operations**, the **Software spend detection** section contains two submodules that support the end-to-end spend detection workflow.

-   **Transaction imports**

    Record of every import job with its status and results.

-   **All transactions**

    Consolidated list of every spend transaction in the system, regardless of import source or state.


## Transaction imports

The **Transaction imports** list shows every import record created in Software Spend Detection. Each row shows the import name, its status, and the row counts for inserts, errors, updates, skipped rows, and ignored rows.

Use this list to monitor the outcome of an import, identify imports that completed with errors, and locate the transactions created by a specific import. Select any record to open the import and review its details, including the file that was uploaded and the transactions the import created.

Selecting an import from the list opens its record with a **Transactions** tab showing every transaction created by that import. If an import contains rows that failed to process, an **Errors** tab also appears with the source row number, error message, and the original values from the file.

To start a spend transaction import, see [Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-spend-transactions.md).

\[Omitted image "spend-detection-workspace-transaction-imports-list-view.png"\] Alt text: Transaction imports list in the Software Asset Workspace showing import jobs with their status and row counts.

## All transactions

The **All transactions** list shows every spend transaction that has been imported or manually created in the Software Asset Workspace. Use this list to review the state of each transaction, verify how it was labeled, and identify transactions that require correction.

Each row shows the transaction details from your source data along with the values assigned during labeling, such as the publisher, product, software indicator, and labeling method. Values assigned by AI, machine learning, or a user are visually distinct, so you can quickly identify which transactions need review.

The following two fields on the transaction record help you identify software purchases that aren't yet tracked in your Software Asset Management Content Library:

-   **Is software**: Indicates whether the transaction represents a software purchase.
-   **Is managed**: Indicates whether the software is already tracked in your Software Asset Management Content Library with an active software model.

Transactions where **Is software** is true and **Is managed** is false represent unmanaged software spend.

The **State** field indicates where each transaction is in the labeling process.

|Value|Description|
|-----|-----------|
|New|Default state assigned when a transaction is imported or manually created.|
|Labeled|The transaction is classified as a software purchase, and both the publisher and product are matched to existing records.|
|Partially labeled|The transaction is classified as a software purchase, and the publisher is matched, but the product isn't.|
|Manually labeled|A user manually set or updated the **Is software**, **Publisher**, or **Product** fields on the transaction.|
|Unlabeled|The labeling process couldn't classify or normalize the transaction after the maximum retry attempts.|

For details on how each state is assigned, see [AI-powered software spend detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md).

To manually create a spend transaction, see [Create a spend transaction manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/manually-update-transactions.md).

\[Omitted image "spend-detection-workspace-all-transactions-list-view.png"\] Alt text: All transactions list in the Software Asset Workspace showing spend transactions with publisher, product, state, and prediction method columns.

**Parent Topic:**[Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/software-spend-detection.md)

**Related topics**  


[Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-spend-transactions.md)

[Create a spend transaction manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/manually-update-transactions.md)

[AI-powered software spend detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md)

