---
title: Software Spend Detection in the Software Asset Workspace
description: The Software Spend Detection feature is available in the Software Asset Workspace under License operations. Use the workspace to import financial transactions, review labeled transactions, and track software spending across your organization.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/spend-detection-sam-workspace.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management, Asset Management]
---

# Software Spend Detection in the Software Asset Workspace

The Software Spend Detection feature is available in the Software Asset Workspace under License operations. Use the workspace to import financial transactions, review labeled transactions, and track software spending across your organization.

**Important:** Starting with Australia Patch 6, the Software Spend Detection feature is no longer available in the Core UI. Existing imports and spend transactions that were created using the Core UI are preserved and available in the Software Asset Workspace. The Software Spend Detection Overview dashboard is also deprecated.

## Overview of Software Spend Detection in the workspace

The Software Asset Workspace provides a unified experience for managing your software spend detection activities. Under **License operations**, the **Software spend detection** section contains two submodules that support the end-to-end spend detection workflow.

-   **Transaction imports**

    Record of every import job with its status and results.

-   **All transactions**

    Consolidated list of every spend transaction in the system, regardless of import source or state.


## Transaction imports

The **Transaction imports** list shows every import record created in Software Spend Detection. Each row shows the import name, its status, and the row counts for inserts, errors, updates, skipped rows, and ignored rows.

Use this list to monitor the outcome of an import, identify imports that completed with errors, and locate the transactions created by a specific import. Select any record to open the import and review its details, including the file that was uploaded and the transactions the import created.

Selecting an import from the list opens its record with a **Transactions** tab showing every transaction created by that import. If an import has any errored rows, an **Errors** tab also appears with the source row number, error message, and the original values from the file.

To start an import, see [Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-spend-transactions.md).

\[Omitted image "spend-detection-workspace-transaction-imports-list-view.png"\] Alt text: Transaction imports list in the Software Asset Workspace showing import jobs with their status and row counts.

## All transactions

The **All transactions** list shows every spend transaction that has been imported or manually created in Software Spend Detection. Use this list to review the state of each transaction, verify how it was labeled, and identify transactions that require correction.

Each row shows the core transaction details from your source data along with the values assigned by Software Spend Detection, such as the publisher, product, whether the transaction represents a software purchase, and the method used to label it. Values assigned by AI, machine learning, or a user are visually distinct so you can quickly identify which transactions were processed automatically and which need review.

Two additional fields help you identify software purchases that aren't yet tracked in your Software Asset Management Content Library. The **Is software** field indicates whether the transaction represents a software purchase. The **Is managed** field indicates whether the software is already tracked in your Software Asset Management Content Library with an active software model. Transactions where **Is software** is true and **Is managed** is false represent unmanaged software spend.

The **State** field indicates where each transaction is in the labeling process. Values include **New**, **Labeled**, **Partially labeled**, **Manually labeled**, and **Unlabeled**. For details on how each state is assigned, see [AI-powered Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md).

To sort, filter, or group the list, use the controls at the top of the page. To review or edit an individual transaction, select the row. To manually create a spend transaction, see [Manually create a spend transaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/manually-update-transactions.md).

\[Omitted image "spend-detection-workspace-all-transactions-list-view.png"\] Alt text: All transactions list in the Software Asset Workspace showing spend transactions with publisher, product, state, and prediction method columns.

**Parent Topic:**[Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-spend-detection.md)

**Related topics**  


[Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-spend-transactions.md)

[Manually create a spend transaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/manually-update-transactions.md)

[AI-powered Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md)

