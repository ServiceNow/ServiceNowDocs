---
title: Financial data sources and field maps - Legacy
description: Financial data sources point to the actual raw expense data table used by financial modeling and financial planning.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Financial data import - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial data sources and field maps - Legacy

Financial data sources point to the actual raw expense data table used by financial modeling and financial planning.

In the Financial Management application, the data source helps to map the raw expense data and its fields to the transaction table fields.

You can use the General Ledger Staged Data table and General Budget Staged Data table for base system financial model activities. These tables can also be extended to create a custom source table for your financial model. You can model your financial activities using any data source or without any data source at all. If it is without any data source, then it is expected that the amounts would be manually entered directly into the cost model. You can create more field maps and configure which fields are to be used for cleansing or split bucket, as and when required.

Financial planning uses data source to generate actuals. The segments used in budget model hierarchy must be a mandatory part of data source field maps to accurately map the actuals with the budget. It also helps in budget key generation.

Start working with the following data sources available with the application:

-   GL Staged
-   Cost Plan Breakdown \(FM-PPS financial planning integration\)

The following table lists the default field maps provided with each data source. You can change the default mapping to point to a different segment or column. For example, by default the Cost Center column is mapped to the Cost Center name \[cmn\_cost\_center\]. If the data in that column is the code in your case, then you can change to Cost Center code \[cmn\_cost\_center\]. You can create more field maps for the custom fields as required.

|Segment name|Transaction table|
|------------|-----------------|
|Cost Center|Cost Center \[cmn\_cost\_center\]|
|Location|Location \[cmn\_location\]|
|Vendor|Company \[core\_company\]|
|Department|Department \[cmn\_department\]|
|Project|Project \[pm\_project\]|

![Financial data source field mappings.](../image/DataSourceFieldMaps.png "Financial data source and its field maps")

**Parent Topic:**[Financial data import - Legacy](c_FinancialManagementImport.md)

