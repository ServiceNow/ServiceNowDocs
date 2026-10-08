---
title: Add or remove scopes from an optimization batch
description: Add a scope to a batch to include it in optimization runs, or remove a scope to reduce the number of scopes the batch contains.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/add-remove-scopes-batch.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Batches and scopes, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Add or remove scopes from an optimization batch

Add a scope to a batch to include it in optimization runs, or remove a scope to reduce the number of scopes the batch contains.

## Before you begin

To add a scope, create it first. See [Create a scope for Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/create-an-optimization-job-soe.md).

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Batches**.

2.  Select the optimization batch that you want to add or remove a scope from.

3.  In the **Optimization Scopes** tab, select **Edit**.

4.  Select the scope.

5.  Add or remove the scope:

    -   To add the scope, select **Add**.
    -   To remove the scope, select **Remove**.
6.  Select **Save**.

    **Note:** When you add an existing scope, a copy of the scope is created and linked to the batch. If the scope is used in more than one batch, schedule the batches so their run times don't overlap. For more information, see [Schedule Optimization batches and scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/batches-and-scopes.md).


## Result

The batch includes the scope you added, or no longer includes the scope you removed.

**Related topics**  


[Batches and scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/batches-and-scopes.md)

[Create a scope for Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/create-an-optimization-job-soe.md)

[Create a batch for Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/create-an-optimization-batch.md)

