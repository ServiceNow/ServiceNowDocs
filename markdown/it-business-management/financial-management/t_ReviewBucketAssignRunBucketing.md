---
title: Review bucket assignments and run bucketing
description: After the data is in buckets, you can see the total amounts for each bucket and the individual general ledger expense records for each bucket.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [The Bucketing stage, Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Review bucket assignments and run bucketing

After the data is in buckets, you can see the total amounts for each bucket and the individual general ledger expense records for each bucket.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Click the information icon \(![The information icon](../image/Information_icon.png)\) on any bucket to display summary information about the bucket.

2.  Under **Advanced Conditions**, verify that the bucket filter condition is correct.

    1.  Click the condition name to open the bucket filter condition form and make changes if necessary.

    2.  Under **Detailed Rows**, click **Show Details** to show the expense records, which are saved in the General Ledger Cleansed Data \[itfm\_gl\_data\_cleansed\] table, that are assigned to the bucket.

    3.  To remove a bucket filter condition, click the delete icon \(![The delete icon](../image/Delete_icon.png)\).

3.  Under **Accounts Assigned**, verify that the correct accounts and all the expenses in them appear in the bucket.

    1.  Click the account name to show the expense records from the General Ledger Cleansed Data table that are assigned to the bucket.

    2.  To remove an account and all expenses that belong to the account from the bucket, click the delete icon \(![The delete icon](../image/Delete_icon.png)\).

4.  Under **Fields to Keep**, select the check boxes for fields you want to keep on the records in the bucket.

    ![Bucket summary](../image/Bucket_summary_bucketing_stage.png "Bucket summary")

5.  Close the window when you are finished.

6.  When the data is correct, click **Run Bucketing** on the right pane.

    -   When you run the bucketing engine, the data is saved in the Groomed General Ledger Data \[itfm\_gl\_data\_groomed\] table.
    -   The application deletes all existing allocation lines for the fiscal period you are working with when you click **Run Bucketing**.

**Parent Topic:**[The Bucketing stage](../concept/c_TheDataBucketingStage.md)

**Related topics**  


[View account details](t_ViewAccountDetails.md)

[Create and modify buckets](t_CreateAndModifyBuckets.md)

[Create bucket filter conditions](t_CreateBucketFilterConditions.md)

[Create groomed lines for cost models with no data source](create-groomed-lines-costmodel-nodatasource.md)

[Put expenses into buckets](t_PutExpensesIntoBuckets.md)

