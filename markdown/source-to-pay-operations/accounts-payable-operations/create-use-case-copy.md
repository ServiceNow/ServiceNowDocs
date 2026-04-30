---
title: Create a copy of the default Invoice Processing use case
description: Create a copy of the default invoice processing use case to customize the invoice flow in your environment.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence, Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Create a copy of the default Invoice Processing use case

Create a copy of the default invoice processing use case to customize the invoice flow in your environment.

## Before you begin

Ensure that the application scope is set to Accounts Payable Operations integration with Document Intelligence.

Role required: admin

## About this task

Do this task to copy the default **DO NOT USE- Invoice Processing V5** use case along with its fields, field groups, integrations, flows, and all the related machine learning \(ML\) models.

## Procedure

1.  Navigate to **Workspaces** &gt; **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Use cases**.

2.  Open the **DO NOT USE- Invoice Processing V5** use case.

3.  Select **Duplicate use case** icon.

    You will be prompted with a message `"Choose the name for this use case"`.

4.  Click **Duplicate** button

    -   The copy is saved automatically into your environment.
    -   A copy of the DO NOT USE - Invoice Processing V5 use case is created with the name entered. You can see the copied use case by navigating to **All** &gt; **Document Intelligence** &gt; **Use Cases**. For more information on configuring use case, see [Configuring Document Intelligence](https://www.servicenow.com/docs/access?context=doc-intel-administration&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
    -   A flow named DocIntel Extract Values Flow is created. This flow is suffixed with the name of the copied use case that was created after you clicked the copy icon. For example, DocIntel Extract Values Flow - name of the entered use case - Invoice Processing v3. You can see this flow by navigating to **All** &gt; **Process Automation** &gt; **Flow Designer** and searching for the flow name.

        You must add the missing information in the newly created flow by copying the existing information from the default DocIntel Extract Values Flow - Invoice Processing v3. For more information, see [Configure the newly created DocIntel Extract Values Flow](configure-extract-values-flow.md).


