---
title: Create bucket filter conditions - Legacy
description: You can also create a condition to filter the data that goes into the bucket. These bucket filter conditions are also called grooming conditions, and they are the Advanced query conditions type.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [The Bucketing stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create bucket filter conditions - Legacy

You can also create a condition to filter the data that goes into the bucket. These bucket filter conditions are also called grooming conditions, and they are the **Advanced query conditions** type.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Click the filter icon in the bucket.

2.  Fill in the form fields \(see table\).

3.  Click **Submit**.

    ![An example bucket filtering condition](../image/Bucket_filter_condition.png "An example bucket filtering condition")

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name for the condition.|
    |Priority|Value that determines when the filter is applied relative to other filters. If two filters have the same settings, the filter with a higher priority is applied.|
    |Table|The table containing the expenses that are filtered when put into the bucket. By default, the General Ledger Cleansed Data \[itfm\_gl\_data\_cleansed\] table is selected.|
    |Advanced bucketing condition|Use the condition builder to create the filter.|

    When you create a bucket filter, it appears in the **Advanced Conditions** tab above the donut chart in the right pane.

    ![The Advanced Conditions tab](../image/Advanced_conditions_summary.png "The Advanced Conditions tab")


## What to do next

You can verify the filter conditions or make changes:

-   Click the name of the condition to open the Advanced Condition form.
-   Click the amount to open the list of general ledger expenses that match the filter.

The advanced filter condition icon also appears on the bucket:

![The advanced filter condition on a bucket](../image/Filter_condition_bucket.png "The advanced filter condition icon on a bucket")

**Parent Topic:**[The Bucketing stage - Legacy](../concept/c_TheDataBucketingStage.md)

**Related topics**  


[View account details - Legacy](t_ViewAccountDetails.md)

[Create and modify buckets - Legacy](t_CreateAndModifyBuckets.md)

[Create groomed lines for cost models with no data source - Legacy](create-groomed-lines-costmodel-nodatasource.md)

[Put expenses into buckets - Legacy](t_PutExpensesIntoBuckets.md)

[Review bucket assignments and run bucketing - Legacy](t_ReviewBucketAssignRunBucketing.md)

