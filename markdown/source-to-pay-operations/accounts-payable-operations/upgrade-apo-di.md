---
title: Upgrade configuration for Accounts Payable Operations integration with Document Intelligence
description: After you upgrade Accounts Payable Operations to the latest version, you must review all the post-upgrade tasks and complete them as needed. Upgrade the copied use case to the latest Document Intelligence model.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Post upgrade tasks for APO, Upgrade Accounts Payable Operations, Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Upgrade configuration for Accounts Payable Operations integration with Document Intelligence

After you upgrade Accounts Payable Operations to the latest version, you must review all the post-upgrade tasks and complete them as needed. Upgrade the copied use case to the latest Document Intelligence model.

## Before you begin

Role required: admin

Install the Document Intelligence for Accounts Payable Operations Content Pack from the ServiceNow® Store.

## Procedure

1.  Select the DO NOT USE- Invoice processing V7 use case as source.

2.  Navigate to **All** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

3.  Search for DO NOT USE- Invoice processing V7 and create a duplicate copy using the ![duplicate icon](../image/duplicate-di-usecase.png) icon.

4.  Save the copied use case.

    Use the copied use case in flows and task definitions.

5.  To upgrade the copied use case to the latest Document Intelligence model, perform the following steps:

    1.  Navigate to **All** &gt; **Fix Scripts**.

    2.  Search for Update DocIntel base\_trained\_model and select **Run Fix Script**.


## Result

The existing copied use case is updated to the latest DI base model.

**Related topics**  


[Run the fix script for Accounts Payable Operations](run-fix-script-for-apo.md)

[Accounts Payable Operations integration with Document Intelligence](../concept/apo-docintel-integration.md)

