---
title: Approve application restricted caller access privileges for Sign document supplier task type
description: Approve restricted caller access \(RCA\) privileges after you create a supplier task of action type Sign document for the very first time so that you can create and use subsequent Sign document supplier tasks.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure document template for the Sign document action type, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Approve application restricted caller access privileges for Sign document supplier task type

Approve restricted caller access \(RCA\) privileges after you create a supplier task of action type Sign document for the very first time so that you can create and use subsequent Sign document supplier tasks.

## Before you begin

Role required: admin

## About this task

Approving RCAs is a one-time activity.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  Open each RCA record that matches the following filter criteria:

    |Column|Value|
    |------|-----|
    |Status|Requested|
    |Target Scope|Document Templates|
    |Source Scope|Supplier Common Architecture, Supplier Collaboration Portal, and Source-to-Pay Workspace|

3.  From the **Status** list, select **Allowed**.

4.  Select **Update**.


**Parent Topic:**[Configure the document template for the Sign document action type for supplier task](configure-pdf-template-sign-doc-task.md)

**Related topics**  


[Configure the document template for the Sign document action type for supplier task](configure-pdf-template-sign-doc-task.md)

