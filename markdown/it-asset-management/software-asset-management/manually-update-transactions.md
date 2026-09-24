---
title: Create a spend transaction manually
description: Create spend transactions for one-off software purchases or spend records that are not captured in your accounts payable import file. This allows you to track all software spending in one location.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/manually-update-transactions.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [software spend detection, software asset management software spend detection, spend transaction manual, SAM - Label Spend Transactions, License operations]
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management, Asset Management]
---

# Create a spend transaction manually

Create spend transactions for one-off software purchases or spend records that are not captured in your accounts payable import file. This allows you to track all software spending in one location.

## Before you begin

Role required: sam\_user

## About this task

The **SAM - Label Spend Transactions** scheduled job processes manual transactions during its next run.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software spend detection** &gt; **All transactions**.

2.  Select **New**.

3.  On the **Create New Software spend transactions** form, fill in the fields.

    For a description of the field values, see [Software spend transaction fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/software-spend-transaction-fields.md).

4.  If you already know the publisher and product for the transaction, identify it as software on the **Create New Software spend transactions** form.

    Select the **Is software** check box, and then provide values for the **Publisher** and **Product** fields.

5.  To exclude this transaction from being shared with the Software Asset Management Content Library team, expand the **More details** section and select the **Exclude from content service** check box.

6.  Select **Save**.

    The transaction is created with the **State** field set to **New** and appears in the All transactions list. The **SAM - Label Spend Transactions** scheduled job processes the transaction on its next run.

    If you provided valid values for the **Is software**, **Publisher**, or **Product** fields during creation, the state changes to **Manually labeled** after save. For details on values of the State field, see [AI-powered software spend detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md).


**Parent Topic:**[Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/software-spend-detection.md)

**Related topics**  


[Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-spend-transactions.md)

[Managing software spend in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-sam-workspace.md)

[AI-powered software spend detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md)

[Software spend transaction fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/software-spend-transaction-fields.md)

