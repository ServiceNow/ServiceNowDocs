---
title: General ledger - Legacy
description: The general ledger contains all expenses for your organization for all fiscal periods.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Financial data import - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# General ledger - Legacy

The general ledger contains all expenses for your organization for all fiscal periods.

The general ledger contains these types of expenses:

-   **Staged expenses** that you [imported from your external source](c_FinancialManagementImport.md). Imported expenses are saved in the General Ledger Staged Data \[itfm\_gl\_data\_staged\] table.
-   **Cleansed expenses** that the workbench uses during the Data Cleansing stage. Changes to expenses during this stage are saved in the General Ledger Cleansed Data \[itfm\_gl\_data\_cleansed\] table. Each time you add an expense to the General Ledger Staged Data table, a corresponding expense is created in this table.
-   **Groomed expenses** that the workbench uses during the Bucketing stage. Changes to expenses during this stage are saved in the Groomed General Ledger Data \[itfm\_gl\_data\_groomed\] table. This is also used for non-General Ledger expenses to hold the amounts manually entered through the workbench or to enter the amounts directly.

**Parent Topic:**[Financial data import - Legacy](c_FinancialManagementImport.md)

