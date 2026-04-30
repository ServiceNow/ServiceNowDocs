---
title: Create a known error article from the Source-to-Pay Workspace
description: Create known error articles to document the root cause and the workaround of a problem to help with resolving incidents.
locale: en-US
release: zurich
product: Source-to-Pay Workspace
classification: source-to-pay-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Workspace, Source-to-Pay Operations, Finance and Supply Chain]
---

# Create a known error article from the Source-to-Pay Workspace

Create known error articles to document the root cause and the workaround of a problem to help with resolving incidents.

## Before you begin

Role required: sn\_slm.manager, sn\_shop.procurement\_specialist\_manager, or admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **Knowledge**, and then select one of the following:

    -   **Supplier articles**
    -   **Procurement articles**
4.  Select **New**.

5.  In the Create article dialog box, do the following:

    -   In the **Knowledge Base** field, select **Purchase and Expense** or **Supplier Knowledge**.
    -   In the **Article Template** field, select **Known Error article**.
    -   Select **Create Article.**
6.  On the Create New Known Error article form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Read-only field. Unique number to identify the known error article.|
    |Knowledge base|Knowledge base to which this article belongs.|
    |Category|Category of the article. Use the category picker to select an existing category or subcategory.|
    |Valid to|Date after which the known error article is deleted from the database. After this date, the article does not appear in the search result.|
    |Version|Read-only field. Managed by the Knowledge Management process when changes are made to a published article.|
    |Workflow|Status of the article.|
    |Source Task|Read-only field. The Problem record on which you are creating the article.|
    |Attachment link|Select the check box so that the article appears as an attachment in the Problem record. If you do not select the check box, the content of the article appears in the work note of the Problem.|
    |Display attachments|Display of attachments in the article. When you do not select this option, the article does not display the attachments.|
    |Short description|Short description of the known error.|
    |Description|Detailed explanation of the known error.|
    |Workaround|Method that you have used to overcome the problem. It can be a way of dealing with a problem or making something work despite the problem not being resolved.|
    |Cause|Information about what had caused the problem.|

7.  Select **Save**.


**Parent Topic:**[Use Source-to-Pay Workspace](../../accounts-payable-operations/concept/using-source-to-pay-ws.md)

