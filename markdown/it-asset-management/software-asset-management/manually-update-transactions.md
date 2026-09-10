---
title: Manually create a spend transaction
description: Manually create a spend transaction in the Software Asset Workspace to track a software purchase that is not part of a scheduled import.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/manually-update-transactions.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management, Asset Management]
---

# Manually create a spend transaction

Manually create a spend transaction in the Software Asset Workspace to track a software purchase that is not part of a scheduled import.

## Before you begin

Role required: sam\_user

## About this task

Manual creation is useful for one-off software purchases or spend records that aren't captured in your accounts payable import file. Manually created transactions appear in the All transactions list along with imported transactions.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software spend detection** &gt; **All transactions**.

2.  Select **New**.

    The **Create New Software spend transactions** form appears with the **State** field set to **New**.

3.  Under **Overview**, complete the mandatory fields.

    -   **Description**

        Enter a short description of the transaction.

    -   **Amount**

        Enter the transaction amount and select the currency.

    -   **Transaction date**

        Enter or select the date of the transaction in YYYY-MM-DD format.

4.  Complete other **Overview** fields as needed.

    Include the vendor name, GL account, source system, and transaction type. If you already know the publisher and product, select the **Is software** check box and populate the **Publisher** and **Product** fields.

5.  Expand the **More details** section and complete any organizational or employee fields.

    You can associate the transaction with a cost center, department, location, or employee record for reporting and tracking purposes.

    To exclude this transaction from being shared with the Software Asset Management Content Library team, select the **Exclude from content service** check box.

6.  Select **Save**.

    The transaction is created with the **State** field set to **New** and appears in the All transactions list. The **SAM - Label Spend Transactions** scheduled job processes the transaction on its next run.

    If you provided the valid values for **Is software**, **Publisher**, or **Product** fields during creation, the state changes to **Manually labeled** after save. For details on state values, see [AI-powered Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md).


**Parent Topic:**[Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-spend-detection.md)

**Related topics**  


[Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/import-spend-transactions.md)

[Software Spend Detection in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-sam-workspace.md)

[AI-powered Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md)

