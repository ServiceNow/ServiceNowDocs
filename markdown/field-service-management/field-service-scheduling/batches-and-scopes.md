---
title: Batches and scopes
description: Learn how batches and scopes work together to control when Schedule Optimization runs and which technicians and tasks it considers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/batches-and-scopes.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Batches and scopes

Learn how batches and scopes work together to control when Schedule Optimization runs and which technicians and tasks it considers.

## How batches and scopes work together

A batch controls when and how often Schedule Optimization runs. A scope controls what each run optimizes. Batch optimization requires scopes to run.

A batch can include multiple scopes. You can create a scope or reuse an existing one. Reusing a scope creates a copy of it, including all configuration records, and links the copy to the batch. Changes to the copy don't affect the original scope. When you reuse a scope in more than one batch, schedule the batches so their run times don't overlap. You can schedule batches that use the same scope on different days or back to back.

## Batch configuration

A batch configuration defines the optimization start date, the start and end time, and the run frequency. You can configure up to 36 batches in a 24-hour period. Each batch must last at least two hours, and no more than three batches can overlap.

For example:

-   Batch 1: midnight to 02:00
-   Batch 2: 01:00 to 03:00
-   Batch 3: 02:00 to 04:00

Optimization runs on a continuous or fixed schedule. The default is every seven days. You can also run a batch one time, every day, or every 30, 60, 90, 120, or 180 days. **Schedule now** runs a batch independently of its regular schedule. It doesn't change or delay the next scheduled run.

Schedule Optimization doesn't detect changes to technicians or tasks records during a run. Schedule Optimization applies those changes in the next run.

## Scope configuration

A scope defines the scheduling attribute configuration, assignment horizon offset, assignment horizon range, rank, and qualifiers. The scope start time is relative to the batch start time. If the batch starts today and the scope start time is tomorrow, optimization focuses on the technicians and tasks for the next day.

A scope also includes:

-   Assignment horizon offset: The delay between the batch run and the start of task assignments. This value determines the window start value on the work order task.
-   Assignment horizon range: The span of time during which tasks are assigned to technicians.
-   Rank: The scope priority when scopes share tasks. Lower numbers indicate a higher priority.
-   Qualifiers: The assignment groups or territories that the scope optimizes.

## Qualifiers

Qualifiers define which assignment groups or territories a scope optimizes.

-   Assignment group qualifiers: Each assignment group must have a unique set of technicians. A technician can't belong to more than one assignment group.
-   Territory qualifiers: A technician can belong to more than one territory. When territories share technicians or tasks, optimization treats them as one group and optimizes them together.

When the Territory Planning plugin is installed and the Territory Model is active, qualifiers are set to territories automatically, and you can't create scopes for assignment groups. For more information, see [Territory-Based Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/territory-based-optimization.md).

**Related topics**  


[Create a scope for Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/create-an-optimization-job-soe.md)

[Create a batch for Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/create-an-optimization-batch.md)

[Add or remove scopes from an optimization batch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/add-remove-scopes-batch.md)

