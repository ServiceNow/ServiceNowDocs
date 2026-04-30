---
title: Prerequisites to modify data source of a cost model
description: Clean the cost model of its existing data source and all the data collected and accumulated in the associated tables. Follow the steps to seamlessly change the data source.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a cost model from Cost Model form, Cost models, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Prerequisites to modify data source of a cost model

Clean the cost model of its existing data source and all the data collected and accumulated in the associated tables. Follow the steps to seamlessly change the data source.

## Steps to change the data source of a cost model

1.  Remove the following data from their respective tables:
    1.  The allocation breakdowns for the cost model from the Cost Allocation Breakdown Aggregate \[itfm\_allocation\_breakdown\] table.
    2.  The allocation for the cost model from Cost Allocation \[itfm\_allocation\] table.
    3.  The allocation aggregates for the cost model from the Cost Allocation Aggregate \[itfm\_allocation\_aggregate\] table.
    4.  The groomed records for the cost model from the Groomed General Ledger Data \[Itfm\_gl\_data\_groomed\] table.
    5.  The cleansed records for the cost model from the General Ledger Cleansed Data \[itfm\_gl\_data\_cleansed\] table.
    6.  The records from the Cost Allocation Runs Log \[itfm\_ca\_run\_log\] table for the cost model.
2.  Modify the data source of the cost model.

**Parent Topic:**[Create a cost model from Cost Model form](../task/t_CreateACostModel.md)

